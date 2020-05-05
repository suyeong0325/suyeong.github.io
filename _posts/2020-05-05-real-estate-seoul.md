---
layout: post
title: Spatial Map of Real Estate Market Price
image: /img/preview_apt.JPG
tags: [Python, API, SQL, Real Estate, Market Price]
bigimg: /img/header_apt.JPG
comments: true
---

The aim of the project is to create a spatial map of market prices of apartments in Seoul, South Korea. Real estate transection histories in 2019 is acquired from the official website of Ministry of Land, Infrastructure and Transport, South Korea (http://rtdown.molit.go.kr/) and modified with simple SQL queries to derive average prices of each address.


**Convert address to sub-region and xy coordinates using Kakao-local API**

~~~
url="https://dapi.kakao.com/v2/local/search/address" #basic string for a test
header={'authorization':'API-Key'}
df_perm=pd.DataFrame({"region":[],"x":[], "y":[]}) #create empty coordinates dataframe
for i in range(0, 6107): #6107 rows
    address={"query":seoul_apt["ADD_KOR"][i]}
    r=requests.get(url, headers=header, params=address)
    full_address=json.loads(r.text)
    try:
        region_temp=full_address['documents'][0]['address']['region_3depth_name']
        x_temp=full_address['documents'][0]['address']['x']
        y_temp=full_address['documents'][0]['address']['y']
        df_perm=df_perm.append(pd.DataFrame({"region":[region_temp], "x":[x_temp], "y":[y_temp]}))
    except (IndexError): #errors occur due to null keys in API address DB
        df_perm=df_perm.append(pd.DataFrame({"region":[null], "x":[null], "y":[null]}))
        continue
~~~

Kakao provides local API that converts address to coordinates based on WGS-1984. Since the DB of API has its limitation due to the new address system in South Korea, a few(27) rows recieved null values.

**Visualization of prices according to coordinates**

CARTOframes library is used to visualize the distribution of real estate prices.

~~~
Map([
    Layer(seoul_apt_min,
          color_bins_style('PRICE_PER1000', palette='pinkyl'),
    legends=color_bins_legend(title='Apartment Prices in Seoul, South Korea 2019',
                                    description='(per 1,000 won)',
                                    footer='Ministry of Land, Infrastructure and Transport',
                                    dynamic=False))
          ])
~~~

**Apartment Prices in Seoul, South Korea (2019)**

![per1000](/img/per_1000.JPG)


**Apartment Prices in Seoul, South Korea (2019) - Per sqaure meter**

![per_area](/img/per_area.jpg)

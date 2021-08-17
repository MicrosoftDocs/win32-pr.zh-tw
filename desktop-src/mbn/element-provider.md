---
description: 提供者
MS-HAID: WWAN\_profile\_v4.element\_Provider
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 提供者
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a701c4dd-967f-4f03-ada4-d34059f5a1e4
api_name:
- Provider
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d9208e3c0aad7ab05348056eaf70747aa23433e0ab5badec5da1f2baf063b1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066304"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span id="WWAN_profile_v4.element_Provider"></span>供應商

在漫遊時所要使用的提供者清單中，指定一個慣用的網路提供者。

這個元素的值是 v1 [**providerType**](./schema-providertype-complextype.md) 複雜型別的實例。

## <a name="element-hierarchy"></a>元素階層

[<MBNProfileExt>](element-mbnprofileext.md)  
[<DataRoamingPartners>](element-dataroamingpartners.md)  
**<Provider>**

## <a name="syntax"></a>Syntax

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent 項目</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-dataroamingpartners.md">DataRoamingPartners</a></td>
<td><p>指定漫遊時的慣用網路提供者清單。</p>
<p>如需詳細資訊，請參閱 v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> 元素的檔。</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>命名空間</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 

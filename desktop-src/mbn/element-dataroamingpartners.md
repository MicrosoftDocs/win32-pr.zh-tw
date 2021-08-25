---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: eb304a89faca2381f8c8c0ede6ba743f740c4d0f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468895"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners

指定漫遊時的慣用網路提供者清單。

如需詳細資訊，請參閱 v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) 元素的檔。

## <a name="element-hierarchy"></a>元素階層

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a>Syntax

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a>答案

`+`   需要 (一或多個) 

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目


| 子元素 | Description | 
|---------------|-------------|
| <a href="element-provider.md">提供者</a> | <p>在漫遊時所要使用的提供者清單中，指定一個慣用的網路提供者。</p><p>這個元素的值是 v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> 複雜型別的實例。</p> | 


 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | Description | 
|----------------|-------------|
| <a href="element-mbnprofileext.md">MBNProfileExt</a> | <p><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。 它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</p><p>設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。 使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</p> | 


 

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 

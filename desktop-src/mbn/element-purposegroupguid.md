---
description: PurposeGroupGuid
MS-HAID: WWAN\_profile\_v4.element\_PurposeGroupGuid
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PurposeGroupGuid
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d772a79d1802c99cde571abc1c665c73ddd06c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476074"
---
# <a name="span-idwwan_profile_v4element_purposegroupguidspanpurposegroupguid"></a><span id="WWAN_profile_v4.element_PurposeGroupGuid"></span>PurposeGroupGuid

代表 PurposeGroup 設定檔中的一個設定檔。

設定檔是由其 [**guidType**](simpletype-guidtype.md) 值指定。

定義四個 GUID 值，如下表所示。

| 目的群組 | GUID                                 |
|---------------|--------------------------------------|
| 網際網路      | 3E5545D2-1137-4DC8-A198-33F1C657515F |
| mms           | 53E2C5D3-D13C-4068-AA38-9C48FF2E55A8 |
| IMS           | 474D66ED-0E4B-476B-A455-19BB1239ED13 |
| SUPL          | 6D42669F-52A9-408E-9493-1071DCC437BD |

 

## <a name="element-hierarchy"></a>元素階層

[<MBNProfileExt>](element-mbnprofileext.md)  
[<PurposeGroups>](element-purposegroups.md)  
**<PurposeGroupGuid>**

## <a name="syntax"></a>Syntax

``` syntax
<PurposeGroupGuid>

  guidType

</PurposeGroupGuid>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | Description | 
|----------------|-------------|
| <a href="element-purposegroups.md">PurposeGroups</a> | <p>選用的設定檔群組清單，其中每個群組都包含用於一般用途的設定檔。</p><p>此元素是架構 v4 的新專案。</p><p>一個設定檔可以列在多個群組中。</p> | 


 

## <a name="requirements"></a>規格需求


| | | <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 




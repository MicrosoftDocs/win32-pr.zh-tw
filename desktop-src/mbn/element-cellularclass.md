---
description: CellularClass
MS-HAID: WWAN\_profile\_v4.element\_CellularClass
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CellularClass
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c442208c40dcfa42a7c603bc20fda94422794ef
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988841"
---
# <a name="span-idwwan_profile_v4element_cellularclassspancellularclass"></a><span id="WWAN_profile_v4.element_CellularClass"></span>CellularClass

指定只有當目前的行動電話類別是指定的時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。

## <a name="element-hierarchy"></a>元素階層

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;ProfileConditionedOn&gt;](element-profileconditionedon.md)  
**&lt;CellularClass&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<CellularClass>

  "3GPP" | "3GPP2"

</CellularClass>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | Description | 
|----------------|-------------|
| <a href="element-profileconditionedon.md">ProfileConditionedOn</a> | <p>指定必須滿足的條件，設定檔才適用。</p><p>此元素是 v4 的新專案。 它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。 這是選擇性的項目。 如果您未指定，則設定檔一律適用于所列出的條件。</p> | 


 

## <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 




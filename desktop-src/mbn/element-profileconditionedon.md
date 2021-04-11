---
description: ProfileConditionedOn
MS-HAID: WWAN\_profile\_v4.element\_ProfileConditionedOn
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileConditionedOn
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729b95872be68ea814b35a593082b2366284f0dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112912"
---
# <a name="span-idwwan_profile_v4element_profileconditionedonspanprofileconditionedon"></a><span id="WWAN_profile_v4.element_ProfileConditionedOn"></span>ProfileConditionedOn

指定必須滿足的條件，設定檔才適用。

此元素是 v4 的新專案。 它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。 這是選擇性的項目。 如果您未指定，則設定檔一律適用于所列出的條件。

## <a name="element-hierarchy"></a>元素階層

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ProfileConditionedOn>**

## <a name="syntax"></a>Syntax

``` syntax
<ProfileConditionedOn>

  <!-- Child elements -->
  CellularClass?,
  RATApplicability?,
  RoamApplicability?,
  IMSI?,
  IwlanApplicability?

</ProfileConditionedOn>
```

### <a name="key"></a>答案

`?`   選擇性 (零或一) 

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>子元素</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-cellularclass.md">CellularClass</a></td>
<td><p>指定只有當目前的行動電話類別是指定的時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</p></td>
</tr>
<tr class="even">
<td><a href="element-imsi.md">IMSI</a></td>
<td><p>指定只有在 ICCID 中目前使用的 IMSI 為指定的時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</p></td>
</tr>
<tr class="odd">
<td><a href="element-iwlanapplicability.md">IwlanApplicability</a></td>
<td><p>指定只有在連接到 IWLAN 網路時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。 這個元素的值必須是有效的 <a href="simpletype-iwlanapplicabilitytype.md"><strong>iwlanApplicabilityType</strong></a> 值。</p></td>
</tr>
<tr class="even">
<td><a href="element-ratapplicability.md">RATApplicability</a></td>
<td><p>指定只有當 RAT 類型是指定的時，才會啟用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</p></td>
</tr>
<tr class="odd">
<td><a href="element-roamapplicability.md">RoamApplicability</a></td>
<td><p>指定只有在目前的漫遊條件是指定的漫遊條件時，才會使用此設定檔。 否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。 這個元素的值必須是有效的 <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> 值。</p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parent 項目</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-mbnprofileext.md">MBNProfileExt</a></td>
<td><p><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。 它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</p>
<p>設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。 使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</p></td>
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

 

 




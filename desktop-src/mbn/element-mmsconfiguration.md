---
description: MmsConfiguration
MS-HAID: WWAN\_profile\_v4.element\_MmsConfiguration
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsConfiguration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb98506476558ed0e39df11bab4b9446de4fd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191305"
---
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration

多媒體訊息服務 (MMS) 的設定資訊。

除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。

-   其 [**Name**](element-name.md) 元素必須包含全系統的唯一名稱。
-   其 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) 必須設定為 **UserProvisioned**。
-   其 [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) 必須包含此設定檔所適用之 SIM 的 ICCID。
-   其 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) 必須設定為 **手動**。
-   其 [**PurposeGroupGuid**](element-purposegroupguid.md) 必須包含 MMS 用途群組的 GUID。
-   其 [**IsAdditionalPdpCoNtextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) 必須設定為 **true**。

## <a name="element-hierarchy"></a>元素階層

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a>Syntax

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
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
<td><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></td>
<td><p>指定 MMS 訊息的大小上限（以 kb 為單位）。 選擇性。</p></td>
</tr>
<tr class="even">
<td><a href="element-mmscport.md">MmscPort</a></td>
<td><p>指定裝置之 MMSC 伺服器的埠號碼。 指定0表示未指定特定埠。 選擇性。</p></td>
</tr>
<tr class="odd">
<td><a href="element-mmscurl.md">MmscUrl</a></td>
<td><p>指定裝置的 MMSC 伺服器 URL。 選擇性。</p></td>
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

 

 

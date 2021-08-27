---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab913845a12f8a54c9cbc4f65de5208f7661555
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986271"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl

指定裝置的 MMSC 伺服器 URL。 選擇性。

## <a name="element-hierarchy"></a>元素階層

[&lt;MBNProfileExt&gt;](element-mbnprofileext.md)  
[&lt;MmsConfiguration&gt;](element-mmsconfiguration.md)  
**&lt;MmscUrl&gt;**

## <a name="syntax"></a>Syntax

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性

無。

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目

無。

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素


| Parent 項目 | Description | 
|----------------|-------------|
| <a href="element-mmsconfiguration.md">MmsConfiguration</a> | <p>多媒體訊息服務 (MMS) 的設定資訊。</p><p>除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</p><ul><li>其 <a href="element-name.md"><strong>Name</strong></a> 元素必須包含全系統的唯一名稱。</li><li>其 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 必須設定為 <strong>UserProvisioned</strong>。</li><li>其 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 必須包含此設定檔所適用之 SIM 的 ICCID。</li><li>其 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 必須設定為 <strong>手動</strong>。</li><li>其 <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> 必須包含 MMS 用途群組的 GUID。</li><li>其 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 必須設定為 <strong>true</strong>。</li></ul> | 


 

## <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p>命名空間</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 

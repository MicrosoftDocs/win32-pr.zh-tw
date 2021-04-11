---
description: MmscUrl
MS-HAID: WWAN\_profile\_v4.element\_MmscUrl
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmscUrl
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319146573e4782365b7db67c453a0866f198d61b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943409"
---
# <a name="span-idwwan_profile_v4element_mmscurlspanmmscurl"></a><span data-ttu-id="691db-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl</span><span class="sxs-lookup"><span data-stu-id="691db-103"><span id="WWAN_profile_v4.element_MmscUrl"></span>MmscUrl</span></span>

<span data-ttu-id="691db-104">指定裝置的 MMSC 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="691db-104">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="691db-105">選擇性。</span><span class="sxs-lookup"><span data-stu-id="691db-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="691db-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="691db-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmscUrl>**

## <a name="syntax"></a><span data-ttu-id="691db-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="691db-107">Syntax</span></span>

``` syntax
<MmscUrl>

  anyURI

</MmscUrl>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="691db-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="691db-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="691db-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="691db-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="691db-110">無。</span><span class="sxs-lookup"><span data-stu-id="691db-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="691db-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="691db-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="691db-112">無。</span><span class="sxs-lookup"><span data-stu-id="691db-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="691db-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="691db-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="691db-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="691db-114">Parent Element</span></span></th>
<th><span data-ttu-id="691db-115">Description</span><span class="sxs-lookup"><span data-stu-id="691db-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="691db-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="691db-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="691db-117">多媒體訊息服務 (MMS) 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="691db-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="691db-118">除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</span><span class="sxs-lookup"><span data-stu-id="691db-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="691db-119">其 <a href="element-name.md"><strong>Name</strong></a> 元素必須包含全系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="691db-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="691db-120">其 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 必須設定為 <strong>UserProvisioned</strong>。</span><span class="sxs-lookup"><span data-stu-id="691db-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="691db-121">其 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 必須包含此設定檔所適用之 SIM 的 ICCID。</span><span class="sxs-lookup"><span data-stu-id="691db-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="691db-122">其 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 必須設定為 <strong>手動</strong>。</span><span class="sxs-lookup"><span data-stu-id="691db-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="691db-123">其 <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> 必須包含 MMS 用途群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="691db-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="691db-124">其 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 必須設定為 <strong>true</strong>。</span><span class="sxs-lookup"><span data-stu-id="691db-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="691db-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="691db-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="691db-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="691db-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 

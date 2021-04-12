---
description: MmsMaximumMessageSize
MS-HAID: WWAN\_profile\_v4.element\_MmsMaximumMessageSize
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MmsMaximumMessageSize
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5b020e7fd6ad4f39bd488c3af0ef14a3aab1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191448"
---
# <a name="span-idwwan_profile_v4element_mmsmaximummessagesizespanmmsmaximummessagesize"></a><span data-ttu-id="775e7-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span><span class="sxs-lookup"><span data-stu-id="775e7-103"><span id="WWAN_profile_v4.element_MmsMaximumMessageSize"></span>MmsMaximumMessageSize</span></span>

<span data-ttu-id="775e7-104">指定 MMS 訊息的大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="775e7-104">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="775e7-105">選擇性。</span><span class="sxs-lookup"><span data-stu-id="775e7-105">Optional.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="775e7-106">元素階層</span><span class="sxs-lookup"><span data-stu-id="775e7-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<MmsConfiguration>](element-mmsconfiguration.md)  
**<MmsMaximumMessageSize>**

## <a name="syntax"></a><span data-ttu-id="775e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="775e7-107">Syntax</span></span>

``` syntax
<MmsMaximumMessageSize>

  nonNegativeInteger

</MmsMaximumMessageSize>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="775e7-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="775e7-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="775e7-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="775e7-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="775e7-110">無。</span><span class="sxs-lookup"><span data-stu-id="775e7-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="775e7-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="775e7-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="775e7-112">無。</span><span class="sxs-lookup"><span data-stu-id="775e7-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="775e7-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="775e7-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="775e7-114">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="775e7-114">Parent Element</span></span></th>
<th><span data-ttu-id="775e7-115">Description</span><span class="sxs-lookup"><span data-stu-id="775e7-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="775e7-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="775e7-116"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="775e7-117">多媒體訊息服務 (MMS) 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="775e7-117">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="775e7-118">除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</span><span class="sxs-lookup"><span data-stu-id="775e7-118">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="775e7-119">其 <a href="element-name.md"><strong>Name</strong></a> 元素必須包含全系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="775e7-119">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="775e7-120">其 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 必須設定為 <strong>UserProvisioned</strong>。</span><span class="sxs-lookup"><span data-stu-id="775e7-120">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="775e7-121">其 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 必須包含此設定檔所適用之 SIM 的 ICCID。</span><span class="sxs-lookup"><span data-stu-id="775e7-121">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="775e7-122">其 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 必須設定為 <strong>手動</strong>。</span><span class="sxs-lookup"><span data-stu-id="775e7-122">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="775e7-123">其 <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> 必須包含 MMS 用途群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="775e7-123">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="775e7-124">其 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 必須設定為 <strong>true</strong>。</span><span class="sxs-lookup"><span data-stu-id="775e7-124">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="775e7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="775e7-125">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="775e7-126">命名空間</span><span class="sxs-lookup"><span data-stu-id="775e7-126">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 

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
# <a name="span-idwwan_profile_v4element_mmsconfigurationspanmmsconfiguration"></a><span data-ttu-id="00d06-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span><span class="sxs-lookup"><span data-stu-id="00d06-103"><span id="WWAN_profile_v4.element_MmsConfiguration"></span>MmsConfiguration</span></span>

<span data-ttu-id="00d06-104">多媒體訊息服務 (MMS) 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="00d06-104">Configuration information for Multimedia Messaging Service (MMS).</span></span>

<span data-ttu-id="00d06-105">除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</span><span class="sxs-lookup"><span data-stu-id="00d06-105">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span>

-   <span data-ttu-id="00d06-106">其 [**Name**](element-name.md) 元素必須包含全系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="00d06-106">Its [**Name**](element-name.md) element must contain a system-wide unique name.</span></span>
-   <span data-ttu-id="00d06-107">其 [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) 必須設定為 **UserProvisioned**。</span><span class="sxs-lookup"><span data-stu-id="00d06-107">Its [**ProfileCreationType**](./schema-profilecreationtype-mbnprofile-element.md) must be set to **UserProvisioned**.</span></span>
-   <span data-ttu-id="00d06-108">其 [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) 必須包含此設定檔所適用之 SIM 的 ICCID。</span><span class="sxs-lookup"><span data-stu-id="00d06-108">Its [**SimIccID**](/windows/win32/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid) must contain the ICCID of the SIM that this profile is intended for.</span></span>
-   <span data-ttu-id="00d06-109">其 [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) 必須設定為 **手動**。</span><span class="sxs-lookup"><span data-stu-id="00d06-109">Its [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) must be set to **Manual**.</span></span>
-   <span data-ttu-id="00d06-110">其 [**PurposeGroupGuid**](element-purposegroupguid.md) 必須包含 MMS 用途群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="00d06-110">Its [**PurposeGroupGuid**](element-purposegroupguid.md) must contain the GUID for MMS purpose group.</span></span>
-   <span data-ttu-id="00d06-111">其 [**IsAdditionalPdpCoNtextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) 必須設定為 **true**。</span><span class="sxs-lookup"><span data-stu-id="00d06-111">Its [**IsAdditionalPdpContextProfile**](/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)) must be set to **true**.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="00d06-112">元素階層</span><span class="sxs-lookup"><span data-stu-id="00d06-112">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<MmsConfiguration>**

## <a name="syntax"></a><span data-ttu-id="00d06-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d06-113">Syntax</span></span>

``` syntax
<MmsConfiguration>

  <!-- Child elements -->
  MmscUrl?,
  MmscPort?,
  MmsMaximumMessageSize?

</MmsConfiguration>
```

### <a name="key"></a><span data-ttu-id="00d06-114">答案</span><span class="sxs-lookup"><span data-stu-id="00d06-114">Key</span></span>

<span data-ttu-id="00d06-115">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="00d06-115">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="00d06-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="00d06-116"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="00d06-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="00d06-117"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="00d06-118">無。</span><span class="sxs-lookup"><span data-stu-id="00d06-118">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="00d06-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="00d06-119"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d06-120">子元素</span><span class="sxs-lookup"><span data-stu-id="00d06-120">Child Element</span></span></th>
<th><span data-ttu-id="00d06-121">Description</span><span class="sxs-lookup"><span data-stu-id="00d06-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00d06-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span><span class="sxs-lookup"><span data-stu-id="00d06-122"><a href="element-mmsmaximummessagesize.md">MmsMaximumMessageSize</a></span></span></td>
<td><p><span data-ttu-id="00d06-123">指定 MMS 訊息的大小上限（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="00d06-123">Specifies the maximum size of MMS messages, in kilobytes.</span></span> <span data-ttu-id="00d06-124">選擇性。</span><span class="sxs-lookup"><span data-stu-id="00d06-124">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="00d06-125"><a href="element-mmscport.md">MmscPort</a></span><span class="sxs-lookup"><span data-stu-id="00d06-125"><a href="element-mmscport.md">MmscPort</a></span></span></td>
<td><p><span data-ttu-id="00d06-126">指定裝置之 MMSC 伺服器的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="00d06-126">Specifies the port number of the MMSC server for the device.</span></span> <span data-ttu-id="00d06-127">指定0表示未指定特定埠。</span><span class="sxs-lookup"><span data-stu-id="00d06-127">Specify 0 to indicate that no specific port is specified.</span></span> <span data-ttu-id="00d06-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="00d06-128">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="00d06-129"><a href="element-mmscurl.md">MmscUrl</a></span><span class="sxs-lookup"><span data-stu-id="00d06-129"><a href="element-mmscurl.md">MmscUrl</a></span></span></td>
<td><p><span data-ttu-id="00d06-130">指定裝置的 MMSC 伺服器 URL。</span><span class="sxs-lookup"><span data-stu-id="00d06-130">Specifies the URL of the MMSC server for the device.</span></span> <span data-ttu-id="00d06-131">選擇性。</span><span class="sxs-lookup"><span data-stu-id="00d06-131">Optional.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="00d06-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="00d06-132"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="00d06-133">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="00d06-133">Parent Element</span></span></th>
<th><span data-ttu-id="00d06-134">Description</span><span class="sxs-lookup"><span data-stu-id="00d06-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00d06-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="00d06-135"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="00d06-136"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="00d06-136">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="00d06-137">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="00d06-137">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="00d06-138">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="00d06-138">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="00d06-139">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="00d06-139">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="00d06-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="00d06-140">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00d06-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="00d06-141">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 

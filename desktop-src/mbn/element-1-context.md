---
description: ModemDMConfigProfile \/ (v4) 的內容
MS-HAID: WWAN\_profile\_v4.element\_1\_Context
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: " (v4) 的內容"
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8f463f14-95b3-4364-b1b1-549a32291959
api_name:
- Context
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 133f48d9c9a1c9dd9f0e04f59d5e35478caa9227
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106979646"
---
# <a name="span-idwwan_profile_v4element_1_contextspanmodemdmconfigprofilecontext-v4"></a><span data-ttu-id="6b28e-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile \/ (v4) 的內容</span><span class="sxs-lookup"><span data-stu-id="6b28e-103"><span id="WWAN_profile_v4.element_1_Context"></span>ModemDMConfigProfile\/Context (v4)</span></span>

<span data-ttu-id="6b28e-104">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="6b28e-104">Specifies the parameters required to establish a data connection.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="6b28e-105">元素階層</span><span class="sxs-lookup"><span data-stu-id="6b28e-105">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;**\<Context\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;**\<Context\>**

## <a name="syntax"></a><span data-ttu-id="6b28e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b28e-106">Syntax</span></span>

``` syntax
<Context>

  <!-- Child elements -->
  AccessString?,
  UserLogonCred?,
  Compression?,
  AuthProtocol?,
  IPType?

</Context>
```

### <a name="key"></a><span data-ttu-id="6b28e-107">答案</span><span class="sxs-lookup"><span data-stu-id="6b28e-107">Key</span></span>

<span data-ttu-id="6b28e-108">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="6b28e-108">`?`   optional (zero or one)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="6b28e-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="6b28e-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="6b28e-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="6b28e-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="6b28e-111">無。</span><span class="sxs-lookup"><span data-stu-id="6b28e-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="6b28e-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="6b28e-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b28e-113">子元素</span><span class="sxs-lookup"><span data-stu-id="6b28e-113">Child Element</span></span></th>
<th><span data-ttu-id="6b28e-114">Description</span><span class="sxs-lookup"><span data-stu-id="6b28e-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b28e-115"><a href="element-1-accessstring.md">AccessString</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-115"><a href="element-1-accessstring.md">AccessString</a></span></span></td>
<td><p><span data-ttu-id="6b28e-116">識別要用來建立資料連線的 APN 或撥號字串。</span><span class="sxs-lookup"><span data-stu-id="6b28e-116">Identifies the APN or dial string to be used to establish a data connection.</span></span></p>
<p><span data-ttu-id="6b28e-117">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-117">For more information, see the documentation for the v1 <a href="../mbn/schema-accessstring-contexttype-element.md"><strong>AccessString</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b28e-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-118"><a href="element-1-authprotocol.md">AuthProtocol</a></span></span></td>
<td><p><span data-ttu-id="6b28e-119">>指定要用於啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6b28e-119">>Specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span></p>
<p><span data-ttu-id="6b28e-120">請注意，在 v4 中，此元素有新的列舉值。</span><span class="sxs-lookup"><span data-stu-id="6b28e-120">Note that in v4, a new enumeration value is available for this element.</span></span> <span data-ttu-id="6b28e-121"><strong>AutoSelection</strong> 表示驗證通訊協定是由較低層 (s) 挑選。</span><span class="sxs-lookup"><span data-stu-id="6b28e-121"><strong>AutoSelection</strong> means that an auth protocol is to be picked by lower layer(s).</span></span></p>
<p><span data-ttu-id="6b28e-122">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-122">For further information, see the documentation for the v1 <a href="../mbn/schema-authprotocol-contexttype-element.md"><strong>AuthProtocol</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b28e-123"><a href="element-1-compression.md">壓縮</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-123"><a href="element-1-compression.md">Compression</a></span></span></td>
<td><p><span data-ttu-id="6b28e-124">指定是否要在資料連結上使用壓縮來進行標頭和資料傳輸。</span><span class="sxs-lookup"><span data-stu-id="6b28e-124">Specifies whether compression will be used at the data link for header and data transfer.</span></span></p>
<p><span data-ttu-id="6b28e-125">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>壓縮</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-125">For more information, see the documentation for the v1 <a href="../mbn/schema-compression-contexttype-element.md"><strong>Compression</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b28e-126"><a href="element-1-iptype.md">IPType</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-126"><a href="element-1-iptype.md">IPType</a></span></span></td>
<td><p><span data-ttu-id="6b28e-127">指定要用於此資料連線的 IP 類型。</span><span class="sxs-lookup"><span data-stu-id="6b28e-127">Specifies the IP type to be used on this data connection.</span></span></p>
<p><span data-ttu-id="6b28e-128">此元素是架構 v4 中的新專案。</span><span class="sxs-lookup"><span data-stu-id="6b28e-128">This element is new in v4 of the schema.</span></span> <span data-ttu-id="6b28e-129">元素可以具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6b28e-129">The element can have one of the following values.</span></span></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6b28e-130">值</span><span class="sxs-lookup"><span data-stu-id="6b28e-130">Value</span></span></th>
<th><span data-ttu-id="6b28e-131">意義</span><span class="sxs-lookup"><span data-stu-id="6b28e-131">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b28e-132">預設</span><span class="sxs-lookup"><span data-stu-id="6b28e-132">Default</span></span></td>
<td><span data-ttu-id="6b28e-133">IP 類型是由較低層 () 所挑選</span><span class="sxs-lookup"><span data-stu-id="6b28e-133">IP type is to be picked by lower layer(s)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b28e-134">IPv4</span><span class="sxs-lookup"><span data-stu-id="6b28e-134">IPv4</span></span></td>
<td><span data-ttu-id="6b28e-135">使用 IPv4</span><span class="sxs-lookup"><span data-stu-id="6b28e-135">Use IPv4</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b28e-136">IPv6</span><span class="sxs-lookup"><span data-stu-id="6b28e-136">IPv6</span></span></td>
<td><span data-ttu-id="6b28e-137">使用 IPv6</span><span class="sxs-lookup"><span data-stu-id="6b28e-137">Use IPv6</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b28e-138">IPv4v6</span><span class="sxs-lookup"><span data-stu-id="6b28e-138">IPv4v6</span></span></td>
<td><span data-ttu-id="6b28e-139">使用 IPv4 和（或） IPv6 （如有提供）。</span><span class="sxs-lookup"><span data-stu-id="6b28e-139">Use IPv4 and/or IPv6, as available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b28e-140">XLAT</span><span class="sxs-lookup"><span data-stu-id="6b28e-140">XLAT</span></span></td>
<td><span data-ttu-id="6b28e-141">使用464XLAT 透過 IPv6 網路將 IPv4 通道</span><span class="sxs-lookup"><span data-stu-id="6b28e-141">Use 464XLAT to tunnel IPv4 over IPv6 networks</span></span></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b28e-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-142"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="6b28e-143">連接的登入認證。</span><span class="sxs-lookup"><span data-stu-id="6b28e-143">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="6b28e-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="6b28e-144"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b28e-145">Parent 項目</span><span class="sxs-lookup"><span data-stu-id="6b28e-145">Parent Element</span></span></th>
<th><span data-ttu-id="6b28e-146">Description</span><span class="sxs-lookup"><span data-stu-id="6b28e-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b28e-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-147"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="6b28e-148"><strong>MBNProfileExt</strong>元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6b28e-148">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="6b28e-149">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-149">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="6b28e-150">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="6b28e-150">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="6b28e-151">使用<strong>MBNProfileExt</strong>的<a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a>子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-151">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b28e-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="6b28e-152"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="6b28e-153">數據機 DM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6b28e-153">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="6b28e-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b28e-154">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b28e-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="6b28e-155">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 




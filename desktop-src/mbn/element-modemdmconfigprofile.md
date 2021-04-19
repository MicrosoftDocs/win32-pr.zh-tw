---
description: ModemDMConfigProfile
MS-HAID: WWAN\_profile\_v4.element\_ModemDMConfigProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ModemDMConfigProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43f4593d1b55b4c95a2ec185fe5545ad7eb04141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973055"
---
# <a name="span-idwwan_profile_v4element_modemdmconfigprofilespanmodemdmconfigprofile"></a><span data-ttu-id="dfd51-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span><span class="sxs-lookup"><span data-stu-id="dfd51-103"><span id="WWAN_profile_v4.element_ModemDMConfigProfile"></span>ModemDMConfigProfile</span></span>

<span data-ttu-id="dfd51-104">數據機 DM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-104">Modem DM configuration profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="dfd51-105">元素階層</span><span class="sxs-lookup"><span data-stu-id="dfd51-105">Element hierarchy</span></span>

**<ModemDMConfigProfile>**

## <a name="syntax"></a><span data-ttu-id="dfd51-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfd51-106">Syntax</span></span>

``` syntax
<ModemDMConfigProfile>

  <!-- Child elements -->
  Name,
  SimIccID,
  ApnID,
  OemConnectionId,
  RoamApplicability?,
  Context,
  AdminEnable,
  AdminRoamControl,
  ProfileCreationType?,
  any element in a non-schema namespace*

</ModemDMConfigProfile>
```

### <a name="key"></a><span data-ttu-id="dfd51-107">答案</span><span class="sxs-lookup"><span data-stu-id="dfd51-107">Key</span></span>

<span data-ttu-id="dfd51-108">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="dfd51-108">`?`   optional (zero or one)</span></span>

<span data-ttu-id="dfd51-109">`*`   選擇性 (零或多個) </span><span class="sxs-lookup"><span data-stu-id="dfd51-109">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="dfd51-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="dfd51-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="dfd51-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="dfd51-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="dfd51-112">無。</span><span class="sxs-lookup"><span data-stu-id="dfd51-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="dfd51-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="dfd51-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dfd51-114">子元素</span><span class="sxs-lookup"><span data-stu-id="dfd51-114">Child Element</span></span></th>
<th><span data-ttu-id="dfd51-115">Description</span><span class="sxs-lookup"><span data-stu-id="dfd51-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfd51-116"><a href="element-1-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-116"><a href="element-1-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="dfd51-117">指定是否以系統管理員的方式啟用設定檔。這是 v4 的新元素。</span><span class="sxs-lookup"><span data-stu-id="dfd51-117">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfd51-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-118"><a href="element-1-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="dfd51-119">指定設定檔是否為系統管理漫遊控制。</span><span class="sxs-lookup"><span data-stu-id="dfd51-119">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="dfd51-120">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="dfd51-120">This element is new for v4.</span></span> <span data-ttu-id="dfd51-121">這個元素的值是 <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="dfd51-121">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="dfd51-122">這是選擇性元素;如果未指定任何值，則 <strong>AllRoamAllowed</strong> 為預設值。</span><span class="sxs-lookup"><span data-stu-id="dfd51-122">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfd51-123"><a href="element-1-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-123"><a href="element-1-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="dfd51-124">與此設定檔相關聯的 APN 識別碼。此元素是 v4 中的新元素，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="dfd51-124">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfd51-125"><a href="element-1-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-125"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="dfd51-126">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="dfd51-126">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfd51-127"><a href="element-1-name.md">名稱</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-127"><a href="element-1-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="dfd51-128">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="dfd51-128">The name of the profile.</span></span> <span data-ttu-id="dfd51-129">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>名稱</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-129">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfd51-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-130"><a href="element-oemconnectionid.md">OemConnectionId</a></span></span></td>
<td><p><span data-ttu-id="dfd51-131">數據機 DM 設定的 OEM 連接識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfd51-131">The OEM connection ID for the modem DM configuration.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfd51-132"><a href="element-1-profilecreationtype.md">ModemDMConfigProfile 中的 ProfileCreationType () </a></span><span class="sxs-lookup"><span data-stu-id="dfd51-132"><a href="element-1-profilecreationtype.md">ProfileCreationType (in ModemDMConfigProfile)</a></span></span></td>
<td><p><span data-ttu-id="dfd51-133">指定此數據機 DM 設定檔的建立方式。</span><span class="sxs-lookup"><span data-stu-id="dfd51-133">Specifies how this modem DM profile was created.</span></span></p>
<p><span data-ttu-id="dfd51-134">這個值是用來決定使用者是否可以刪除設定檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-134">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="dfd51-135">使用者只能刪除 <strong>UserProvisioned</strong> 設定檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-135">Users can only delete <strong>UserProvisioned</strong> profiles.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfd51-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-136"><a href="element-1-roamapplicability.md">RoamApplicability</a></span></span></td>
<td><p><span data-ttu-id="dfd51-137">指定只有在目前的漫遊條件是指定的漫遊條件時，才會使用此設定檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-137">Specifies that this profile is active only when the current roaming condition is the one specified.</span></span> <span data-ttu-id="dfd51-138">否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="dfd51-138">Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="dfd51-139">這個元素的值必須是有效的 <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="dfd51-139">The value of this element must be a valid <a href="simpletype-roamapplicabilitytype.md"><strong>roamApplicabilityType</strong></a> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfd51-140"><a href="element-1-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="dfd51-140"><a href="element-1-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="dfd51-141">適用于 GSM 裝置的 SIM Identifcation 號碼。</span><span class="sxs-lookup"><span data-stu-id="dfd51-141">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="dfd51-142">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="dfd51-142">For more details , see the documentation for the v1 <a href="../mbn/schema-simiccid-mbnprofile-element.md"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="dfd51-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="dfd51-143"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="dfd51-144">這個最外層的 (檔) 元素可能不會包含在任何其他專案中。</span><span class="sxs-lookup"><span data-stu-id="dfd51-144">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfd51-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfd51-145">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfd51-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfd51-146">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 




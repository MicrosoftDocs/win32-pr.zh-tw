---
description: MBNProfileExt
MS-HAID: WWAN\_profile\_v4.element\_MBNProfileExt
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: MBNProfileExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f84d56ba74325b6c65fb5c06ba2db9228c78d30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318488"
---
# <a name="span-idwwan_profile_v4element_mbnprofileextspanmbnprofileext"></a><span data-ttu-id="a3f5b-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span><span class="sxs-lookup"><span data-stu-id="a3f5b-103"><span id="WWAN_profile_v4.element_MBNProfileExt"></span>MBNProfileExt</span></span>

<span data-ttu-id="a3f5b-104">**MBNProfileExt** 元素是先前 MBNProfile 專案的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-104">The **MBNProfileExt** element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="a3f5b-105">它會以比 MBNProfile 元素更豐富的選項組來識別行動寬頻設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-105">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span>

<span data-ttu-id="a3f5b-106">設定檔中可以有一個以上的 MbnProfileExt 元素，描述一組特定作業條件的設定檔設定。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-106">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="a3f5b-107">使用 **MBNProfileExt** 的 [**ProfileConditionedOn**](element-profileconditionedon.md)子項目，以指定哪些作業條件會將特定的設定檔設為使用中的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-107">Use the [**ProfileConditionedOn**](element-profileconditionedon.md) child element of **MBNProfileExt** to specify which operating conditions make a particular profile the active profile.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a3f5b-108">元素階層</span><span class="sxs-lookup"><span data-stu-id="a3f5b-108">Element hierarchy</span></span>

**<MBNProfileExt>**

## <a name="syntax"></a><span data-ttu-id="a3f5b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3f5b-109">Syntax</span></span>

``` syntax
<MBNProfileExt>

  <!-- Child elements -->
  Name,
  Description?,
  ICONFilePath?,
  IsDefault,
  ProfileCreationType?,
  SubscriberID?,
  SimIccID,
  HomeProviderName?,
  AutoConnectOnInternet?,
  ConnectionMode?,
  Context?,
  DataRoamingPartners?,
  PurposeGroups?,
  ProfileConditionedOn?,
  IsProvisioningProfile?,
  ApnID?,
  AdminEnable?,
  AdminRoamControl?,
  IsExclusiveToOther?,
  IsLongStandingAdditionalPdpContextProfile?,
  MmsConfiguration?,
  any element in a non-schema namespace*

</MBNProfileExt>
```

### <a name="key"></a><span data-ttu-id="a3f5b-110">答案</span><span class="sxs-lookup"><span data-stu-id="a3f5b-110">Key</span></span>

<span data-ttu-id="a3f5b-111">`?`   選擇性 (零或一) </span><span class="sxs-lookup"><span data-stu-id="a3f5b-111">`?`   optional (zero or one)</span></span>

<span data-ttu-id="a3f5b-112">`*`   選擇性 (零或多個) </span><span class="sxs-lookup"><span data-stu-id="a3f5b-112">`*`   optional (zero or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a3f5b-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>屬性和元素</span><span class="sxs-lookup"><span data-stu-id="a3f5b-113"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a3f5b-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="a3f5b-114"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a3f5b-115">無。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-115">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a3f5b-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>子項目</span><span class="sxs-lookup"><span data-stu-id="a3f5b-116"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3f5b-117">子元素</span><span class="sxs-lookup"><span data-stu-id="a3f5b-117">Child Element</span></span></th>
<th><span data-ttu-id="a3f5b-118">Description</span><span class="sxs-lookup"><span data-stu-id="a3f5b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3f5b-119"><a href="element-adminenable.md">AdminEnable</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-119"><a href="element-adminenable.md">AdminEnable</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-120">指定是否以系統管理員的方式啟用設定檔。這是 v4 的新元素。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-120">Specifies whether the profile is enabled administratively.This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-121"><a href="element-adminroamcontrol.md">AdminRoamControl</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-122">指定設定檔是否為系統管理漫遊控制。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-122">Specifies whether the profile is administratively roam controlled.</span></span> <span data-ttu-id="a3f5b-123">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-123">This element is new for v4.</span></span> <span data-ttu-id="a3f5b-124">這個元素的值是 <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> 值。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-124">The value of this element is a <a href="simpletype-roamcontroltype.md"><strong>roamControlType</strong></a> value.</span></span> <span data-ttu-id="a3f5b-125">這是選擇性元素;如果未指定任何值，則 <strong>AllRoamAllowed</strong> 為預設值。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-125">This is an optional element; if no value is specified, then <strong>AllRoamAllowed</strong> is the default.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-126"><a href="element-apnid.md">ApnID</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-126"><a href="element-apnid.md">ApnID</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-127">與此設定檔相關聯的 APN 識別碼。此元素是 v4 中的新元素，而且是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-127">An APN ID associated with this profile.This element is new in v4, and it is optional.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-128"><a href="element-autoconnectoninternet.md">AutoConnectOnInternet</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-129">指定行動寬頻裝置是否會自動連接到網路。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-129">Specifies whether the Mobile Broadband device will automatically connect to a network.</span></span></p>
<p><span data-ttu-id="a3f5b-130">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-130">For more information, see the documentation for the v1 <a href="../mbn/schema-autoconnectoninternet-mbnprofile-element.md"><strong>AutoConnectOnInternet</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-131"><a href="element-connectionmode.md">ConnectionMode</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-131"><a href="element-connectionmode.md">ConnectionMode</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-132">指定要用於行動寬頻裝置的自動連線設定。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-132">Specifies the auto connection setting to be used for a Mobile Broadband device.</span></span></p>
<p><span data-ttu-id="a3f5b-133">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-133">For more information, see the documentation for the v1 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-134"><a href="element-context.md">內容</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-134"><a href="element-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-135">指定建立資料連線所需的參數。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-135">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-136"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-137">指定漫遊時的慣用網路提供者清單。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-137">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="a3f5b-138">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-138">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-139"><a href="element-description.md">說明</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-139"><a href="element-description.md">Description</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-140">設定檔的描述。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-140">A description of the profile.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-141"><a href="element-homeprovidername.md">HomeProviderName</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-141"><a href="element-homeprovidername.md">HomeProviderName</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-142">給定 SIM/裝置的家用提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-142">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="a3f5b-143">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-143">For more information, see the documentation for the v1 <a href="../mbn/schema-homeprovidername-mbnprofile-element.md"><strong>HomeProviderName</strong></a> element.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-144"><a href="element-iconfilepath.md">ICONFilePath</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-144"><a href="element-iconfilepath.md">ICONFilePath</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-145">連接的圖示檔路徑。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-145">The path to the icon file for the connection.</span></span> <span data-ttu-id="a3f5b-146">當使用此設定檔建立連接時，作業系統連接使用者介面會顯示圖示。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-146">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span></p>
<p><span data-ttu-id="a3f5b-147">如需使用此元素的詳細資訊，請參閱 <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>的 v1 檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-147">For more details on using this element, see the v1 documentation for <a href="../mbn/schema-iconfilepath-mbnprofile-element.md"><strong>ICONFilePath</strong></a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-148"><a href="element-isdefault.md">IsDefault</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-148"><a href="element-isdefault.md">IsDefault</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-149">指定此設定檔是否為預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-149">Specifies whether this profile is the default profile.</span></span></p>
<p><span data-ttu-id="a3f5b-150">如需此專案的詳細資訊，請參閱 <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>的 v1 檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-150">For more detail on this element, see the v1 documentation for <a href="../mbn/schema-isdefault-mbnprofile-element.md"><strong>IsDefault</strong></a>.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-151"><a href="element-isexclusivetoother.md">IsExclusiveToOther</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-152">指定此設定檔對於相同設定檔集 (s) 的其他設定檔是專屬的。此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-152">Specifies that this profile is exclusive to other profiles of the same profile set(s).This element is new for v4.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpCoNtextProfile</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-153"><a href="element-islongstandingadditionalpdpcontextprofile.md">IsLongStandingAdditionalPdpContextProfile</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-154">指定此設定檔為長期額外的 PDP 內容設定檔。如果這個元素的值是 <strong>true</strong>，則 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 也必須設定為 <strong>true</strong>。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-154">Specifies that this profile is a long-standing additional PDP context profile.If the value of this element is <strong>true</strong>, then <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must also be set to <strong>true</strong>.</span></span> <span data-ttu-id="a3f5b-155">這是 v4 的新元素。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-155">This is a new element for v4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-156"><a href="element-isprovisioningprofile.md">IsProvisioningProfile</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-157">指定此設定檔僅用於布建。否則，此設定檔並不適用，也無法用來啟用 (PDP) 內容的封包資料通訊協定。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-157">Specifies that this profile is to be used for provisioning only.Otherwise, the profile is not applicable, and cannot be used to activate a Packet Data Protocol (PDP) context.</span></span> <span data-ttu-id="a3f5b-158">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-158">This element is new for v4.</span></span></p>
<p><span data-ttu-id="a3f5b-159">如果 <strong>IsProvisioningProfile</strong> 為 True， <a href="element-isdefault.md"><strong>IsDefault</strong></a> 必須為 false，而且 <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> 必須是手動。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-159">If <strong>IsProvisioningProfile</strong> is true, <a href="element-isdefault.md"><strong>IsDefault</strong></a> must be false, and <a href="element-connectionmode.md"><strong>ConnectionMode</strong></a> must be manual.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-160"><a href="element-mmsconfiguration.md">MmsConfiguration</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-161">多媒體訊息服務 (MMS) 的設定資訊。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-161">Configuration information for Multimedia Messaging Service (MMS).</span></span></p>
<p><span data-ttu-id="a3f5b-162">除了設定此元素內的設定元素之外，MMS 設定檔也必須具有下列設定。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-162">In addition to setting the configuration elements within this element, an MMS profile must have the following settings.</span></span></p>
<ul>
<li><span data-ttu-id="a3f5b-163">其 <a href="element-name.md"><strong>Name</strong></a> 元素必須包含全系統的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-163">Its <a href="element-name.md"><strong>Name</strong></a> element must contain a system-wide unique name.</span></span></li>
<li><span data-ttu-id="a3f5b-164">其 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 必須設定為 <strong>UserProvisioned</strong>。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-164">Its <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> must be set to <strong>UserProvisioned</strong>.</span></span></li>
<li><span data-ttu-id="a3f5b-165">其 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 必須包含此設定檔所適用之 SIM 的 ICCID。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-165">Its <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> must contain the ICCID of the SIM that this profile is intended for.</span></span></li>
<li><span data-ttu-id="a3f5b-166">其 <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> 必須設定為 <strong>手動</strong>。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-166">Its <a href="../mbn/schema-connectionmode-mbnprofile-element.md"><strong>ConnectionMode</strong></a> must be set to <strong>Manual</strong>.</span></span></li>
<li><span data-ttu-id="a3f5b-167">其 <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> 必須包含 MMS 用途群組的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-167">Its <a href="element-purposegroupguid.md"><strong>PurposeGroupGuid</strong></a> must contain the GUID for MMS purpose group.</span></span></li>
<li><span data-ttu-id="a3f5b-168">其 <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpCoNtextProfile</strong></a> 必須設定為 <strong>true</strong>。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-168">Its <a href="/previous-versions/windows/desktop/legacy/mt156987(v=vs.85)"><strong>IsAdditionalPdpContextProfile</strong></a> must be set to <strong>true</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-169"><a href="element-name.md">名稱</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-169"><a href="element-name.md">Name</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-170">設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-170">The name of the profile.</span></span> <span data-ttu-id="a3f5b-171">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>名稱</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-171">For more information, see the documentation for the v1 <a href="../mbn/schema-name-mbnprofile-element.md"><strong>Name</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-172"><a href="element-profileconditionedon.md">ProfileConditionedOn</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-173">指定必須滿足的條件，設定檔才適用。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-173">Specifies the conditions which must be satisfied for a profile to be applicable.</span></span></p>
<p><span data-ttu-id="a3f5b-174">此元素是 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-174">This element is new for v4.</span></span> <span data-ttu-id="a3f5b-175">它可讓您指定在不同條件下套用的多個設定檔，並在適用時自動使用適當的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-175">It enables you to specify multiple profiles that apply in different conditions, and for the proper profile to be used automatically when it is applicable.</span></span> <span data-ttu-id="a3f5b-176">這是選擇性的項目。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-176">This element is optional.</span></span> <span data-ttu-id="a3f5b-177">如果您未指定，則設定檔一律適用于所列出的條件。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-177">If you do not specify it, then the profile is always applicable with respect to the conditions listed.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-178"><a href="element-profilecreationtype.md">MBNProfileExt 中的 ProfileCreationType () </a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-178"><a href="element-profilecreationtype.md">ProfileCreationType (in MBNProfileExt)</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-179">指定設定檔的建立者。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-179">Specifies the creator of the profile.</span></span></p>
<p><span data-ttu-id="a3f5b-180">如需此元素的詳細資訊，請參閱 v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-180">For more information about this element, see the documentation for the v1 <a href="../mbn/schema-profilecreationtype-mbnprofile-element.md"><strong>ProfileCreationType</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-181"><a href="element-purposegroups.md">PurposeGroups</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-181"><a href="element-purposegroups.md">PurposeGroups</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-182">選用的設定檔群組清單，其中每個群組都包含用於一般用途的設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-182">An optional list of groups of profiles, where each group includes profiles used for a common purpose.</span></span></p>
<p><span data-ttu-id="a3f5b-183">此元素是架構 v4 的新專案。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-183">This element is new for v4 of the schema.</span></span></p>
<p><span data-ttu-id="a3f5b-184">一個設定檔可以列在多個群組中。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-184">One profile can be listed in multiple groups.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a3f5b-185"><a href="element-simiccid.md">SimIccID</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-185"><a href="element-simiccid.md">SimIccID</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-186">適用于 GSM 裝置的 SIM Identifcation 號碼。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-186">The SIM Identifcation number for GSM devices.</span></span> <span data-ttu-id="a3f5b-187">如需詳細資訊，請參閱 v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-187">For more details , see the documentation for the v1 <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnsubscriberinformation-get_simiccid"><strong>SimIccID</strong></a> element.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a3f5b-188"><a href="element-subscriberid.md">SubscriberID</a></span><span class="sxs-lookup"><span data-stu-id="a3f5b-188"><a href="element-subscriberid.md">SubscriberID</a></span></span></td>
<td><p><span data-ttu-id="a3f5b-189">識別設定檔的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-189">Identifies the unique identifier of the profile.</span></span></p>
<p><span data-ttu-id="a3f5b-190">若為 GSM 網路，這應該包含 SIM 的 IMSI (國際行動使用者身分識別) ，而針對 CDMA 裝置，則應該包含裝置的最小 (行動電話識別碼) 。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-190">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span></p>
<p><span data-ttu-id="a3f5b-191">如需詳細資訊，請參閱 v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> 元素的檔。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-191">For more information, see the documentation for the v1 <a href="../mbn/schema-subscriberid-mbnprofile-element.md"><strong>SubscriberID</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a3f5b-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>父元素</span><span class="sxs-lookup"><span data-stu-id="a3f5b-192"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="a3f5b-193">這個最外層的 (檔) 元素可能不會包含在任何其他專案中。</span><span class="sxs-lookup"><span data-stu-id="a3f5b-193">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3f5b-194">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3f5b-194">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3f5b-195">命名空間</span><span class="sxs-lookup"><span data-stu-id="a3f5b-195">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 

---
description: 描述一組具有必要屬性和方法的類別，這些類別具有必要的屬性和方法，需要用來管理真實世界的實體，或以互通的方式支援使用案例。
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026815"
---
# <a name="msvm_registeredprofile-class"></a><span data-ttu-id="0e9af-103">Msvm \_ RegisteredProfile 類別</span><span class="sxs-lookup"><span data-stu-id="0e9af-103">Msvm\_RegisteredProfile class</span></span>

<span data-ttu-id="0e9af-104">描述一組具有必要屬性和方法的類別，這些類別具有必要的屬性和方法，需要用來管理真實世界的實體，或以互通的方式支援使用案例。</span><span class="sxs-lookup"><span data-stu-id="0e9af-104">Describes a set of classes with required properties and methods, necessary to manage a real-world entity or to support a usage scenario, in an interoperable fashion.</span></span>

<span data-ttu-id="0e9af-105">下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="0e9af-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9af-106">語法</span><span class="sxs-lookup"><span data-stu-id="0e9af-106">Syntax</span></span>

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="0e9af-107">成員</span><span class="sxs-lookup"><span data-stu-id="0e9af-107">Members</span></span>

<span data-ttu-id="0e9af-108">**Msvm \_ RegisteredProfile** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0e9af-108">The **Msvm\_RegisteredProfile** class has these types of members:</span></span>

-   [<span data-ttu-id="0e9af-109">屬性</span><span class="sxs-lookup"><span data-stu-id="0e9af-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0e9af-110">屬性</span><span class="sxs-lookup"><span data-stu-id="0e9af-110">Properties</span></span>

<span data-ttu-id="0e9af-111">**Msvm \_ RegisteredProfile** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0e9af-111">The **Msvm\_RegisteredProfile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0e9af-112">**AdvertiseTypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="0e9af-112">**AdvertiseTypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-113">資料類型： **字串** 陣列</span><span class="sxs-lookup"><span data-stu-id="0e9af-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-114">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-115">提供與 **AdvertiseType** 屬性相關之其他資訊的字串陣列。</span><span class="sxs-lookup"><span data-stu-id="0e9af-115">An array of strings that provides additional information related to the **AdvertiseType** property.</span></span> <span data-ttu-id="0e9af-116">當 **AdvertiseType** 是 1 (其他) 時，必須提供描述。</span><span class="sxs-lookup"><span data-stu-id="0e9af-116">A description must be provided when the **AdvertiseType** is 1 (Other).</span></span> <span data-ttu-id="0e9af-117">這個陣列中的專案會對應至 **AdvertiseTypes** 陣列中的相同索引。</span><span class="sxs-lookup"><span data-stu-id="0e9af-117">An entry in this array corresponds to the same index in the **AdvertiseTypes** array.</span></span> <span data-ttu-id="0e9af-118">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-118">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-119">**AdvertiseTypes**</span><span class="sxs-lookup"><span data-stu-id="0e9af-119">**AdvertiseTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-120">資料類型： **uint16** 陣列</span><span class="sxs-lookup"><span data-stu-id="0e9af-120">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-121">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-122">指定設定檔資訊的公告。</span><span class="sxs-lookup"><span data-stu-id="0e9af-122">Specifies the advertisement for the profile information.</span></span> <span data-ttu-id="0e9af-123">WBEM 基礎結構的廣告服務會使用它，透過哪些機制來判斷應公告的內容。</span><span class="sxs-lookup"><span data-stu-id="0e9af-123">It is used by the advertising services of the WBEM infrastructure to determine what should be advertised, through what mechanisms.</span></span> <span data-ttu-id="0e9af-124">屬性是陣列，因此可以使用數種機制來公告設定檔。</span><span class="sxs-lookup"><span data-stu-id="0e9af-124">The property is an array so that the profile can be advertised using several mechanisms.</span></span> <span data-ttu-id="0e9af-125">如果此屬性為 **Null**，這就相當於指定值 2 (不會) 公告。</span><span class="sxs-lookup"><span data-stu-id="0e9af-125">If this property is **Null**, this is equivalent to specifying the value 2 (Not Advertised).</span></span> <span data-ttu-id="0e9af-126">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-126">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0e9af-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0e9af-127"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**未公告** (2) </span><span class="sxs-lookup"><span data-stu-id="0e9af-128"><span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Not Advertised** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 ) </span><span class="sxs-lookup"><span data-stu-id="0e9af-129"><span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e9af-130">**標題**</span><span class="sxs-lookup"><span data-stu-id="0e9af-130">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-131">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-133">物件的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="0e9af-133">A short description of the object.</span></span> <span data-ttu-id="0e9af-134">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0e9af-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-135">**說明**</span><span class="sxs-lookup"><span data-stu-id="0e9af-135">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-136">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-137">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-138">對物件的描述。</span><span class="sxs-lookup"><span data-stu-id="0e9af-138">A description of the object.</span></span> <span data-ttu-id="0e9af-139">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0e9af-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0e9af-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-143">物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="0e9af-143">A display name for the object.</span></span> <span data-ttu-id="0e9af-144">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0e9af-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0e9af-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-146">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-147">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-148">限定詞：索引 **鍵**、覆 **寫**</span><span class="sxs-lookup"><span data-stu-id="0e9af-148">Qualifiers: **Key**, **Override**</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-149">可唯一識別這個類別之實例的字串。</span><span class="sxs-lookup"><span data-stu-id="0e9af-149">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0e9af-150">這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。</span><span class="sxs-lookup"><span data-stu-id="0e9af-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-151">**OtherRegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="0e9af-151">**OtherRegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-152">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-153">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-154">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="0e9af-154">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-155">當 **RegisteredOrganization** 包含 1 (其他) 時，提供組織描述的字串。</span><span class="sxs-lookup"><span data-stu-id="0e9af-155">A string that provides a description of the organization when **RegisteredOrganization** contains 1 (Other).</span></span> <span data-ttu-id="0e9af-156">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-156">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-157">**RegisteredName**</span><span class="sxs-lookup"><span data-stu-id="0e9af-157">**RegisteredName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-158">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-159">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-160">限定詞： **MaxLen** ( 256 ) </span><span class="sxs-lookup"><span data-stu-id="0e9af-160">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-161">這個已註冊設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e9af-161">The name of this registered profile.</span></span> <span data-ttu-id="0e9af-162">由於相同 **RegisteredName** 可以有多個版本， **RegisteredName**、 **RegisteredOrganization** 和 **RegisteredVersion** 的組合必須在組織範圍內唯一識別已註冊的設定檔。</span><span class="sxs-lookup"><span data-stu-id="0e9af-162">Since multiple versions can exist for the same **RegisteredName**, the combination of **RegisteredName**, **RegisteredOrganization**, and **RegisteredVersion** must uniquely identify the registered profile within the scope of the organization.</span></span> <span data-ttu-id="0e9af-163">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-163">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0e9af-164">**RegisteredOrganization**</span><span class="sxs-lookup"><span data-stu-id="0e9af-164">**RegisteredOrganization**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-165">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="0e9af-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-166">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-167">定義此設定檔的組織。</span><span class="sxs-lookup"><span data-stu-id="0e9af-167">The organization that defines this profile.</span></span> <span data-ttu-id="0e9af-168">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-168">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="0e9af-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="0e9af-169"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2) </span><span class="sxs-lookup"><span data-stu-id="0e9af-170"><span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3) </span><span class="sxs-lookup"><span data-stu-id="0e9af-171"><span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**服務創新的聯盟** (4) </span><span class="sxs-lookup"><span data-stu-id="0e9af-172"><span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5) </span><span class="sxs-lookup"><span data-stu-id="0e9af-173"><span id="FAST"></span><span id="fast"></span>**FAST** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6) </span><span class="sxs-lookup"><span data-stu-id="0e9af-174"><span id="GGF"></span><span id="ggf"></span>**GGF** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7) </span><span class="sxs-lookup"><span data-stu-id="0e9af-175"><span id="INTAP"></span><span id="intap"></span>**INTAP** (7)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8) </span><span class="sxs-lookup"><span data-stu-id="0e9af-176"><span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9) </span><span class="sxs-lookup"><span data-stu-id="0e9af-177"><span id="NAC"></span><span id="nac"></span>**NAC** (9)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10 名西北部能源效率聯盟** (10) </span><span class="sxs-lookup"><span data-stu-id="0e9af-178"><span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11) </span><span class="sxs-lookup"><span data-stu-id="0e9af-179"><span id="SNIA"></span><span id="snia"></span>**SNIA** (11)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM 論壇** (12) </span><span class="sxs-lookup"><span data-stu-id="0e9af-180"><span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM Forum** (12)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**開啟的群組** (13) </span><span class="sxs-lookup"><span data-stu-id="0e9af-181"><span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14) </span><span class="sxs-lookup"><span data-stu-id="0e9af-182"><span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15) </span><span class="sxs-lookup"><span data-stu-id="0e9af-183"><span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16) </span><span class="sxs-lookup"><span data-stu-id="0e9af-184"><span id="IETF"></span><span id="ietf"></span>**IETF** (16)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17) </span><span class="sxs-lookup"><span data-stu-id="0e9af-185"><span id="INCITS"></span><span id="incits"></span>**INCITS** (17)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18) </span><span class="sxs-lookup"><span data-stu-id="0e9af-186"><span id="ISO"></span><span id="iso"></span>**ISO** (18)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19) </span><span class="sxs-lookup"><span data-stu-id="0e9af-187"><span id="W3C"></span><span id="w3c"></span>**W3C** (19)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** (20) </span><span class="sxs-lookup"><span data-stu-id="0e9af-188"><span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**綠色方格** (21) </span><span class="sxs-lookup"><span data-stu-id="0e9af-189"><span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**The Green Grid** (21)</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。</span><span class="sxs-lookup"><span data-stu-id="0e9af-190"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="0e9af-191">)</span><span class="sxs-lookup"><span data-stu-id="0e9af-191">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0e9af-192">**RegisteredVersion**</span><span class="sxs-lookup"><span data-stu-id="0e9af-192">**RegisteredVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0e9af-193">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0e9af-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0e9af-194">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="0e9af-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0e9af-195">此設定檔的版本。</span><span class="sxs-lookup"><span data-stu-id="0e9af-195">The version of this profile.</span></span> <span data-ttu-id="0e9af-196">字串的格式必須為： "*M*。*N*。*U*"Where：</span><span class="sxs-lookup"><span data-stu-id="0e9af-196">The string must be in the form: "*M*.*N*.*U*" Where:</span></span>

-   <span data-ttu-id="0e9af-197">*M* 是以數值形式 (的主要版本，) 描述設定檔的建立或上次修改。</span><span class="sxs-lookup"><span data-stu-id="0e9af-197">*M* is the major version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="0e9af-198">*N* 是以數值形式 (的次要版本，) 描述設定檔的建立或上次修改。</span><span class="sxs-lookup"><span data-stu-id="0e9af-198">*N* is the minor version (in numeric form) describing the profile's creation or last modification.</span></span>
-   <span data-ttu-id="0e9af-199">*U* 是以數值形式 (的更新，) 描述設定檔的建立或上次修改。</span><span class="sxs-lookup"><span data-stu-id="0e9af-199">*U* is the update (in numeric form) describing the profile's creation or last modification.</span></span>

<span data-ttu-id="0e9af-200">這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="0e9af-200">This property is inherited from [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e9af-201">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e9af-201">Requirements</span></span>



| <span data-ttu-id="0e9af-202">需求</span><span class="sxs-lookup"><span data-stu-id="0e9af-202">Requirement</span></span> | <span data-ttu-id="0e9af-203">值</span><span class="sxs-lookup"><span data-stu-id="0e9af-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e9af-204">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0e9af-204">Minimum supported client</span></span><br/> | <span data-ttu-id="0e9af-205">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9af-205">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="0e9af-206">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0e9af-206">Minimum supported server</span></span><br/> | <span data-ttu-id="0e9af-207">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0e9af-207">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0e9af-208">命名空間</span><span class="sxs-lookup"><span data-stu-id="0e9af-208">Namespace</span></span><br/>                | <span data-ttu-id="0e9af-209">根 \\ interop</span><span class="sxs-lookup"><span data-stu-id="0e9af-209">Root\\interop</span></span><br/>                                                                                |
| <span data-ttu-id="0e9af-210">MOF</span><span class="sxs-lookup"><span data-stu-id="0e9af-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e9af-211"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0e9af-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e9af-212">DLL</span><span class="sxs-lookup"><span data-stu-id="0e9af-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e9af-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0e9af-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



 


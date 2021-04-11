---
title: MDM_Policy_Config01_Privacy02 類別
description: MDM \_ Policy \_ Config01 \_ Privacy02 類別代表可用的搜尋原則。
ms.assetid: 202213b9-5301-4c55-bbc6-6ce3daf705ad
keywords:
- MDM_Policy_Config01_Privacy02 類別
- MDM_Policy_Config01_Privacy02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Privacy02
- MDM_Policy_Config01_Privacy02.InstanceID
- MDM_Policy_Config01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca714dc17db60982e5ba047690886bc88aa79853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934355"
---
# <a name="mdm_policy_config01_privacy02-class"></a><span data-ttu-id="ac324-105">MDM \_ 原則 \_ Config01 \_ Privacy02 類別</span><span class="sxs-lookup"><span data-stu-id="ac324-105">MDM\_Policy\_Config01\_Privacy02 class</span></span>

<span data-ttu-id="ac324-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="ac324-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac324-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="ac324-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac324-108">**MDM \_ Policy \_ Config01 \_ Privacy02** 類別代表可用的搜尋原則。</span><span class="sxs-lookup"><span data-stu-id="ac324-108">The **MDM\_Policy\_Config01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="ac324-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="ac324-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac324-110">語法</span><span class="sxs-lookup"><span data-stu-id="ac324-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="ac324-111">成員</span><span class="sxs-lookup"><span data-stu-id="ac324-111">Members</span></span>

<span data-ttu-id="ac324-112">**MDM \_ Policy \_ Config01 \_ Privacy02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac324-112">The **MDM\_Policy\_Config01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac324-113">屬性</span><span class="sxs-lookup"><span data-stu-id="ac324-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac324-114">屬性</span><span class="sxs-lookup"><span data-stu-id="ac324-114">Properties</span></span>

<span data-ttu-id="ac324-115">**MDM \_ Policy \_ Config01 \_ Privacy02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="ac324-115">The **MDM\_Policy\_Config01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac324-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="ac324-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="ac324-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="ac324-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="ac324-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac324-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac324-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-129">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-130">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac324-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac324-131">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac324-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac324-132">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac324-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="ac324-133">此類別的字串為 "隱私權"。</span><span class="sxs-lookup"><span data-stu-id="ac324-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="ac324-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="ac324-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-137">LetAppsAccessAccountInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-140">LetAppsAccessAccountInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-143">LetAppsAccessAccountInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="ac324-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-149">LetAppsAccessCalendar \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-152">LetAppsAccessCalendar \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-155">LetAppsAccessCalendar \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="ac324-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-161">LetAppsAccessCallHistory \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-164">LetAppsAccessCallHistory \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-165">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-167">LetAppsAccessCallHistory \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="ac324-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-173">LetAppsAccessCamera \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-176">LetAppsAccessCamera \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-177">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-179">LetAppsAccessCamera \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="ac324-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-185">LetAppsAccessContacts \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-188">LetAppsAccessContacts \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-191">LetAppsAccessContacts \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="ac324-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-195">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-196">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-197">LetAppsAccessEmail \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-198">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-200">LetAppsAccessEmail \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-202">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-203">LetAppsAccessEmail \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-204">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-205">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="ac324-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-207">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-209">LetAppsAccessLocation \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-210">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-212">LetAppsAccessLocation \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-215">LetAppsAccessLocation \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-216">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="ac324-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-219">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-221">LetAppsAccessMessaging \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-222">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-224">LetAppsAccessMessaging \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-227">LetAppsAccessMessaging \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-228">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="ac324-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-231">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-233">LetAppsAccessMicrophone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-234">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-236">LetAppsAccessMicrophone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-237">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-239">LetAppsAccessMicrophone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-240">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="ac324-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-243">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-245">LetAppsAccessMotion \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-246">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-248">LetAppsAccessMotion \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-249">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-251">LetAppsAccessMotion \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-252">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="ac324-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-255">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-257">LetAppsAccessNotifications \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-258">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-260">LetAppsAccessNotifications \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-261">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-263">LetAppsAccessNotifications \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="ac324-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-267">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-269">LetAppsAccessPhone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-270">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-271">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-272">LetAppsAccessPhone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-273">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-274">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-275">LetAppsAccessPhone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-276">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-277">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="ac324-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-279">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-280">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-281">LetAppsAccessRadios \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-282">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-283">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-284">LetAppsAccessRadios \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-285">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-286">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-287">LetAppsAccessRadios \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-288">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-289">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="ac324-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-291">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-292">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-293">LetAppsAccessTasks \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-294">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-295">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-296">LetAppsAccessTasks \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-297">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-298">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-299">LetAppsAccessTasks \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-300">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-301">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="ac324-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-303">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-304">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-305">LetAppsAccessTrustedDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-306">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-307">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-308">LetAppsAccessTrustedDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-309">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-310">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-311">LetAppsAccessTrustedDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-312">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-313">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="ac324-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-315">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-316">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-317">LetAppsGetDiagnosticInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-318">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-319">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-320">LetAppsGetDiagnosticInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-321">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-322">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-323">LetAppsGetDiagnosticInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-324">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-325">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="ac324-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-327">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-328">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-329">LetAppsRunInBackground \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-330">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-331">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-332">LetAppsRunInBackground \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-333">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-334">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-335">LetAppsRunInBackground \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-336">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-337">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="ac324-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-339">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-340">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-341">LetAppsSyncWithDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-342">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-343">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-344">LetAppsSyncWithDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-345">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-346">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac324-347">LetAppsSyncWithDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="ac324-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-348">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-349">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac324-350">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac324-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-351">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac324-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-352">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="ac324-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac324-353">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac324-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ac324-354">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ac324-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="ac324-355">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="ac324-355">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="ac324-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="ac324-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac324-357">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="ac324-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ac324-358">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="ac324-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac324-359">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac324-359">Requirements</span></span>



| <span data-ttu-id="ac324-360">需求</span><span class="sxs-lookup"><span data-stu-id="ac324-360">Requirement</span></span> | <span data-ttu-id="ac324-361">值</span><span class="sxs-lookup"><span data-stu-id="ac324-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac324-362">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac324-362">Minimum supported client</span></span><br/> | <span data-ttu-id="ac324-363">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac324-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac324-364">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac324-364">Minimum supported server</span></span><br/> | <span data-ttu-id="ac324-365">都不支援</span><span class="sxs-lookup"><span data-stu-id="ac324-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac324-366">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac324-366">Namespace</span></span><br/>                | <span data-ttu-id="ac324-367">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="ac324-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac324-368">MOF</span><span class="sxs-lookup"><span data-stu-id="ac324-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac324-369"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac324-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac324-370">DLL</span><span class="sxs-lookup"><span data-stu-id="ac324-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac324-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac324-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac324-372">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac324-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac324-373">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="ac324-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


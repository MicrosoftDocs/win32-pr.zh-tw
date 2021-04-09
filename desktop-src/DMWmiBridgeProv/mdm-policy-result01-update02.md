---
title: MDM_Policy_Result01_Update02 類別
description: MDM \_ Policy \_ Result01 \_ Update02 類別代表可用的更新原則。
ms.assetid: 06604da6-5298-4273-a030-529491c2823c
keywords:
- MDM_Policy_Result01_Update02 類別
- MDM_Policy_Result01_Update02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Update02
- MDM_Policy_Result01_Update02.InstanceID
- MDM_Policy_Result01_Update02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0be844bb4ef8fc20e7ab5bbc8b7709cdfde4034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933952"
---
# <a name="mdm_policy_result01_update02-class"></a><span data-ttu-id="a357c-105">MDM \_ 原則 \_ Result01 \_ Update02 類別</span><span class="sxs-lookup"><span data-stu-id="a357c-105">MDM\_Policy\_Result01\_Update02 class</span></span>

<span data-ttu-id="a357c-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="a357c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a357c-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="a357c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a357c-108">**MDM \_ Policy \_ Result01 \_ Update02** 類別代表可用的更新原則。</span><span class="sxs-lookup"><span data-stu-id="a357c-108">The **MDM\_Policy\_Result01\_Update02** class represents the update policies available.</span></span>

<span data-ttu-id="a357c-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a357c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a357c-110">語法</span><span class="sxs-lookup"><span data-stu-id="a357c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Update02
{
  string InstanceID;
  string ParentID;
  sint32 RequireUpdateApproval;
  sint32 AllowAutoUpdate;
  sint32 AllowAutoWindowsUpdateDownloadOverMeteredNetwork;
  sint32 AllowMUUpdateService;
  sint32 ScheduledInstallDay;
  sint32 ScheduledInstallThirdWeek;
  sint32 ScheduledInstallSecondWeek;
  sint32 ScheduledInstallFourthWeek;
  sint32 ScheduledInstallFirstWeek;
  sint32 ScheduledInstallEveryWeek;
  sint32 ScheduledInstallTime;
  sint32 AllowUpdateService;
  sint32 DeferQualityUpdatesPeriodInDays;
  sint32 DeferFeatureUpdatesPeriodInDays;
  sint32 BranchReadinessLevel;
  string UpdateServiceUrl;
  sint32 SetEDURestart;
  sint32 AutoRestartDeadlinePeriodInDays;
  string UpdateServiceUrlAlternate;
  sint32 FillEmptyContentUrls;
  sint32 AllowNonMicrosoftSignedUpdate;
  sint32 RequireDeferUpgrade;
  sint32 PauseDeferrals;
  sint32 PauseQualityUpdates;
  sint32 PhoneUpdateRestrictions;
  string PauseQualityUpdatesStartTime;
  sint32 PauseFeatureUpdates;
  string PauseFeatureUpdatesStartTime;
  sint32 DeferUpgradePeriod;
  sint32 ExcludeWUDriversInQualityUpdate;
  sint32 IgnoreMOUpdateDownloadLimit;
  sint32 ManagePreviewBuilds;
  sint32 IgnoreMOAppDownloadLimit;
  sint32 DeferUpdatePeriod;
  sint32 ActiveHoursEnd;
  sint32 ActiveHoursStart;
  sint32 DetectionFrequency;
  sint32 DisableDualScan;
  sint32 EngagedRestartDeadline;
  sint32 EngagedRestartSnoozeSchedule;
  sint32 EngagedRestartTransitionSchedule;
  sint32 ScheduleImminentRestartWarning;
  sint32 ScheduleRestartWarning;
  sint32 SetAutoRestartNotificationDisable;
  sint32 AutoRestartNotificationSchedule;
  sint32 AutoRestartRequiredNotificationDismissal;
  sint32 ActiveHoursMaxRange;
};
```

## <a name="members"></a><span data-ttu-id="a357c-111">成員</span><span class="sxs-lookup"><span data-stu-id="a357c-111">Members</span></span>

<span data-ttu-id="a357c-112">**MDM \_ Policy \_ Result01 \_ Update02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a357c-112">The **MDM\_Policy\_Result01\_Update02** class has these types of members:</span></span>

-   [<span data-ttu-id="a357c-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a357c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a357c-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a357c-114">Properties</span></span>

<span data-ttu-id="a357c-115">**MDM \_ Policy \_ Result01 \_ Update02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a357c-115">The **MDM\_Policy\_Result01\_Update02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a357c-116">ActiveHoursEnd</span><span class="sxs-lookup"><span data-stu-id="a357c-116">ActiveHoursEnd</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursend)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-119">ActiveHoursMaxRange</span><span class="sxs-lookup"><span data-stu-id="a357c-119">ActiveHoursMaxRange</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursmaxrange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-122">ActiveHoursStart</span><span class="sxs-lookup"><span data-stu-id="a357c-122">ActiveHoursStart</span></span>](/windows/client-management/mdm/policy-csp-update#update-activehoursstart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-125">AllowAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="a357c-125">AllowAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span><span class="sxs-lookup"><span data-stu-id="a357c-128">AllowAutoWindowsUpdateDownloadOverMeteredNetwork</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowautowindowsupdatedownloadovermeterednetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-131">AllowMUUpdateService</span><span class="sxs-lookup"><span data-stu-id="a357c-131">AllowMUUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowmuupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-134">AllowNonMicrosoftSignedUpdate</span><span class="sxs-lookup"><span data-stu-id="a357c-134">AllowNonMicrosoftSignedUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-allownonmicrosoftsignedupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-137">AllowUpdateService</span><span class="sxs-lookup"><span data-stu-id="a357c-137">AllowUpdateService</span></span>](/windows/client-management/mdm/policy-csp-update#update-allowupdateservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-140">AutoRestartDeadlinePeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a357c-140">AutoRestartDeadlinePeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartdeadlineperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-143">AutoRestartNotificationSchedule</span><span class="sxs-lookup"><span data-stu-id="a357c-143">AutoRestartNotificationSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartnotificationschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-146">AutoRestartRequiredNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="a357c-146">AutoRestartRequiredNotificationDismissal</span></span>](/windows/client-management/mdm/policy-csp-update#update-autorestartrequirednotificationdismissal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-149">BranchReadinessLevel</span><span class="sxs-lookup"><span data-stu-id="a357c-149">BranchReadinessLevel</span></span>](/windows/client-management/mdm/policy-csp-update#update-branchreadinesslevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-152">DeferFeatureUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a357c-152">DeferFeatureUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferfeatureupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-155">DeferQualityUpdatesPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="a357c-155">DeferQualityUpdatesPeriodInDays</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferqualityupdatesperiodindays)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-158">DeferUpdatePeriod</span><span class="sxs-lookup"><span data-stu-id="a357c-158">DeferUpdatePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupdateperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-161">DeferUpgradePeriod</span><span class="sxs-lookup"><span data-stu-id="a357c-161">DeferUpgradePeriod</span></span>](/windows/client-management/mdm/policy-csp-update#update-deferupgradeperiod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-164">DetectionFrequency</span><span class="sxs-lookup"><span data-stu-id="a357c-164">DetectionFrequency</span></span>](/windows/client-management/mdm/policy-csp-update#update-detectionfrequency)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-167">DisableDualScan</span><span class="sxs-lookup"><span data-stu-id="a357c-167">DisableDualScan</span></span>](/windows/client-management/mdm/policy-csp-update#update-disabledualscan)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-170">EngagedRestartDeadline</span><span class="sxs-lookup"><span data-stu-id="a357c-170">EngagedRestartDeadline</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartdeadline)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-173">EngagedRestartSnoozeSchedule</span><span class="sxs-lookup"><span data-stu-id="a357c-173">EngagedRestartSnoozeSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestartsnoozeschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-174">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-176">EngagedRestartTransitionSchedule</span><span class="sxs-lookup"><span data-stu-id="a357c-176">EngagedRestartTransitionSchedule</span></span>](/windows/client-management/mdm/policy-csp-update#update-engagedrestarttransitionschedule)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-177">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-179">ExcludeWUDriversInQualityUpdate</span><span class="sxs-lookup"><span data-stu-id="a357c-179">ExcludeWUDriversInQualityUpdate</span></span>](/windows/client-management/mdm/policy-csp-update#update-excludewudriversinqualityupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-180">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-182">FillEmptyContentUrls</span><span class="sxs-lookup"><span data-stu-id="a357c-182">FillEmptyContentUrls</span></span>](/windows/client-management/mdm/policy-csp-update#update-fillemptycontenturls)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-185">IgnoreMOAppDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="a357c-185">IgnoreMOAppDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoappdownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-186">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-188">IgnoreMOUpdateDownloadLimit</span><span class="sxs-lookup"><span data-stu-id="a357c-188">IgnoreMOUpdateDownloadLimit</span></span>](/windows/client-management/mdm/policy-csp-update#update-ignoremoupdatedownloadlimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-189">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a357c-191">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a357c-191">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a357c-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a357c-194">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a357c-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a357c-195">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="a357c-195">Identifies the name of the parent node.</span></span> <span data-ttu-id="a357c-196">針對此類別，字串為 "Update"</span><span class="sxs-lookup"><span data-stu-id="a357c-196">For this class, the string is "Update"</span></span>

</dd> <dt>

[<span data-ttu-id="a357c-197">ManagePreviewBuilds</span><span class="sxs-lookup"><span data-stu-id="a357c-197">ManagePreviewBuilds</span></span>](/windows/client-management/mdm/policy-csp-update#update-managepreviewbuilds)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-198">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-199">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a357c-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a357c-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a357c-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a357c-203">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a357c-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a357c-204">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a357c-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="a357c-205">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="a357c-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="a357c-206">PauseDeferrals</span><span class="sxs-lookup"><span data-stu-id="a357c-206">PauseDeferrals</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausedeferrals)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-207">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-209">PauseFeatureUpdates</span><span class="sxs-lookup"><span data-stu-id="a357c-209">PauseFeatureUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-210">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-212">PauseFeatureUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="a357c-212">PauseFeatureUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausefeatureupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-213">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-215">PauseQualityUpdates</span><span class="sxs-lookup"><span data-stu-id="a357c-215">PauseQualityUpdates</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-216">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-218">PauseQualityUpdatesStartTime</span><span class="sxs-lookup"><span data-stu-id="a357c-218">PauseQualityUpdatesStartTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-pausequalityupdatesstarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-219">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-221">PhoneUpdateRestrictions</span><span class="sxs-lookup"><span data-stu-id="a357c-221">PhoneUpdateRestrictions</span></span>](/windows/client-management/mdm/policy-csp-update#update-phoneupdaterestrictions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-222">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-224">RequireDeferUpgrade</span><span class="sxs-lookup"><span data-stu-id="a357c-224">RequireDeferUpgrade</span></span>](/windows/client-management/mdm/policy-csp-update#update-requiredeferupgrade)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-225">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-227">RequireUpdateApproval</span><span class="sxs-lookup"><span data-stu-id="a357c-227">RequireUpdateApproval</span></span>](/windows/client-management/mdm/policy-csp-update#update-requireupdateapproval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-228">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-230">ScheduledInstallDay</span><span class="sxs-lookup"><span data-stu-id="a357c-230">ScheduledInstallDay</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-231">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-233">ScheduledInstallEveryWeek</span><span class="sxs-lookup"><span data-stu-id="a357c-233">ScheduledInstallEveryWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalleveryweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-234">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-234">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-235">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-236">ScheduledInstallFirstWeek</span><span class="sxs-lookup"><span data-stu-id="a357c-236">ScheduledInstallFirstWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfirstweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-237">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-237">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-238">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-239">ScheduledInstallFourthWeek</span><span class="sxs-lookup"><span data-stu-id="a357c-239">ScheduledInstallFourthWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallfourthweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-240">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-240">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-241">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-242">ScheduledInstallSecondWeek</span><span class="sxs-lookup"><span data-stu-id="a357c-242">ScheduledInstallSecondWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallsecondweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-243">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-244">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-245">ScheduledInstallThirdWeek</span><span class="sxs-lookup"><span data-stu-id="a357c-245">ScheduledInstallThirdWeek</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstallthirdweek)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-246">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-246">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-247">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-248">ScheduledInstallTime</span><span class="sxs-lookup"><span data-stu-id="a357c-248">ScheduledInstallTime</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduledinstalltime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-249">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-249">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-250">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-251">ScheduleImminentRestartWarning</span><span class="sxs-lookup"><span data-stu-id="a357c-251">ScheduleImminentRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-scheduleimminentrestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-252">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-252">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-253">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-254">ScheduleRestartWarning</span><span class="sxs-lookup"><span data-stu-id="a357c-254">ScheduleRestartWarning</span></span>](/windows/client-management/mdm/policy-csp-update#update-schedulerestartwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-255">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-256">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-257">SetAutoRestartNotificationDisable</span><span class="sxs-lookup"><span data-stu-id="a357c-257">SetAutoRestartNotificationDisable</span></span>](/windows/client-management/mdm/policy-csp-update#update-setautorestartnotificationdisable)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-258">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-258">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-259">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-260">SetEDURestart</span><span class="sxs-lookup"><span data-stu-id="a357c-260">SetEDURestart</span></span>](/windows/client-management/mdm/policy-csp-update#update-setedurestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-261">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="a357c-261">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-262">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-263">UpdateServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a357c-263">UpdateServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-264">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-265">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a357c-266">UpdateServiceUrlAlternate</span><span class="sxs-lookup"><span data-stu-id="a357c-266">UpdateServiceUrlAlternate</span></span>](/windows/client-management/mdm/policy-csp-update#update-updateserviceurlalternate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a357c-267">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a357c-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a357c-268">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a357c-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a357c-269">規格需求</span><span class="sxs-lookup"><span data-stu-id="a357c-269">Requirements</span></span>



| <span data-ttu-id="a357c-270">需求</span><span class="sxs-lookup"><span data-stu-id="a357c-270">Requirement</span></span> | <span data-ttu-id="a357c-271">值</span><span class="sxs-lookup"><span data-stu-id="a357c-271">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a357c-272">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a357c-272">Minimum supported client</span></span><br/> | <span data-ttu-id="a357c-273">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a357c-273">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a357c-274">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a357c-274">Minimum supported server</span></span><br/> | <span data-ttu-id="a357c-275">都不支援</span><span class="sxs-lookup"><span data-stu-id="a357c-275">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a357c-276">命名空間</span><span class="sxs-lookup"><span data-stu-id="a357c-276">Namespace</span></span><br/>                | <span data-ttu-id="a357c-277">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="a357c-277">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a357c-278">MOF</span><span class="sxs-lookup"><span data-stu-id="a357c-278">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a357c-279"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="a357c-279"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a357c-280">DLL</span><span class="sxs-lookup"><span data-stu-id="a357c-280">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a357c-281"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a357c-281"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a357c-282">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a357c-282">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a357c-283">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="a357c-283">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


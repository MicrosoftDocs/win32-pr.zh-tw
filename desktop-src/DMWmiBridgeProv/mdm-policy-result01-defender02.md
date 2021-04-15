---
title: MDM_Policy_Result01_Defender02 類別
description: '[MDM \_ 原則 \_ Result01] \_ Defender02class 代表與 Windows Defender 相關的原則。'
ms.assetid: 82c8a7a2-8369-46c4-aa87-b44b742a274d
keywords:
- MDM_Policy_Result01_Defender02 類別
- MDM_Policy_Result01_Defender02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Defender02
- MDM_Policy_Result01_Defender02.InstanceID
- MDM_Policy_Result01_Defender02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae898751a9f15af1c945efd3e6a473dfe07c7cd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464757"
---
# <a name="mdm_policy_result01_defender02-class"></a><span data-ttu-id="71d65-105">MDM \_ 原則 \_ Result01 \_ Defender02 類別</span><span class="sxs-lookup"><span data-stu-id="71d65-105">MDM\_Policy\_Result01\_Defender02 class</span></span>

<span data-ttu-id="71d65-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="71d65-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="71d65-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="71d65-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="71d65-108">**MDM \_ Policy \_ Result01 \_ Defender02** 類別代表與 Windows Defender 相關的原則</span><span class="sxs-lookup"><span data-stu-id="71d65-108">The **MDM\_Policy\_Result01\_Defender02** class represents policies related to Windows Defender</span></span>

<span data-ttu-id="71d65-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="71d65-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d65-110">語法</span><span class="sxs-lookup"><span data-stu-id="71d65-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Defender02
{
  string InstanceID;
  string ParentID;
  sint32 AllowArchiveScanning;
  sint32 AllowBehaviorMonitoring;
  sint32 AllowCloudProtection;
  sint32 AllowEmailScanning;
  sint32 AllowFullScanOnMappedNetworkDrives;
  sint32 AllowFullScanRemovableDriveScanning;
  sint32 AllowIntrusionPreventionSystem;
  sint32 AllowIOAVProtection;
  sint32 AllowOnAccessProtection;
  sint32 AllowRealtimeMonitoring;
  sint32 AllowScanningNetworkFiles;
  sint32 AllowScriptScanning;
  sint32 AllowUserUIAccess;
  string AttackSurfaceReductionRules;
  string AttackSurfaceReductionOnlyExclusions;
  sint32 AVGCPULoadFactor;
  sint32 CloudExtendedTimeout;
  string ControlledFolderAccessProtectedFolders;
  string ControlledFolderAccessAllowedApplications;
  sint32 CloudBlockLevel;
  sint32 DaysToRetainCleanedMalware;
  sint32 EnableControlledFolderAccess;
  sint32 EnableNetworkProtection;
  sint32 PUAProtection;
  string ExcludedProcesses;
  string ExcludedPaths;
  string ExcludedExtensions;
  sint32 RealTimeScanDirection;
  sint32 ScheduleQuickScanTime;
  sint32 ScheduleScanDay;
  sint32 ScheduleScanTime;
  sint32 SignatureUpdateInterval;
  sint32 SubmitSamplesConsent;
  string ThreatSeverityDefaultAction;
  sint32 ScanParameter;
};
```

## <a name="members"></a><span data-ttu-id="71d65-111">成員</span><span class="sxs-lookup"><span data-stu-id="71d65-111">Members</span></span>

<span data-ttu-id="71d65-112">**MDM \_ Policy \_ Result01 \_ Defender02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="71d65-112">The **MDM\_Policy\_Result01\_Defender02** class has these types of members:</span></span>

-   [<span data-ttu-id="71d65-113">屬性</span><span class="sxs-lookup"><span data-stu-id="71d65-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="71d65-114">屬性</span><span class="sxs-lookup"><span data-stu-id="71d65-114">Properties</span></span>

<span data-ttu-id="71d65-115">**MDM \_ Policy \_ Result01 \_ Defender02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="71d65-115">The **MDM\_Policy\_Result01\_Defender02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="71d65-116">AllowArchiveScanning</span><span class="sxs-lookup"><span data-stu-id="71d65-116">AllowArchiveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowarchivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-119">AllowBehaviorMonitoring</span><span class="sxs-lookup"><span data-stu-id="71d65-119">AllowBehaviorMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowbehaviormonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-122">AllowCloudProtection</span><span class="sxs-lookup"><span data-stu-id="71d65-122">AllowCloudProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowcloudprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-125">AllowEmailScanning</span><span class="sxs-lookup"><span data-stu-id="71d65-125">AllowEmailScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowemailscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-128">AllowFullScanOnMappedNetworkDrives</span><span class="sxs-lookup"><span data-stu-id="71d65-128">AllowFullScanOnMappedNetworkDrives</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanonmappednetworkdrives)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-131">AllowFullScanRemovableDriveScanning</span><span class="sxs-lookup"><span data-stu-id="71d65-131">AllowFullScanRemovableDriveScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowfullscanremovabledrivescanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-134">AllowIntrusionPreventionSystem</span><span class="sxs-lookup"><span data-stu-id="71d65-134">AllowIntrusionPreventionSystem</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowintrusionpreventionsystem)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-137">AllowIOAVProtection</span><span class="sxs-lookup"><span data-stu-id="71d65-137">AllowIOAVProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowioavprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-140">AllowOnAccessProtection</span><span class="sxs-lookup"><span data-stu-id="71d65-140">AllowOnAccessProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowonaccessprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-143">AllowRealtimeMonitoring</span><span class="sxs-lookup"><span data-stu-id="71d65-143">AllowRealtimeMonitoring</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowrealtimemonitoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-146">AllowScanningNetworkFiles</span><span class="sxs-lookup"><span data-stu-id="71d65-146">AllowScanningNetworkFiles</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscanningnetworkfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-149">AllowScriptScanning</span><span class="sxs-lookup"><span data-stu-id="71d65-149">AllowScriptScanning</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowscriptscanning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-152">AllowUserUIAccess</span><span class="sxs-lookup"><span data-stu-id="71d65-152">AllowUserUIAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-allowuseruiaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-155">AttackSurfaceReductionOnlyExclusions</span><span class="sxs-lookup"><span data-stu-id="71d65-155">AttackSurfaceReductionOnlyExclusions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductiononlyexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-156">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-158">AttackSurfaceReductionRules</span><span class="sxs-lookup"><span data-stu-id="71d65-158">AttackSurfaceReductionRules</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-attacksurfacereductionrules)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-159">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-161">AVGCPULoadFactor</span><span class="sxs-lookup"><span data-stu-id="71d65-161">AVGCPULoadFactor</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-avgcpuloadfactor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-164">CloudBlockLevel</span><span class="sxs-lookup"><span data-stu-id="71d65-164">CloudBlockLevel</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudblocklevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-167">CloudExtendedTimeout</span><span class="sxs-lookup"><span data-stu-id="71d65-167">CloudExtendedTimeout</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-cloudextendedtimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-170">ControlledFolderAccessAllowedApplications</span><span class="sxs-lookup"><span data-stu-id="71d65-170">ControlledFolderAccessAllowedApplications</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessallowedapplications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-171">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-173">ControlledFolderAccessProtectedFolders</span><span class="sxs-lookup"><span data-stu-id="71d65-173">ControlledFolderAccessProtectedFolders</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-controlledfolderaccessprotectedfolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-175">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-176">DaysToRetainCleanedMalware</span><span class="sxs-lookup"><span data-stu-id="71d65-176">DaysToRetainCleanedMalware</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-daystoretaincleanedmalware)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-177">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-178">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-179">EnableControlledFolderAccess</span><span class="sxs-lookup"><span data-stu-id="71d65-179">EnableControlledFolderAccess</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablecontrolledfolderaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-180">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-182">EnableNetworkProtection</span><span class="sxs-lookup"><span data-stu-id="71d65-182">EnableNetworkProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-enablenetworkprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-185">ExcludedExtensions</span><span class="sxs-lookup"><span data-stu-id="71d65-185">ExcludedExtensions</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-186">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-187">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-188">ExcludedPaths</span><span class="sxs-lookup"><span data-stu-id="71d65-188">ExcludedPaths</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-189">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-190">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-191">ExcludedProcesses</span><span class="sxs-lookup"><span data-stu-id="71d65-191">ExcludedProcesses</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-excludedprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-192">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-193">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="71d65-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="71d65-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-195">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-196">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71d65-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71d65-197">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71d65-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71d65-198">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="71d65-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="71d65-199">此類別的字串為 "Defender"。</span><span class="sxs-lookup"><span data-stu-id="71d65-199">For this class, the string is "Defender".</span></span>

</dd> <dt>

<span data-ttu-id="71d65-200">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="71d65-200">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-201">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-202">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="71d65-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="71d65-203">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="71d65-203">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="71d65-204">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="71d65-204">Describes the full path to the parent node.</span></span> <span data-ttu-id="71d65-205">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="71d65-205">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="71d65-206">PUAProtection</span><span class="sxs-lookup"><span data-stu-id="71d65-206">PUAProtection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-puaprotection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-207">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-208">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-209">RealTimeScanDirection</span><span class="sxs-lookup"><span data-stu-id="71d65-209">RealTimeScanDirection</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-realtimescandirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-210">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-211">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-212">ScanParameter</span><span class="sxs-lookup"><span data-stu-id="71d65-212">ScanParameter</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-scanparameter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-213">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-214">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-215">ScheduleQuickScanTime</span><span class="sxs-lookup"><span data-stu-id="71d65-215">ScheduleQuickScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulequickscantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-216">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-216">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-217">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-218">ScheduleScanDay</span><span class="sxs-lookup"><span data-stu-id="71d65-218">ScheduleScanDay</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescanday)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-219">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-220">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-221">ScheduleScanTime</span><span class="sxs-lookup"><span data-stu-id="71d65-221">ScheduleScanTime</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-schedulescantime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-222">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-222">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-223">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-224">SignatureUpdateInterval</span><span class="sxs-lookup"><span data-stu-id="71d65-224">SignatureUpdateInterval</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-signatureupdateinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-225">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-226">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-227">SubmitSamplesConsent</span><span class="sxs-lookup"><span data-stu-id="71d65-227">SubmitSamplesConsent</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-submitsamplesconsent)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-228">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="71d65-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-229">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="71d65-230">ThreatSeverityDefaultAction</span><span class="sxs-lookup"><span data-stu-id="71d65-230">ThreatSeverityDefaultAction</span></span>](/windows/client-management/mdm/policy-csp-defender#defender-threatseveritydefaultaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="71d65-231">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="71d65-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="71d65-232">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="71d65-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="71d65-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="71d65-233">Requirements</span></span>



| <span data-ttu-id="71d65-234">需求</span><span class="sxs-lookup"><span data-stu-id="71d65-234">Requirement</span></span> | <span data-ttu-id="71d65-235">值</span><span class="sxs-lookup"><span data-stu-id="71d65-235">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71d65-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71d65-236">Minimum supported client</span></span><br/> | <span data-ttu-id="71d65-237">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="71d65-237">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71d65-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71d65-238">Minimum supported server</span></span><br/> | <span data-ttu-id="71d65-239">都不支援</span><span class="sxs-lookup"><span data-stu-id="71d65-239">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="71d65-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="71d65-240">Namespace</span></span><br/>                | <span data-ttu-id="71d65-241">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="71d65-241">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="71d65-242">MOF</span><span class="sxs-lookup"><span data-stu-id="71d65-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71d65-243"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-243"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="71d65-244">DLL</span><span class="sxs-lookup"><span data-stu-id="71d65-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71d65-245"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d65-245"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71d65-246">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71d65-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71d65-247">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="71d65-247">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


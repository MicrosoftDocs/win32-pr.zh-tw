---
title: MDM_Policy_Config01_System02 類別
description: MDM \_ Policy \_ Config01 \_ System02 類別代表可用的系統原則。
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- MDM_Policy_ConfigSource01_System02 類別
- MDM_Policy_ConfigSource01_System02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685951"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="f3b89-105">MDM \_ 原則 \_ Config01 \_ System02 類別</span><span class="sxs-lookup"><span data-stu-id="f3b89-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="f3b89-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="f3b89-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f3b89-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="f3b89-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f3b89-108">**MDM \_ Policy \_ Config01 \_ System02** 類別代表可用的系統原則。</span><span class="sxs-lookup"><span data-stu-id="f3b89-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="f3b89-109">這些原則會決定允許的系統組態。</span><span class="sxs-lookup"><span data-stu-id="f3b89-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="f3b89-110">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b89-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b89-111">語法</span><span class="sxs-lookup"><span data-stu-id="f3b89-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="f3b89-112">成員</span><span class="sxs-lookup"><span data-stu-id="f3b89-112">Members</span></span>

<span data-ttu-id="f3b89-113">**MDM \_ Policy \_ ConfigSource01 \_ System02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3b89-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="f3b89-114">屬性</span><span class="sxs-lookup"><span data-stu-id="f3b89-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3b89-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f3b89-115">Properties</span></span>

<span data-ttu-id="f3b89-116">**MDM \_ Policy \_ ConfigSource01 \_ System02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f3b89-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f3b89-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="f3b89-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-118">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-119">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="f3b89-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-121">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-122">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="f3b89-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-124">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-125">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="f3b89-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-127">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-128">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="f3b89-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-130">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-131">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="f3b89-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-133">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-134">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="f3b89-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-136">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-137">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="f3b89-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-139">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-140">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="f3b89-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3b89-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-143">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="f3b89-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-145">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-146">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="f3b89-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-148">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-149">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="f3b89-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-151">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3b89-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-152">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f3b89-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="f3b89-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-154">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-155">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3b89-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f3b89-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3b89-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3b89-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-159">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3b89-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3b89-160">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3b89-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="f3b89-161">此類別的字串為 "System"。</span><span class="sxs-lookup"><span data-stu-id="f3b89-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="f3b89-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="f3b89-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-163">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="f3b89-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-164">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f3b89-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f3b89-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-166">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3b89-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-167">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="f3b89-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-168">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f3b89-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f3b89-169">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="f3b89-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="f3b89-170">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="f3b89-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="f3b89-171">"./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="f3b89-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="f3b89-172">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="f3b89-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3b89-173">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f3b89-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3b89-174">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f3b89-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3b89-175">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3b89-175">Requirements</span></span>



| <span data-ttu-id="f3b89-176">需求</span><span class="sxs-lookup"><span data-stu-id="f3b89-176">Requirement</span></span> | <span data-ttu-id="f3b89-177">值</span><span class="sxs-lookup"><span data-stu-id="f3b89-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b89-178">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3b89-178">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b89-179">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3b89-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3b89-180">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3b89-180">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b89-181">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3b89-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f3b89-182">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3b89-182">Namespace</span></span><br/>                | <span data-ttu-id="f3b89-183">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="f3b89-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="f3b89-184">MOF</span><span class="sxs-lookup"><span data-stu-id="f3b89-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3b89-185"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3b89-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3b89-186">DLL</span><span class="sxs-lookup"><span data-stu-id="f3b89-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3b89-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3b89-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b89-188">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3b89-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b89-189">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="f3b89-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


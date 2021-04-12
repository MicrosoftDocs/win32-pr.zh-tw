---
title: MDM_Policy_Result01_WindowsDefenderSecurityCenter02 類別
description: MDM \_ Policy \_ Result01 \_ WindowsDefenderSecurityCenter02 類別代表 Windows Defender 的安全中心原則。
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02 類別
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464372"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="599d1-105">MDM \_ 原則 \_ Result01 \_ WindowsDefenderSecurityCenter02 類別</span><span class="sxs-lookup"><span data-stu-id="599d1-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="599d1-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="599d1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="599d1-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="599d1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="599d1-108">MDM \_ Policy \_ Result01 \_ WindowsDefenderSecurityCenter02 類別代表 Windows Defender 的安全中心原則。</span><span class="sxs-lookup"><span data-stu-id="599d1-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="599d1-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="599d1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="599d1-110">語法</span><span class="sxs-lookup"><span data-stu-id="599d1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="599d1-111">成員</span><span class="sxs-lookup"><span data-stu-id="599d1-111">Members</span></span>

<span data-ttu-id="599d1-112">**MDM \_ Policy \_ Result01 \_ WindowsDefenderSecurityCenter02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="599d1-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="599d1-113">屬性</span><span class="sxs-lookup"><span data-stu-id="599d1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="599d1-114">屬性</span><span class="sxs-lookup"><span data-stu-id="599d1-114">Properties</span></span>

<span data-ttu-id="599d1-115">**MDM \_ Policy \_ Result01 \_ WindowsDefenderSecurityCenter02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="599d1-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="599d1-116">CompanyName</span><span class="sxs-lookup"><span data-stu-id="599d1-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-117">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="599d1-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="599d1-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="599d1-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="599d1-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="599d1-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="599d1-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-135">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="599d1-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-138">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="599d1-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-143">電子郵件</span><span class="sxs-lookup"><span data-stu-id="599d1-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="599d1-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="599d1-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="599d1-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="599d1-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="599d1-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599d1-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599d1-155">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="599d1-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="599d1-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="599d1-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-157">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-158">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="599d1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="599d1-159">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="599d1-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-160">電話</span><span class="sxs-lookup"><span data-stu-id="599d1-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-161">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-162">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="599d1-163">URL</span><span class="sxs-lookup"><span data-stu-id="599d1-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="599d1-164">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="599d1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="599d1-165">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="599d1-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="599d1-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="599d1-166">Requirements</span></span>



| <span data-ttu-id="599d1-167">需求</span><span class="sxs-lookup"><span data-stu-id="599d1-167">Requirement</span></span> | <span data-ttu-id="599d1-168">值</span><span class="sxs-lookup"><span data-stu-id="599d1-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599d1-169">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="599d1-169">Minimum supported client</span></span><br/> | <span data-ttu-id="599d1-170">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="599d1-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="599d1-171">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="599d1-171">Minimum supported server</span></span><br/> | <span data-ttu-id="599d1-172">都不支援</span><span class="sxs-lookup"><span data-stu-id="599d1-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="599d1-173">命名空間</span><span class="sxs-lookup"><span data-stu-id="599d1-173">Namespace</span></span><br/>                | <span data-ttu-id="599d1-174">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="599d1-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="599d1-175">MOF</span><span class="sxs-lookup"><span data-stu-id="599d1-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="599d1-176"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="599d1-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="599d1-177">DLL</span><span class="sxs-lookup"><span data-stu-id="599d1-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="599d1-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="599d1-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 


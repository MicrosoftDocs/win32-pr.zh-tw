---
title: MDM_Policy_Config01_DeviceLock02 類別
description: MDM \_ Policy \_ Config01 \_ DeviceLock02 類別代表可用的裝置鎖定原則。
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- MDM_Policy_Config01_DeviceLock02 類別
- MDM_Policy_Config01_DeviceLock02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105726"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="1c345-105">MDM \_ 原則 \_ Config01 \_ DeviceLock02 類別</span><span class="sxs-lookup"><span data-stu-id="1c345-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="1c345-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="1c345-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1c345-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="1c345-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c345-108">**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別代表可用的裝置鎖定原則。</span><span class="sxs-lookup"><span data-stu-id="1c345-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="1c345-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1c345-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c345-110">語法</span><span class="sxs-lookup"><span data-stu-id="1c345-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="1c345-111">成員</span><span class="sxs-lookup"><span data-stu-id="1c345-111">Members</span></span>

<span data-ttu-id="1c345-112">**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1c345-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="1c345-113">屬性</span><span class="sxs-lookup"><span data-stu-id="1c345-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c345-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1c345-114">Properties</span></span>

<span data-ttu-id="1c345-115">**MDM \_ Policy \_ Config01 \_ DeviceLock02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1c345-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c345-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="1c345-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="1c345-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="1c345-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="1c345-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1c345-128">當使用 WMI 來設定 EAS DeviceLock 原則時，不應該將 DevicePasswordEnabled 設定為啟用 (0) ，因為它在原則 CSP 中預設為啟用，以提供與 Windows 8 的回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="1c345-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="1c345-129">如果 DevicePasswordEnabled 設為 Enabled (0) 則原則 CSP 將會傳回錯誤，指出 DevicePasswordEnabled 已經存在。</span><span class="sxs-lookup"><span data-stu-id="1c345-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="1c345-130">Windows 8. x 不支援 DevicePassword 原則。</span><span class="sxs-lookup"><span data-stu-id="1c345-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="1c345-131">停用 DevicePasswordEnabled (1) 之後，這應該是從下面的原則 DeviceLock 群組中唯一設定的原則。</span><span class="sxs-lookup"><span data-stu-id="1c345-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="1c345-132">原則列示如下： >-DevicePasswordEnabled 是下列的父原則：</span><span class="sxs-lookup"><span data-stu-id="1c345-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="1c345-133">DevicePasswordEnabled 是下列的父原則：</span><span class="sxs-lookup"><span data-stu-id="1c345-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="1c345-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="1c345-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="1c345-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="1c345-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="1c345-136">AlphanumericDevicePasswordRequired 是的父原則：</span><span class="sxs-lookup"><span data-stu-id="1c345-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="1c345-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="1c345-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="1c345-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="1c345-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="1c345-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="1c345-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="1c345-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="1c345-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-141">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-142">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="1c345-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-144">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-145">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-146">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="1c345-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c345-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c345-149">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="1c345-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-150">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c345-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c345-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1c345-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-153">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c345-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-154">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c345-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c345-155">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c345-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c345-156">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="1c345-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="1c345-157">此類別的字串為 "DeviceLock"。</span><span class="sxs-lookup"><span data-stu-id="1c345-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="1c345-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="1c345-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="1c345-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-162">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-163">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="1c345-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-165">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-166">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="1c345-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-168">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1c345-170">Msds-minimumpasswordage</span><span class="sxs-lookup"><span data-stu-id="1c345-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c345-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1c345-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-174">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c345-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-175">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1c345-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c345-176">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1c345-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1c345-177">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="1c345-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="1c345-178">此類別的字串為 "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="1c345-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="1c345-179">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="1c345-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-180">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c345-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-181">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1c345-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="1c345-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c345-183">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="1c345-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1c345-184">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1c345-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1c345-185">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c345-185">Requirements</span></span>



| <span data-ttu-id="1c345-186">需求</span><span class="sxs-lookup"><span data-stu-id="1c345-186">Requirement</span></span> | <span data-ttu-id="1c345-187">值</span><span class="sxs-lookup"><span data-stu-id="1c345-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c345-188">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c345-188">Minimum supported client</span></span><br/> | <span data-ttu-id="1c345-189">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c345-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c345-190">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c345-190">Minimum supported server</span></span><br/> | <span data-ttu-id="1c345-191">都不支援</span><span class="sxs-lookup"><span data-stu-id="1c345-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1c345-192">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c345-192">Namespace</span></span><br/>                | <span data-ttu-id="1c345-193">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="1c345-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="1c345-194">MOF</span><span class="sxs-lookup"><span data-stu-id="1c345-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c345-195"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c345-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c345-196">DLL</span><span class="sxs-lookup"><span data-stu-id="1c345-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c345-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c345-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c345-198">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c345-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c345-199">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="1c345-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


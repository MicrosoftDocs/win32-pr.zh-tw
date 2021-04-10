---
title: MDM_Policy_Result01_DeviceLock02 類別
description: MDM \_ Policy \_ Result01 \_ DeviceLock02 類別代表可用的裝置鎖定原則。
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- MDM_Policy_Result01_DeviceLock02 類別
- MDM_Policy_Result01_DeviceLock02 類別，描述
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843635"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="3e605-105">MDM \_ 原則 \_ Result01 \_ DeviceLock02 類別</span><span class="sxs-lookup"><span data-stu-id="3e605-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="3e605-106">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3e605-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e605-107">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3e605-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e605-108">**MDM \_ Policy \_ Result01 \_ DeviceLock02** 類別代表可用的裝置鎖定原則。</span><span class="sxs-lookup"><span data-stu-id="3e605-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="3e605-109">下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="3e605-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e605-110">語法</span><span class="sxs-lookup"><span data-stu-id="3e605-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="3e605-111">成員</span><span class="sxs-lookup"><span data-stu-id="3e605-111">Members</span></span>

<span data-ttu-id="3e605-112">**MDM \_ Policy \_ Result01 \_ DeviceLock02** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="3e605-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="3e605-113">屬性</span><span class="sxs-lookup"><span data-stu-id="3e605-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e605-114">屬性</span><span class="sxs-lookup"><span data-stu-id="3e605-114">Properties</span></span>

<span data-ttu-id="3e605-115">**MDM \_ Policy \_ Result01 \_ DeviceLock02** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="3e605-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e605-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="3e605-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-117">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-118">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="3e605-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-120">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-121">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="3e605-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-123">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-124">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="3e605-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-126">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-127">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="3e605-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-129">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-130">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="3e605-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-132">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-133">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-134">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="3e605-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-135">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e605-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-136">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e605-137">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="3e605-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-138">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e605-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-139">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e605-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e605-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-141">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e605-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-142">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e605-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e605-143">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e605-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e605-144">識別父節點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e605-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="3e605-145">此類別的字串為 "DeviceLock"。</span><span class="sxs-lookup"><span data-stu-id="3e605-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="3e605-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="3e605-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-147">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-148">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="3e605-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-150">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-151">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="3e605-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-153">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-154">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="3e605-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-156">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-157">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e605-158">Msds-minimumpasswordage</span><span class="sxs-lookup"><span data-stu-id="3e605-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-159">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-160">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e605-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e605-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-162">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e605-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-163">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="3e605-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e605-164">限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e605-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3e605-165">描述父節點的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="3e605-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="3e605-166">此類別的字串為 "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="3e605-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="3e605-167">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="3e605-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-168">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3e605-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-169">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e605-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="3e605-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e605-171">資料類型： **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e605-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e605-172">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="3e605-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e605-173">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e605-173">Requirements</span></span>



| <span data-ttu-id="3e605-174">需求</span><span class="sxs-lookup"><span data-stu-id="3e605-174">Requirement</span></span> | <span data-ttu-id="3e605-175">值</span><span class="sxs-lookup"><span data-stu-id="3e605-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e605-176">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e605-176">Minimum supported client</span></span><br/> | <span data-ttu-id="3e605-177">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e605-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e605-178">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e605-178">Minimum supported server</span></span><br/> | <span data-ttu-id="3e605-179">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e605-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3e605-180">命名空間</span><span class="sxs-lookup"><span data-stu-id="3e605-180">Namespace</span></span><br/>                | <span data-ttu-id="3e605-181">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="3e605-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3e605-182">MOF</span><span class="sxs-lookup"><span data-stu-id="3e605-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e605-183"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e605-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e605-184">DLL</span><span class="sxs-lookup"><span data-stu-id="3e605-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e605-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e605-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e605-186">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e605-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e605-187">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="3e605-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 


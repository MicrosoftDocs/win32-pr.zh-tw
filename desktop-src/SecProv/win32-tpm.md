---
description: 代表 (TPM) 的可信賴平臺模組，這是為電腦系統提供根信任的硬體安全晶片。
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988951"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="72da4-103">Win32 \_ Tpm 類別</span><span class="sxs-lookup"><span data-stu-id="72da4-103">Win32\_Tpm class</span></span>

<span data-ttu-id="72da4-104">**Win32 \_ tpm** 類別代表 (Tpm) 的可信賴平臺模組，這是為電腦系統提供根信任的硬體安全晶片。</span><span class="sxs-lookup"><span data-stu-id="72da4-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="72da4-105">語法</span><span class="sxs-lookup"><span data-stu-id="72da4-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="72da4-106">成員</span><span class="sxs-lookup"><span data-stu-id="72da4-106">Members</span></span>

<span data-ttu-id="72da4-107">**Win32 \_ Tpm** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="72da4-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="72da4-108">方法</span><span class="sxs-lookup"><span data-stu-id="72da4-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="72da4-109">屬性</span><span class="sxs-lookup"><span data-stu-id="72da4-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="72da4-110">方法</span><span class="sxs-lookup"><span data-stu-id="72da4-110">Methods</span></span>

<span data-ttu-id="72da4-111">**Win32 \_ Tpm** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="72da4-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="72da4-112">方法</span><span class="sxs-lookup"><span data-stu-id="72da4-112">Method</span></span>                                                                                   | <span data-ttu-id="72da4-113">描述</span><span class="sxs-lookup"><span data-stu-id="72da4-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72da4-114">**AddBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="72da4-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="72da4-115">將 TPM 命令新增至 Windows 上封鎖的本機命令清單。</span><span class="sxs-lookup"><span data-stu-id="72da4-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="72da4-116">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="72da4-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="72da4-117">變更 TPM 擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="72da4-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="72da4-118">**清楚**</span><span class="sxs-lookup"><span data-stu-id="72da4-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="72da4-119">將 TPM 重設為其原廠預設狀態。</span><span class="sxs-lookup"><span data-stu-id="72da4-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="72da4-120">**ConvertToOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="72da4-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="72da4-121">將使用者提供的複雜密碼轉換成20位元組的擁有者授權值，可用來與 TPM 互動。</span><span class="sxs-lookup"><span data-stu-id="72da4-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="72da4-122">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="72da4-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="72da4-123">在 TPM 上建立2048位簽署金鑰組。</span><span class="sxs-lookup"><span data-stu-id="72da4-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="72da4-124">**停用**</span><span class="sxs-lookup"><span data-stu-id="72da4-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="72da4-125">允許 TPM 擁有者停用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="72da4-126">**啟用**</span><span class="sxs-lookup"><span data-stu-id="72da4-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="72da4-127">允許 TPM 擁有者啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="72da4-128">**GetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="72da4-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="72da4-129">取得並傳回暫止的 TPM 實體存在性作業。</span><span class="sxs-lookup"><span data-stu-id="72da4-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="72da4-130">使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來要求作業。</span><span class="sxs-lookup"><span data-stu-id="72da4-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="72da4-131">**GetPhysicalPresenceResponse**</span><span class="sxs-lookup"><span data-stu-id="72da4-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="72da4-132">取得並傳回已執行之 TPM 實體存在作業的結果。</span><span class="sxs-lookup"><span data-stu-id="72da4-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="72da4-133">**GetPhysicalPresenceTransition**</span><span class="sxs-lookup"><span data-stu-id="72da4-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="72da4-134">指出執行 TPM 實體目前狀態作業所需的使用者動作。</span><span class="sxs-lookup"><span data-stu-id="72da4-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="72da4-135">**IsActivated**</span><span class="sxs-lookup"><span data-stu-id="72da4-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="72da4-136">指出是否啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="72da4-137">**IsCommandBlocked**</span><span class="sxs-lookup"><span data-stu-id="72da4-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="72da4-138">指出 TPM 命令是否可在此作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="72da4-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="72da4-139">**IsCommandPresent**</span><span class="sxs-lookup"><span data-stu-id="72da4-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="72da4-140">指出此電腦是否支援 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="72da4-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="72da4-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="72da4-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="72da4-142">指出是否已啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="72da4-143">**IsEndorsementKeyPairPresent**</span><span class="sxs-lookup"><span data-stu-id="72da4-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="72da4-144">指出 TPM 是否有簽署金鑰組。</span><span class="sxs-lookup"><span data-stu-id="72da4-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="72da4-145">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="72da4-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="72da4-146">指出 TPM 是否有擁有者。</span><span class="sxs-lookup"><span data-stu-id="72da4-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="72da4-147">**IsOwnerClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="72da4-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="72da4-148">指出 TPM 擁有者是否可以清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="72da4-149">**IsOwnershipAllowed**</span><span class="sxs-lookup"><span data-stu-id="72da4-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="72da4-150">指出是否可以安裝 TPM 擁有者。</span><span class="sxs-lookup"><span data-stu-id="72da4-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="72da4-151">**IsPhysicalClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="72da4-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="72da4-152">指出 TPM 實體存在作業是否可以清除 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="72da4-153">**IsPhysicalPresenceHardwareEnabled**</span><span class="sxs-lookup"><span data-stu-id="72da4-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="72da4-154">指出此電腦是否支援專用硬體路徑來表示實體存在。</span><span class="sxs-lookup"><span data-stu-id="72da4-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="72da4-155">**IsSrkAuthCompatible**</span><span class="sxs-lookup"><span data-stu-id="72da4-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="72da4-156">指出儲存根金鑰 (SRK) 授權是否與 Windows 相容。</span><span class="sxs-lookup"><span data-stu-id="72da4-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="72da4-157">**RemoveBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="72da4-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="72da4-158">從 Windows 封鎖的本機命令清單中移除 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="72da4-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="72da4-159">**ResetAuthLockOut**</span><span class="sxs-lookup"><span data-stu-id="72da4-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="72da4-160">重設 TPM 製造商所實行的超時時間或其他機制，以防止 TPM 上的字典攻擊。</span><span class="sxs-lookup"><span data-stu-id="72da4-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="72da4-161">**ResetSrkAuth**</span><span class="sxs-lookup"><span data-stu-id="72da4-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="72da4-162">重設儲存體根金鑰 (SRK) 授權值，以與 Windows 相容。</span><span class="sxs-lookup"><span data-stu-id="72da4-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="72da4-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="72da4-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="72da4-164">執行 TPM 的自我測試，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="72da4-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="72da4-165">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="72da4-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="72da4-166">要求執行 TPM 實體存在作業。</span><span class="sxs-lookup"><span data-stu-id="72da4-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="72da4-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="72da4-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="72da4-168">安裝 TPM 的擁有者。</span><span class="sxs-lookup"><span data-stu-id="72da4-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="72da4-169">屬性</span><span class="sxs-lookup"><span data-stu-id="72da4-169">Properties</span></span>

<span data-ttu-id="72da4-170">**Win32 \_ Tpm** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="72da4-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72da4-171">**IsActivated \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="72da4-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-172">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="72da4-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-174">指出是否啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="72da4-175">如果裝置已啟動 (即為 true，如果 **IsActivated \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="72da4-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="72da4-176">當具現化類別時，會儲存這個值。</span><span class="sxs-lookup"><span data-stu-id="72da4-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="72da4-177">TPM 可以在具現化和您檢查此值之間變更狀態。</span><span class="sxs-lookup"><span data-stu-id="72da4-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="72da4-178">若要檢查 TPM 是否為即時啟用，請使用 [**IsActivated**](isactivated-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="72da4-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="72da4-179">**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="72da4-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-180">**IsEnabled \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="72da4-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-181">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="72da4-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-182">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-183">指出是否已啟用 TPM。</span><span class="sxs-lookup"><span data-stu-id="72da4-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="72da4-184">如果啟用裝置 (即為 true，如果 **IsEnabled \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="72da4-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="72da4-185">當具現化類別時，會儲存這個值。</span><span class="sxs-lookup"><span data-stu-id="72da4-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="72da4-186">TPM 可以在具現化和您檢查此值之間變更狀態。</span><span class="sxs-lookup"><span data-stu-id="72da4-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="72da4-187">若要檢查是否已即時啟用 TPM，請使用 [**IsEnabled**](isenabled-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="72da4-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="72da4-188">**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="72da4-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-189">**IsOwned \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="72da4-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-190">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="72da4-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-191">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-192">指出 TPM 是否有擁有者。</span><span class="sxs-lookup"><span data-stu-id="72da4-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="72da4-193">如果裝置具有擁有者 (即為 true，如果 **IsOwned \_ InitialValue** 為 true) ，則為 **true** ，否則為 **false**。</span><span class="sxs-lookup"><span data-stu-id="72da4-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="72da4-194">當具現化類別時，會儲存這個值。</span><span class="sxs-lookup"><span data-stu-id="72da4-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="72da4-195">TPM 可以在具現化和您檢查此值之間變更狀態。</span><span class="sxs-lookup"><span data-stu-id="72da4-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="72da4-196">若要檢查 TPM 是否為即時擁有，請使用 [**IsOwned**](isowned-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="72da4-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="72da4-197">**Windows Server 2008 和 Windows Vista：** 無法使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="72da4-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-198">**ManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="72da4-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-199">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="72da4-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-200">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-201">唯一為 TPM 製造商命名的識別資訊。</span><span class="sxs-lookup"><span data-stu-id="72da4-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="72da4-202">當資料無法使用時，會傳回零。</span><span class="sxs-lookup"><span data-stu-id="72da4-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="72da4-203">您可以將每個位元組解讀為 ASCII 字元，以將此整數值轉譯成字串值。</span><span class="sxs-lookup"><span data-stu-id="72da4-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="72da4-204">例如，整數值1414548736可以分成4個位元組：0x54、0x50、0x4D 和0x00。</span><span class="sxs-lookup"><span data-stu-id="72da4-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="72da4-205">假設字串是由左至右解釋，此整數值會轉譯為 "TPM" 的字串值。</span><span class="sxs-lookup"><span data-stu-id="72da4-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="72da4-206">**ManufacturerVersion**</span><span class="sxs-lookup"><span data-stu-id="72da4-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-207">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72da4-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-208">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-209">製造商所指定的 TPM 版本。</span><span class="sxs-lookup"><span data-stu-id="72da4-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="72da4-210">當資料無法使用時，會傳回「不支援」。</span><span class="sxs-lookup"><span data-stu-id="72da4-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-211">**ManufacturerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="72da4-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-212">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72da4-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-213">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-214">TPM 的其他製造商特定版本資訊。</span><span class="sxs-lookup"><span data-stu-id="72da4-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="72da4-215">當資料無法使用時，會傳回「不支援」。</span><span class="sxs-lookup"><span data-stu-id="72da4-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-216">**PhysicalPresenceVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="72da4-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-217">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72da4-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-218">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-219">實體存在性介面的版本，這是一種通訊機制，可用來執行電腦支援的裝置作業，該作業需要實體存在。</span><span class="sxs-lookup"><span data-stu-id="72da4-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="72da4-220">此介面必須可用來執行 TPM 實體目前狀態作業。</span><span class="sxs-lookup"><span data-stu-id="72da4-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="72da4-221">**Win32 \_ Tpm** 方法 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)、 [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)、 [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)和 [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)會公開實體狀態介面的功能。</span><span class="sxs-lookup"><span data-stu-id="72da4-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="72da4-222">當資料無法使用時，會傳回「不支援」。</span><span class="sxs-lookup"><span data-stu-id="72da4-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="72da4-223">**SpecVersion**</span><span class="sxs-lookup"><span data-stu-id="72da4-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72da4-224">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="72da4-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72da4-225">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="72da4-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72da4-226">受信任運算群組的版本 (可支援 TPM 的 TCG) 規格。</span><span class="sxs-lookup"><span data-stu-id="72da4-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="72da4-227">此值包含主要和次要 TCG 規格版本、規格修訂層級和錯誤修訂層級。</span><span class="sxs-lookup"><span data-stu-id="72da4-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="72da4-228">所有值都是十六進位值。</span><span class="sxs-lookup"><span data-stu-id="72da4-228">All values are in hexadecimal.</span></span> <span data-ttu-id="72da4-229">例如，"1.2，2，0" 的版本資訊表示裝置已實作為 TCG 規格1.2 版、修訂層級2，而不含任何勘誤表。</span><span class="sxs-lookup"><span data-stu-id="72da4-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="72da4-230">當資料無法使用時，會傳回「不支援」。</span><span class="sxs-lookup"><span data-stu-id="72da4-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72da4-231">備註</span><span class="sxs-lookup"><span data-stu-id="72da4-231">Remarks</span></span>

<span data-ttu-id="72da4-232">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="72da4-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72da4-233">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="72da4-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="72da4-234">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="72da4-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72da4-235">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="72da4-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72da4-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="72da4-236">Requirements</span></span>



| <span data-ttu-id="72da4-237">需求</span><span class="sxs-lookup"><span data-stu-id="72da4-237">Requirement</span></span> | <span data-ttu-id="72da4-238">值</span><span class="sxs-lookup"><span data-stu-id="72da4-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="72da4-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72da4-239">Minimum supported client</span></span><br/> | <span data-ttu-id="72da4-240">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72da4-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="72da4-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72da4-241">Minimum supported server</span></span><br/> | <span data-ttu-id="72da4-242">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72da4-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="72da4-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="72da4-243">Namespace</span></span><br/>                | <span data-ttu-id="72da4-244">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="72da4-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="72da4-245">MOF</span><span class="sxs-lookup"><span data-stu-id="72da4-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72da4-246"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="72da4-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="72da4-247">DLL</span><span class="sxs-lookup"><span data-stu-id="72da4-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72da4-248"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72da4-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 

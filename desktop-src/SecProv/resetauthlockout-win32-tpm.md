---
description: 重設 TPM 製造商所實行的超時時間或其他機制，以防止對 TPM 授權值的字典攻擊。
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Win32_Tpm 類別的 ResetAuthLockOut 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971191"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="1c80d-103">Win32 Tpm 類別的 ResetAuthLockOut 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1c80d-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="1c80d-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **ResetAuthLockOut** 方法會重設 tpm 製造商所實行的超時時間或其他機制，以防止對 tpm 授權值的字典攻擊。</span><span class="sxs-lookup"><span data-stu-id="1c80d-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="1c80d-105">在字典攻擊中，攻擊者會嘗試透過徹底嘗試所有可能的值，來猜測正確的 TPM 授權值。</span><span class="sxs-lookup"><span data-stu-id="1c80d-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="1c80d-106">如果 TPM 因為輸入擁有者授權或其他授權值的錯誤嘗試太多次而遭到鎖定，請使用此方法。</span><span class="sxs-lookup"><span data-stu-id="1c80d-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="1c80d-107">當 TPM 被鎖定時，發出至 TPM 的部分或所有命令將會傳回錯誤，也就是執行 \_ \_ \_ \_ (0x80280803) 的 tpm E 防護鎖定。</span><span class="sxs-lookup"><span data-stu-id="1c80d-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="1c80d-108">此方法只能在 TPM 被鎖定時使用一次。如果提供給這個方法的擁有者授權不正確，TPM 將會鎖定整個超時期間，而重設鎖定的其他嘗試將會失敗。</span><span class="sxs-lookup"><span data-stu-id="1c80d-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1c80d-109">語法</span><span class="sxs-lookup"><span data-stu-id="1c80d-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="1c80d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1c80d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c80d-111">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="1c80d-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1c80d-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1c80d-112">Type: **string**</span></span>

<span data-ttu-id="1c80d-113">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="1c80d-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="1c80d-114">此字串必須是 base64 編碼的 null 終止字串，其中包含剛好20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="1c80d-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="1c80d-115">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="1c80d-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="1c80d-116">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="1c80d-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c80d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="1c80d-117">Return value</span></span>

<span data-ttu-id="1c80d-118">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1c80d-118">Type: **uint32**</span></span>

<span data-ttu-id="1c80d-119">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1c80d-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="1c80d-120">下表列出一些常見的傳回值。</span><span class="sxs-lookup"><span data-stu-id="1c80d-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="1c80d-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1c80d-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="1c80d-122">Description</span><span class="sxs-lookup"><span data-stu-id="1c80d-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c80d-123"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1c80d-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="1c80d-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1c80d-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1c80d-125"><dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="1c80d-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="1c80d-126">提供的擁有者授權值不正確。</span><span class="sxs-lookup"><span data-stu-id="1c80d-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="1c80d-127">重設鎖定的其他嘗試將會失敗，並出現相同的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1c80d-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="1c80d-128">請等到超時時間或其他製造商專屬的機制過期，再重試鎖定的 TPM 命令。</span><span class="sxs-lookup"><span data-stu-id="1c80d-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c80d-129">備註</span><span class="sxs-lookup"><span data-stu-id="1c80d-129">Remarks</span></span>

<span data-ttu-id="1c80d-130">這個方法會 \_ 在 tpm 上呼叫 tpm ResetLockValue 命令。</span><span class="sxs-lookup"><span data-stu-id="1c80d-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="1c80d-131">這種方法的確切行為會因 TPM 製造商而異。</span><span class="sxs-lookup"><span data-stu-id="1c80d-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="1c80d-132">電腦或 TPM 製造商提供的檔，可能會提供反字典攻擊機制的執行其他資訊。</span><span class="sxs-lookup"><span data-stu-id="1c80d-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="1c80d-133">一般情況下，製造商可以藉由追蹤失敗的驗證來偵測字典攻擊。</span><span class="sxs-lookup"><span data-stu-id="1c80d-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="1c80d-134">如果失敗的數目或頻率很高，TPM 將會在一段時間內鎖定更多命令。</span><span class="sxs-lookup"><span data-stu-id="1c80d-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="1c80d-135">一般來說，最初的超時期間會很短，讓合法的使用者有機會修正此情況。</span><span class="sxs-lookup"><span data-stu-id="1c80d-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="1c80d-136">如果失敗持續發生，每個後續超時期間的持續時間可能會快速增加。</span><span class="sxs-lookup"><span data-stu-id="1c80d-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="1c80d-137">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1c80d-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1c80d-138">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1c80d-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1c80d-139">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1c80d-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1c80d-140">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1c80d-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c80d-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="1c80d-141">Requirements</span></span>



| <span data-ttu-id="1c80d-142">需求</span><span class="sxs-lookup"><span data-stu-id="1c80d-142">Requirement</span></span> | <span data-ttu-id="1c80d-143">值</span><span class="sxs-lookup"><span data-stu-id="1c80d-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c80d-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1c80d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="1c80d-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c80d-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1c80d-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1c80d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="1c80d-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1c80d-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1c80d-148">命名空間</span><span class="sxs-lookup"><span data-stu-id="1c80d-148">Namespace</span></span><br/>                | <span data-ttu-id="1c80d-149">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="1c80d-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="1c80d-150">MOF</span><span class="sxs-lookup"><span data-stu-id="1c80d-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c80d-151"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c80d-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c80d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1c80d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c80d-153"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c80d-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c80d-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1c80d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c80d-155">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="1c80d-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

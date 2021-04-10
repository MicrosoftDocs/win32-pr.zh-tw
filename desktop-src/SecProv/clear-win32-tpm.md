---
description: 將 TPM 重設為其原廠預設狀態。
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Win32_Tpm 類別的 Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194170"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="eeef5-103">Win32 Tpm 類別的 Clear 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eeef5-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="eeef5-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **CLEAR** 方法會將 Tpm 重設為其原廠預設狀態。</span><span class="sxs-lookup"><span data-stu-id="eeef5-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="eeef5-105">TPM 擁有者可以使用這個方法來取消 TPM 擁有權，並使前一個擁有者所建立的密碼編譯材質失效。</span><span class="sxs-lookup"><span data-stu-id="eeef5-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="eeef5-106">如果呼叫可能會導致需要 BitLocker 修復，此方法會暫停 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="eeef5-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="eeef5-107">布建 TPM 之後，BitLocker 會自動繼續。</span><span class="sxs-lookup"><span data-stu-id="eeef5-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="eeef5-108">藉由清除 TPM，您將會遺失應用程式所建立和使用的所有 TPM 金鑰。</span><span class="sxs-lookup"><span data-stu-id="eeef5-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="eeef5-109">如果使用這些金鑰來將資料加密，請確定您有另一種方式可以在清除 TPM 之前存取資料。</span><span class="sxs-lookup"><span data-stu-id="eeef5-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eeef5-110">語法</span><span class="sxs-lookup"><span data-stu-id="eeef5-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="eeef5-111">參數</span><span class="sxs-lookup"><span data-stu-id="eeef5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeef5-112">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="eeef5-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eeef5-113">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="eeef5-113">Type: **string**</span></span>

<span data-ttu-id="eeef5-114">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="eeef5-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="eeef5-115">此字串必須是 base64 編碼的字串，其中只包含20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="eeef5-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="eeef5-116">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="eeef5-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="eeef5-117">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="eeef5-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeef5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="eeef5-118">Return value</span></span>

<span data-ttu-id="eeef5-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eeef5-119">Type: **uint32**</span></span>

<span data-ttu-id="eeef5-120">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="eeef5-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="eeef5-121">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="eeef5-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="eeef5-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="eeef5-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="eeef5-123">Description</span><span class="sxs-lookup"><span data-stu-id="eeef5-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eeef5-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eeef5-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="eeef5-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="eeef5-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="eeef5-126"><dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="eeef5-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="eeef5-127">提供的擁有者授權值無法執行要求。</span><span class="sxs-lookup"><span data-stu-id="eeef5-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="eeef5-128"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="eeef5-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="eeef5-129">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="eeef5-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="eeef5-130">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="eeef5-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eeef5-131">備註</span><span class="sxs-lookup"><span data-stu-id="eeef5-131">Remarks</span></span>

<span data-ttu-id="eeef5-132">執行此方法可協助準備配備 TPM 的電腦以進行回收。</span><span class="sxs-lookup"><span data-stu-id="eeef5-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="eeef5-133">若要清除 TPM，但不再擁有 TPM 擁有者授權，您需要電腦的實體存取權。</span><span class="sxs-lookup"><span data-stu-id="eeef5-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="eeef5-134">[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)方法包含的功能可協助您清除沒有 tpm 擁有者授權的 tpm。</span><span class="sxs-lookup"><span data-stu-id="eeef5-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="eeef5-135">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="eeef5-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eeef5-136">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="eeef5-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eeef5-137">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="eeef5-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eeef5-138">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="eeef5-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeef5-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="eeef5-139">Requirements</span></span>



| <span data-ttu-id="eeef5-140">需求</span><span class="sxs-lookup"><span data-stu-id="eeef5-140">Requirement</span></span> | <span data-ttu-id="eeef5-141">值</span><span class="sxs-lookup"><span data-stu-id="eeef5-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeef5-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eeef5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eeef5-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeef5-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eeef5-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eeef5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eeef5-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eeef5-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eeef5-146">命名空間</span><span class="sxs-lookup"><span data-stu-id="eeef5-146">Namespace</span></span><br/>                | <span data-ttu-id="eeef5-147">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="eeef5-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="eeef5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="eeef5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eeef5-149"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="eeef5-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="eeef5-150">DLL</span><span class="sxs-lookup"><span data-stu-id="eeef5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeef5-151"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeef5-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeef5-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eeef5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeef5-153">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="eeef5-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

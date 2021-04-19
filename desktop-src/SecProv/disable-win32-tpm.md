---
description: 允許 TPM 擁有者停用或暫停 TPM。
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Disable Win32_Tpm 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972192"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="ff967-103">Disable Win32 \_ Tpm 類別的方法</span><span class="sxs-lookup"><span data-stu-id="ff967-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="ff967-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **DISABLE** 方法可讓 tpm 擁有者停用或暫停 tpm。</span><span class="sxs-lookup"><span data-stu-id="ff967-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="ff967-105">如果呼叫可能會導致需要 BitLocker 修復，此方法會暫停 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="ff967-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="ff967-106">布建 TPM 之後，BitLocker 會自動繼續。</span><span class="sxs-lookup"><span data-stu-id="ff967-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff967-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff967-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="ff967-108">參數</span><span class="sxs-lookup"><span data-stu-id="ff967-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff967-109">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ff967-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ff967-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ff967-110">Type: **string**</span></span>

<span data-ttu-id="ff967-111">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="ff967-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="ff967-112">此字串必須是 base64 編碼的字串，其中只包含20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="ff967-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="ff967-113">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="ff967-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="ff967-114">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="ff967-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff967-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff967-115">Return value</span></span>

<span data-ttu-id="ff967-116">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ff967-116">Type: **uint32**</span></span>

<span data-ttu-id="ff967-117">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff967-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="ff967-118">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="ff967-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="ff967-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ff967-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="ff967-120">Description</span><span class="sxs-lookup"><span data-stu-id="ff967-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff967-121"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ff967-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="ff967-122">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ff967-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="ff967-123"><dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="ff967-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="ff967-124">提供的擁有者授權值無法執行要求。</span><span class="sxs-lookup"><span data-stu-id="ff967-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="ff967-125"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="ff967-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="ff967-126">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="ff967-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="ff967-127">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff967-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff967-128">備註</span><span class="sxs-lookup"><span data-stu-id="ff967-128">Remarks</span></span>

<span data-ttu-id="ff967-129">若要在沒有 TPM 擁有者授權值的情況下停用 TPM，請使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="ff967-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="ff967-130">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ff967-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ff967-131">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ff967-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ff967-132">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ff967-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ff967-133">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="ff967-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff967-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff967-134">Requirements</span></span>



| <span data-ttu-id="ff967-135">需求</span><span class="sxs-lookup"><span data-stu-id="ff967-135">Requirement</span></span> | <span data-ttu-id="ff967-136">值</span><span class="sxs-lookup"><span data-stu-id="ff967-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff967-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff967-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ff967-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff967-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ff967-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff967-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ff967-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff967-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="ff967-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="ff967-141">Namespace</span></span><br/>                | <span data-ttu-id="ff967-142">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="ff967-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="ff967-143">MOF</span><span class="sxs-lookup"><span data-stu-id="ff967-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff967-144"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff967-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff967-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ff967-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff967-146"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff967-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff967-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff967-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff967-148">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="ff967-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="ff967-149">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="ff967-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

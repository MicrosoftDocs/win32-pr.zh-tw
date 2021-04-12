---
description: 允許 TPM 擁有者啟用或繼續 TPM。
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Enable Win32_Tpm 類別的方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192935"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="efe0d-103">啟用 Win32 \_ Tpm 類別的方法</span><span class="sxs-lookup"><span data-stu-id="efe0d-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="efe0d-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **ENABLE** 方法可讓 tpm 擁有者啟用或繼續 tpm。</span><span class="sxs-lookup"><span data-stu-id="efe0d-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="efe0d-105">若要執行此方法，TPM 必須已經有擁有者。</span><span class="sxs-lookup"><span data-stu-id="efe0d-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="efe0d-106">若要啟用還沒有擁有者的 TPM，請使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="efe0d-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe0d-107">語法</span><span class="sxs-lookup"><span data-stu-id="efe0d-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="efe0d-108">參數</span><span class="sxs-lookup"><span data-stu-id="efe0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe0d-109">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="efe0d-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="efe0d-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="efe0d-110">Type: **string**</span></span>

<span data-ttu-id="efe0d-111">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="efe0d-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="efe0d-112">此字串必須是 base64 編碼的字串，其中只包含20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="efe0d-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="efe0d-113">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="efe0d-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="efe0d-114">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="efe0d-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe0d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="efe0d-115">Return value</span></span>

<span data-ttu-id="efe0d-116">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="efe0d-116">Type: **uint32**</span></span>

<span data-ttu-id="efe0d-117">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="efe0d-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="efe0d-118">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="efe0d-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="efe0d-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="efe0d-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="efe0d-120">Description</span><span class="sxs-lookup"><span data-stu-id="efe0d-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="efe0d-121"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="efe0d-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="efe0d-122">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="efe0d-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="efe0d-123"><dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="efe0d-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="efe0d-124">提供的擁有者授權值無法執行要求。</span><span class="sxs-lookup"><span data-stu-id="efe0d-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="efe0d-125"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="efe0d-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="efe0d-126">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="efe0d-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="efe0d-127">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="efe0d-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efe0d-128">備註</span><span class="sxs-lookup"><span data-stu-id="efe0d-128">Remarks</span></span>

<span data-ttu-id="efe0d-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="efe0d-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="efe0d-130">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="efe0d-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="efe0d-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="efe0d-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="efe0d-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="efe0d-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efe0d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="efe0d-133">Requirements</span></span>



| <span data-ttu-id="efe0d-134">需求</span><span class="sxs-lookup"><span data-stu-id="efe0d-134">Requirement</span></span> | <span data-ttu-id="efe0d-135">值</span><span class="sxs-lookup"><span data-stu-id="efe0d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe0d-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="efe0d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="efe0d-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe0d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="efe0d-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="efe0d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="efe0d-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="efe0d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="efe0d-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="efe0d-140">Namespace</span></span><br/>                | <span data-ttu-id="efe0d-141">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="efe0d-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="efe0d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="efe0d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efe0d-143"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="efe0d-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="efe0d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="efe0d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efe0d-145"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efe0d-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe0d-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="efe0d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe0d-147">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="efe0d-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="efe0d-148">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="efe0d-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

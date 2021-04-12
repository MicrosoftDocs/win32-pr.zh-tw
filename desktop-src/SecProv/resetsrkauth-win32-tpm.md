---
description: 重設儲存體根金鑰 (SRK) 授權值，以與作業系統相容。
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Win32_Tpm 類別的 ResetSrkAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320540"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="bdece-103">Win32 Tpm 類別的 ResetSrkAuth 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bdece-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="bdece-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **ResetSrkAuth** 方法會重設儲存體根金鑰 (SRK) 授權值，以與作業系統相容。</span><span class="sxs-lookup"><span data-stu-id="bdece-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdece-105">語法</span><span class="sxs-lookup"><span data-stu-id="bdece-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="bdece-106">參數</span><span class="sxs-lookup"><span data-stu-id="bdece-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdece-107">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bdece-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bdece-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bdece-108">Type: **string**</span></span>

<span data-ttu-id="bdece-109">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="bdece-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="bdece-110">此字串必須是 base64 編碼的 null 終止字串，其中包含剛好20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="bdece-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="bdece-111">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="bdece-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="bdece-112">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="bdece-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdece-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdece-113">Return value</span></span>

<span data-ttu-id="bdece-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bdece-114">Type: **uint32**</span></span>

<span data-ttu-id="bdece-115">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bdece-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="bdece-116">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="bdece-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="bdece-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="bdece-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="bdece-118">Description</span><span class="sxs-lookup"><span data-stu-id="bdece-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdece-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bdece-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="bdece-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="bdece-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="bdece-121"><dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="bdece-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="bdece-122">提供的擁有者授權值無法履行要求。</span><span class="sxs-lookup"><span data-stu-id="bdece-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="bdece-123"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="bdece-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="bdece-124">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="bdece-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="bdece-125">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="bdece-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdece-126">備註</span><span class="sxs-lookup"><span data-stu-id="bdece-126">Remarks</span></span>

<span data-ttu-id="bdece-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="bdece-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bdece-128">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bdece-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bdece-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="bdece-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bdece-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="bdece-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bdece-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdece-131">Requirements</span></span>



| <span data-ttu-id="bdece-132">需求</span><span class="sxs-lookup"><span data-stu-id="bdece-132">Requirement</span></span> | <span data-ttu-id="bdece-133">值</span><span class="sxs-lookup"><span data-stu-id="bdece-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdece-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdece-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bdece-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdece-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bdece-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdece-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bdece-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdece-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bdece-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="bdece-138">Namespace</span></span><br/>                | <span data-ttu-id="bdece-139">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="bdece-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="bdece-140">MOF</span><span class="sxs-lookup"><span data-stu-id="bdece-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bdece-141"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bdece-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="bdece-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bdece-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdece-143"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdece-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdece-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdece-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdece-145">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="bdece-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

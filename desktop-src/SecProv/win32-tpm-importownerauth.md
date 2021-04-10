---
description: 匯入已擁有作業系統登錄之 TPM 的擁有者授權資訊。
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: Win32_Tpm：： ImportOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943324"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="0be8f-103">Win32 \_ Tpm：： ImportOwnerAuth 方法</span><span class="sxs-lookup"><span data-stu-id="0be8f-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="0be8f-104">匯入已擁有作業系統登錄之 TPM 的擁有者授權資訊。</span><span class="sxs-lookup"><span data-stu-id="0be8f-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="0be8f-105">這項作業會先驗證提供的擁有者授權資訊是否正確。</span><span class="sxs-lookup"><span data-stu-id="0be8f-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="0be8f-106">如果正確，方法會將此資訊匯入至登錄。</span><span class="sxs-lookup"><span data-stu-id="0be8f-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="0be8f-107">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="0be8f-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be8f-108">語法</span><span class="sxs-lookup"><span data-stu-id="0be8f-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="0be8f-109">參數</span><span class="sxs-lookup"><span data-stu-id="0be8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0be8f-110">*OwnerAuth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0be8f-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0be8f-111">TPM 的有效擁有者授權資訊。</span><span class="sxs-lookup"><span data-stu-id="0be8f-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0be8f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0be8f-112">Return value</span></span>

<span data-ttu-id="0be8f-113">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0be8f-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="0be8f-114">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="0be8f-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="0be8f-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="0be8f-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="0be8f-116">Description</span><span class="sxs-lookup"><span data-stu-id="0be8f-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0be8f-117"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0be8f-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0be8f-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="0be8f-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0be8f-119">備註</span><span class="sxs-lookup"><span data-stu-id="0be8f-119">Remarks</span></span>

<span data-ttu-id="0be8f-120">在 TPM 處於「可縮減功能狀態」的情況下，此方法特別有用，而且需要匯入擁有者授權才能完全就緒，或在其中一個作業系統擁有 TPM 的雙重開機案例中，以及在其他作業系統中無法使用 TPM 的擁有者授權資訊。</span><span class="sxs-lookup"><span data-stu-id="0be8f-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="0be8f-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0be8f-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0be8f-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0be8f-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0be8f-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0be8f-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0be8f-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="0be8f-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0be8f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0be8f-125">Requirements</span></span>



| <span data-ttu-id="0be8f-126">需求</span><span class="sxs-lookup"><span data-stu-id="0be8f-126">Requirement</span></span> | <span data-ttu-id="0be8f-127">值</span><span class="sxs-lookup"><span data-stu-id="0be8f-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0be8f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0be8f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0be8f-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0be8f-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0be8f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0be8f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0be8f-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0be8f-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0be8f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="0be8f-132">Namespace</span></span><br/>                | <span data-ttu-id="0be8f-133">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="0be8f-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="0be8f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0be8f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0be8f-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0be8f-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0be8f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0be8f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0be8f-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0be8f-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0be8f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0be8f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0be8f-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="0be8f-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

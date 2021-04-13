---
description: 取得 TPM 的擁有者授權資訊（如果登錄中有提供的話）。
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: Win32_Tpm：： GetOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511151"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="58f7d-103">Win32 \_ Tpm：： GetOwnerAuth 方法</span><span class="sxs-lookup"><span data-stu-id="58f7d-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="58f7d-104">取得 TPM 的擁有者授權資訊（如果登錄中有提供的話）。</span><span class="sxs-lookup"><span data-stu-id="58f7d-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="58f7d-105">如果使用預設設定在 Windows 8 中擁有或布建 TPM，TPM 擁有者授權資訊會儲存在登錄中，而且可供此方法使用。</span><span class="sxs-lookup"><span data-stu-id="58f7d-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="58f7d-106">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="58f7d-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f7d-107">語法</span><span class="sxs-lookup"><span data-stu-id="58f7d-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="58f7d-108">參數</span><span class="sxs-lookup"><span data-stu-id="58f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f7d-109">*OwnerAuth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="58f7d-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58f7d-110">TPM 的擁有者授權資訊（如果登錄中有提供的話）。</span><span class="sxs-lookup"><span data-stu-id="58f7d-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f7d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="58f7d-111">Return value</span></span>

<span data-ttu-id="58f7d-112">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="58f7d-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="58f7d-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="58f7d-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="58f7d-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="58f7d-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="58f7d-115">Description</span><span class="sxs-lookup"><span data-stu-id="58f7d-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="58f7d-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="58f7d-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="58f7d-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="58f7d-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="58f7d-118">備註</span><span class="sxs-lookup"><span data-stu-id="58f7d-118">Remarks</span></span>

<span data-ttu-id="58f7d-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="58f7d-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="58f7d-120">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="58f7d-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="58f7d-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="58f7d-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="58f7d-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="58f7d-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58f7d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="58f7d-123">Requirements</span></span>



| <span data-ttu-id="58f7d-124">需求</span><span class="sxs-lookup"><span data-stu-id="58f7d-124">Requirement</span></span> | <span data-ttu-id="58f7d-125">值</span><span class="sxs-lookup"><span data-stu-id="58f7d-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="58f7d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="58f7d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="58f7d-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58f7d-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="58f7d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="58f7d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="58f7d-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58f7d-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="58f7d-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="58f7d-130">Namespace</span></span><br/>                | <span data-ttu-id="58f7d-131">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="58f7d-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="58f7d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="58f7d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58f7d-133"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="58f7d-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="58f7d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="58f7d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58f7d-135"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58f7d-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58f7d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58f7d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f7d-137">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="58f7d-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

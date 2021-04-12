---
description: 啟用 TPM 的自動布建（如果目前已停用）。
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: Win32_Tpm：： EnableAutoProvisioning 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318203"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="17970-103">Win32 \_ Tpm：： EnableAutoProvisioning 方法</span><span class="sxs-lookup"><span data-stu-id="17970-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="17970-104">啟用 TPM 的自動布建（如果目前已停用）。</span><span class="sxs-lookup"><span data-stu-id="17970-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="17970-105">如果已啟用自動布建，則作業沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="17970-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="17970-106">預設會啟用 Windows 8 和 Windows Server 2012 的自動布建。</span><span class="sxs-lookup"><span data-stu-id="17970-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="17970-107">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="17970-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="17970-108">語法</span><span class="sxs-lookup"><span data-stu-id="17970-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="17970-109">參數</span><span class="sxs-lookup"><span data-stu-id="17970-109">Parameters</span></span>

<span data-ttu-id="17970-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="17970-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="17970-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="17970-111">Return value</span></span>

<span data-ttu-id="17970-112">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="17970-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="17970-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="17970-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="17970-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="17970-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="17970-115">Description</span><span class="sxs-lookup"><span data-stu-id="17970-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="17970-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="17970-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="17970-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="17970-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17970-118">備註</span><span class="sxs-lookup"><span data-stu-id="17970-118">Remarks</span></span>

<span data-ttu-id="17970-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="17970-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="17970-120">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="17970-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="17970-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="17970-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="17970-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="17970-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17970-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="17970-123">Requirements</span></span>



| <span data-ttu-id="17970-124">需求</span><span class="sxs-lookup"><span data-stu-id="17970-124">Requirement</span></span> | <span data-ttu-id="17970-125">值</span><span class="sxs-lookup"><span data-stu-id="17970-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="17970-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17970-126">Minimum supported client</span></span><br/> | <span data-ttu-id="17970-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17970-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="17970-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17970-128">Minimum supported server</span></span><br/> | <span data-ttu-id="17970-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17970-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="17970-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="17970-130">Namespace</span></span><br/>                | <span data-ttu-id="17970-131">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="17970-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="17970-132">MOF</span><span class="sxs-lookup"><span data-stu-id="17970-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17970-133"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="17970-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="17970-134">DLL</span><span class="sxs-lookup"><span data-stu-id="17970-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17970-135"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17970-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17970-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17970-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17970-137">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="17970-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

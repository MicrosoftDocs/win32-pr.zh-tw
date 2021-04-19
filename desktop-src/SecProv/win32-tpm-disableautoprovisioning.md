---
description: 如果目前已啟用，則停用 TPM 的自動布建。
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm：:D isableAutoProvisioning 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975348"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="bc8d5-103">Win32 \_ Tpm：:D isableautoprovisioning 方法</span><span class="sxs-lookup"><span data-stu-id="bc8d5-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="bc8d5-104">如果目前已啟用，則停用 TPM 的自動布建。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="bc8d5-105">如果已停用自動布建，則作業沒有任何作用。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="bc8d5-106">預設會啟用 Windows 8 和 Windows Server 2012 的自動布建。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="bc8d5-107">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8d5-108">語法</span><span class="sxs-lookup"><span data-stu-id="bc8d5-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="bc8d5-109">參數</span><span class="sxs-lookup"><span data-stu-id="bc8d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc8d5-110">*OnlyForNextBoot* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="bc8d5-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bc8d5-111">如果設定為 **TRUE**，則僅針對下一次開機停用自動布建。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="bc8d5-112">如果設定為 **FALSE** 或未指定，則會永久停用自動布建。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc8d5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc8d5-113">Return value</span></span>

<span data-ttu-id="bc8d5-114">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="bc8d5-115">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="bc8d5-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="bc8d5-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="bc8d5-117">Description</span><span class="sxs-lookup"><span data-stu-id="bc8d5-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bc8d5-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bc8d5-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bc8d5-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc8d5-120">備註</span><span class="sxs-lookup"><span data-stu-id="bc8d5-120">Remarks</span></span>

<span data-ttu-id="bc8d5-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bc8d5-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bc8d5-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bc8d5-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="bc8d5-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc8d5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc8d5-125">Requirements</span></span>



| <span data-ttu-id="bc8d5-126">需求</span><span class="sxs-lookup"><span data-stu-id="bc8d5-126">Requirement</span></span> | <span data-ttu-id="bc8d5-127">值</span><span class="sxs-lookup"><span data-stu-id="bc8d5-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8d5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc8d5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bc8d5-129">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc8d5-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc8d5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc8d5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bc8d5-131">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc8d5-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bc8d5-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="bc8d5-132">Namespace</span></span><br/>                | <span data-ttu-id="bc8d5-133">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="bc8d5-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="bc8d5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="bc8d5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc8d5-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc8d5-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc8d5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc8d5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc8d5-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc8d5-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8d5-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc8d5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8d5-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="bc8d5-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

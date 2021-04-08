---
description: 指出是否已啟用 TPM 的自動布建。
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: Win32_Tpm：： IsAutoProvisioningEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850831"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="30728-103">Win32 \_ Tpm：： IsAutoProvisioningEnabled 方法</span><span class="sxs-lookup"><span data-stu-id="30728-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="30728-104">指出是否已啟用 TPM 的自動布建。</span><span class="sxs-lookup"><span data-stu-id="30728-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="30728-105">預設會啟用 Windows 8 和 Windows Server 2012 的自動布建。</span><span class="sxs-lookup"><span data-stu-id="30728-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="30728-106">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="30728-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="30728-107">語法</span><span class="sxs-lookup"><span data-stu-id="30728-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="30728-108">參數</span><span class="sxs-lookup"><span data-stu-id="30728-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30728-109">*IsAutoProvisioningEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="30728-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30728-110">如果已啟用 TPM 自動布建，則設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="30728-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30728-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="30728-111">Return value</span></span>

<span data-ttu-id="30728-112">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="30728-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="30728-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="30728-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="30728-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="30728-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="30728-115">Description</span><span class="sxs-lookup"><span data-stu-id="30728-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="30728-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="30728-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="30728-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="30728-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30728-118">備註</span><span class="sxs-lookup"><span data-stu-id="30728-118">Remarks</span></span>

<span data-ttu-id="30728-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="30728-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="30728-120">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="30728-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="30728-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="30728-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="30728-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="30728-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30728-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="30728-123">Requirements</span></span>



| <span data-ttu-id="30728-124">需求</span><span class="sxs-lookup"><span data-stu-id="30728-124">Requirement</span></span> | <span data-ttu-id="30728-125">值</span><span class="sxs-lookup"><span data-stu-id="30728-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30728-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="30728-126">Minimum supported client</span></span><br/> | <span data-ttu-id="30728-127">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30728-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30728-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="30728-128">Minimum supported server</span></span><br/> | <span data-ttu-id="30728-129">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="30728-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="30728-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="30728-130">Namespace</span></span><br/>                | <span data-ttu-id="30728-131">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="30728-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="30728-132">MOF</span><span class="sxs-lookup"><span data-stu-id="30728-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30728-133"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="30728-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="30728-134">DLL</span><span class="sxs-lookup"><span data-stu-id="30728-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30728-135"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30728-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30728-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30728-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30728-137">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="30728-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

---
description: 指出 TPM 是否已準備好可供使用。
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: Win32_Tpm：： IsReady 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511150"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="5b9c6-103">Win32 \_ Tpm：： IsReady 方法</span><span class="sxs-lookup"><span data-stu-id="5b9c6-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="5b9c6-104">指出 TPM 是否已準備好可供使用。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="5b9c6-105">只有本機系統管理員才能存取此方法。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b9c6-106">語法</span><span class="sxs-lookup"><span data-stu-id="5b9c6-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="5b9c6-107">參數</span><span class="sxs-lookup"><span data-stu-id="5b9c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b9c6-108">*IsReady* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b9c6-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b9c6-109">如果 TPM 和系統已完全布建以供 TPM 使用，則設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b9c6-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b9c6-110">Return value</span></span>

<span data-ttu-id="5b9c6-111">您可以傳回所有 TPM 錯誤以及 [Tpm 基礎服務](../tbs/tbs-return-codes.md) 特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="5b9c6-112">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="5b9c6-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5b9c6-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5b9c6-114">Description</span><span class="sxs-lookup"><span data-stu-id="5b9c6-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5b9c6-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5b9c6-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5b9c6-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b9c6-117">備註</span><span class="sxs-lookup"><span data-stu-id="5b9c6-117">Remarks</span></span>

<span data-ttu-id="5b9c6-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5b9c6-119">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5b9c6-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5b9c6-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="5b9c6-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5b9c6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b9c6-122">Requirements</span></span>



| <span data-ttu-id="5b9c6-123">需求</span><span class="sxs-lookup"><span data-stu-id="5b9c6-123">Requirement</span></span> | <span data-ttu-id="5b9c6-124">值</span><span class="sxs-lookup"><span data-stu-id="5b9c6-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b9c6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b9c6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="5b9c6-126">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b9c6-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5b9c6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b9c6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="5b9c6-128">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b9c6-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5b9c6-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b9c6-129">Namespace</span></span><br/>                | <span data-ttu-id="5b9c6-130">\\\\.\\根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="5b9c6-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="5b9c6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="5b9c6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b9c6-132"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b9c6-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b9c6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5b9c6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b9c6-134"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b9c6-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b9c6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b9c6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b9c6-136">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="5b9c6-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

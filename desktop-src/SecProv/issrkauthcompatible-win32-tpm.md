---
description: Win32 Tpm 類別的 IsSrkAuthCompatible 方法 \_ 會指出儲存根金鑰 (SRK) 授權是否與 Windows Vista 所預期的值相容。
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Win32_Tpm 類別的 IsSrkAuthCompatible 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850840"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="6b24d-103">Win32 Tpm 類別的 IsSrkAuthCompatible 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6b24d-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="6b24d-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsSrkAuthCompatible** 方法會指出儲存根金鑰 (SRK) 授權是否與 Windows Vista 所預期的值相容。</span><span class="sxs-lookup"><span data-stu-id="6b24d-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b24d-105">語法</span><span class="sxs-lookup"><span data-stu-id="6b24d-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="6b24d-106">參數</span><span class="sxs-lookup"><span data-stu-id="6b24d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b24d-107">*IsSrkAuthCompatible* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6b24d-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b24d-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6b24d-108">Type: **boolean**</span></span>

<span data-ttu-id="6b24d-109">若 **為 true**，則 SRK 授權值的值為零。</span><span class="sxs-lookup"><span data-stu-id="6b24d-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b24d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b24d-110">Return value</span></span>

<span data-ttu-id="6b24d-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6b24d-111">Type: **uint32**</span></span>

<span data-ttu-id="6b24d-112">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6b24d-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="6b24d-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="6b24d-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="6b24d-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6b24d-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="6b24d-115">Description</span><span class="sxs-lookup"><span data-stu-id="6b24d-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6b24d-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b24d-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6b24d-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6b24d-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6b24d-118">備註</span><span class="sxs-lookup"><span data-stu-id="6b24d-118">Remarks</span></span>

<span data-ttu-id="6b24d-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6b24d-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6b24d-120">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6b24d-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6b24d-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6b24d-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6b24d-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="6b24d-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b24d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b24d-123">Requirements</span></span>



| <span data-ttu-id="6b24d-124">需求</span><span class="sxs-lookup"><span data-stu-id="6b24d-124">Requirement</span></span> | <span data-ttu-id="6b24d-125">值</span><span class="sxs-lookup"><span data-stu-id="6b24d-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b24d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b24d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6b24d-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b24d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b24d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b24d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6b24d-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b24d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6b24d-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="6b24d-130">Namespace</span></span><br/>                | <span data-ttu-id="6b24d-131">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="6b24d-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="6b24d-132">MOF</span><span class="sxs-lookup"><span data-stu-id="6b24d-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b24d-133"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b24d-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b24d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6b24d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b24d-135"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b24d-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b24d-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b24d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b24d-137">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="6b24d-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

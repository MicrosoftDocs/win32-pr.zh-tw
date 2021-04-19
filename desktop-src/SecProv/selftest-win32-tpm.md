---
description: 執行 TPM 的自我測試，並傳回結果。
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Win32_Tpm 類別的 SelfTest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991815"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="fadbf-103">Win32 Tpm 類別的 SelfTest 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fadbf-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="fadbf-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **SELFTEST** 方法會執行 Tpm 的自我測試，並傳回結果。</span><span class="sxs-lookup"><span data-stu-id="fadbf-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="fadbf-105">當電腦啟動時，會自動執行 TPM 自我測試。</span><span class="sxs-lookup"><span data-stu-id="fadbf-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="fadbf-106">語法</span><span class="sxs-lookup"><span data-stu-id="fadbf-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="fadbf-107">參數</span><span class="sxs-lookup"><span data-stu-id="fadbf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fadbf-108">*SelfTestResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fadbf-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fadbf-109">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fadbf-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="fadbf-110">包含自我測試結果的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="fadbf-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="fadbf-111">此參數的格式是製造商專用的。</span><span class="sxs-lookup"><span data-stu-id="fadbf-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fadbf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fadbf-112">Return value</span></span>

<span data-ttu-id="fadbf-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fadbf-113">Type: **uint32**</span></span>

<span data-ttu-id="fadbf-114">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="fadbf-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="fadbf-115">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="fadbf-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="fadbf-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fadbf-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="fadbf-117">Description</span><span class="sxs-lookup"><span data-stu-id="fadbf-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="fadbf-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fadbf-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="fadbf-119">此方法已成功執行。</span><span class="sxs-lookup"><span data-stu-id="fadbf-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fadbf-120">備註</span><span class="sxs-lookup"><span data-stu-id="fadbf-120">Remarks</span></span>

<span data-ttu-id="fadbf-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fadbf-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fadbf-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fadbf-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fadbf-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fadbf-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fadbf-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="fadbf-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fadbf-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="fadbf-125">Requirements</span></span>



| <span data-ttu-id="fadbf-126">需求</span><span class="sxs-lookup"><span data-stu-id="fadbf-126">Requirement</span></span> | <span data-ttu-id="fadbf-127">值</span><span class="sxs-lookup"><span data-stu-id="fadbf-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fadbf-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fadbf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fadbf-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fadbf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="fadbf-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fadbf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fadbf-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fadbf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fadbf-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="fadbf-132">Namespace</span></span><br/>                | <span data-ttu-id="fadbf-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="fadbf-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="fadbf-134">MOF</span><span class="sxs-lookup"><span data-stu-id="fadbf-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fadbf-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fadbf-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="fadbf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fadbf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fadbf-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fadbf-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fadbf-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fadbf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fadbf-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="fadbf-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

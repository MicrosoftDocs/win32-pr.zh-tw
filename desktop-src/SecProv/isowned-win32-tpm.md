---
description: Win32 Tpm 類別的 IsOwned 方法會 \_ 指出裝置是否有擁有者。 TakeOwnership 方法會變更這個值。
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Win32_Tpm 類別的 IsOwned 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511154"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="aef2f-104">Win32 Tpm 類別的 IsOwned 方法 \_</span><span class="sxs-lookup"><span data-stu-id="aef2f-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="aef2f-105">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsOwned** 方法會指出裝置是否有擁有者。</span><span class="sxs-lookup"><span data-stu-id="aef2f-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="aef2f-106">[**TakeOwnership**](takeownership-win32-tpm.md)方法會變更這個值。</span><span class="sxs-lookup"><span data-stu-id="aef2f-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef2f-107">語法</span><span class="sxs-lookup"><span data-stu-id="aef2f-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="aef2f-108">參數</span><span class="sxs-lookup"><span data-stu-id="aef2f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef2f-109">*IsOwned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aef2f-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aef2f-110">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="aef2f-110">Type: **boolean**</span></span>

<span data-ttu-id="aef2f-111">若 **為 true**，表示裝置具有擁有者。</span><span class="sxs-lookup"><span data-stu-id="aef2f-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef2f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="aef2f-112">Return value</span></span>

<span data-ttu-id="aef2f-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="aef2f-113">Type: **uint32**</span></span>

<span data-ttu-id="aef2f-114">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="aef2f-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="aef2f-115">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="aef2f-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="aef2f-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="aef2f-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="aef2f-117">Description</span><span class="sxs-lookup"><span data-stu-id="aef2f-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="aef2f-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="aef2f-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="aef2f-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="aef2f-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aef2f-120">備註</span><span class="sxs-lookup"><span data-stu-id="aef2f-120">Remarks</span></span>

<span data-ttu-id="aef2f-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="aef2f-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="aef2f-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="aef2f-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="aef2f-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="aef2f-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="aef2f-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="aef2f-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aef2f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="aef2f-125">Requirements</span></span>



| <span data-ttu-id="aef2f-126">需求</span><span class="sxs-lookup"><span data-stu-id="aef2f-126">Requirement</span></span> | <span data-ttu-id="aef2f-127">值</span><span class="sxs-lookup"><span data-stu-id="aef2f-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef2f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aef2f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="aef2f-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aef2f-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="aef2f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aef2f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="aef2f-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aef2f-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="aef2f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="aef2f-132">Namespace</span></span><br/>                | <span data-ttu-id="aef2f-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="aef2f-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="aef2f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="aef2f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef2f-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="aef2f-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef2f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="aef2f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef2f-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aef2f-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aef2f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aef2f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef2f-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="aef2f-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

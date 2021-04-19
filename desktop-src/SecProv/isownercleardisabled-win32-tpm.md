---
description: Win32 Tpm 類別的 IsOwnerClearDisabled 方法 \_ 會指出裝置擁有者是否受到限制而無法清除裝置。
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Win32_Tpm 類別的 IsOwnerClearDisabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979940"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="9fa99-103">Win32 Tpm 類別的 IsOwnerClearDisabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9fa99-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9fa99-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsOwnerClearDisabled** 方法會指出裝置擁有者是否受到限制而無法清除裝置。</span><span class="sxs-lookup"><span data-stu-id="9fa99-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fa99-105">語法</span><span class="sxs-lookup"><span data-stu-id="9fa99-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="9fa99-106">參數</span><span class="sxs-lookup"><span data-stu-id="9fa99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fa99-107">*IsOwnerClearDisabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9fa99-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9fa99-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="9fa99-108">Type: **boolean**</span></span>

<span data-ttu-id="9fa99-109">若 **為 true**，則裝置擁有者無法清除裝置。</span><span class="sxs-lookup"><span data-stu-id="9fa99-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="9fa99-110">只有實際存在的使用者可以清除裝置。</span><span class="sxs-lookup"><span data-stu-id="9fa99-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="9fa99-111">如果 **為 false**，則裝置擁有者可以清除裝置。</span><span class="sxs-lookup"><span data-stu-id="9fa99-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fa99-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fa99-112">Return value</span></span>

<span data-ttu-id="9fa99-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9fa99-113">Type: **uint32**</span></span>

<span data-ttu-id="9fa99-114">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fa99-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9fa99-115">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="9fa99-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="9fa99-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9fa99-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="9fa99-117">Description</span><span class="sxs-lookup"><span data-stu-id="9fa99-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="9fa99-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9fa99-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="9fa99-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="9fa99-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9fa99-120">備註</span><span class="sxs-lookup"><span data-stu-id="9fa99-120">Remarks</span></span>

<span data-ttu-id="9fa99-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9fa99-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9fa99-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9fa99-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9fa99-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9fa99-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9fa99-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="9fa99-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fa99-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="9fa99-125">Requirements</span></span>



| <span data-ttu-id="9fa99-126">需求</span><span class="sxs-lookup"><span data-stu-id="9fa99-126">Requirement</span></span> | <span data-ttu-id="9fa99-127">值</span><span class="sxs-lookup"><span data-stu-id="9fa99-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa99-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9fa99-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fa99-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fa99-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9fa99-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9fa99-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fa99-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9fa99-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9fa99-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="9fa99-132">Namespace</span></span><br/>                | <span data-ttu-id="9fa99-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="9fa99-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9fa99-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9fa99-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fa99-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fa99-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fa99-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9fa99-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fa99-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fa99-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa99-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9fa99-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa99-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="9fa99-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

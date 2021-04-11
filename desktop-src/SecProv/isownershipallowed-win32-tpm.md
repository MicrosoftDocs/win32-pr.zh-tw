---
description: Win32 Tpm 類別的 IsOwnershipAllowed 方法 \_ 會指出是否允許安裝裝置擁有者的能力。
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Win32_Tpm 類別的 IsOwnershipAllowed 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191255"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="4189f-103">Win32 Tpm 類別的 IsOwnershipAllowed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4189f-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="4189f-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsOwnershipAllowed** 方法會指出是否允許安裝裝置擁有者的能力。</span><span class="sxs-lookup"><span data-stu-id="4189f-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="4189f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4189f-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="4189f-106">參數</span><span class="sxs-lookup"><span data-stu-id="4189f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4189f-107">*IsOwnershipAllowed* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4189f-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4189f-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="4189f-108">Type: **boolean**</span></span>

<span data-ttu-id="4189f-109">若為 **true**，則允許安裝裝置擁有者的能力。</span><span class="sxs-lookup"><span data-stu-id="4189f-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="4189f-110">如果 **為 false**，則方法 [**TakeOwnership**](takeownership-win32-tpm.md) 將無法安裝裝置的擁有者。</span><span class="sxs-lookup"><span data-stu-id="4189f-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="4189f-111">您可以使用 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法來變更這個值。</span><span class="sxs-lookup"><span data-stu-id="4189f-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="4189f-112">執行 [**Clear**](clear-win32-tpm.md)方法之後，此值會重設為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="4189f-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4189f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4189f-113">Return value</span></span>

<span data-ttu-id="4189f-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4189f-114">Type: **uint32**</span></span>

<span data-ttu-id="4189f-115">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="4189f-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="4189f-116">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="4189f-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="4189f-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4189f-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="4189f-118">Description</span><span class="sxs-lookup"><span data-stu-id="4189f-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="4189f-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="4189f-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4189f-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4189f-121">備註</span><span class="sxs-lookup"><span data-stu-id="4189f-121">Remarks</span></span>

<span data-ttu-id="4189f-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="4189f-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4189f-123">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4189f-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4189f-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="4189f-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4189f-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="4189f-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4189f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="4189f-126">Requirements</span></span>



| <span data-ttu-id="4189f-127">需求</span><span class="sxs-lookup"><span data-stu-id="4189f-127">Requirement</span></span> | <span data-ttu-id="4189f-128">值</span><span class="sxs-lookup"><span data-stu-id="4189f-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4189f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4189f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4189f-130">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4189f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4189f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4189f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4189f-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4189f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4189f-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="4189f-133">Namespace</span></span><br/>                | <span data-ttu-id="4189f-134">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="4189f-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="4189f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="4189f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4189f-136"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="4189f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4189f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4189f-138"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4189f-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4189f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4189f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4189f-140">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="4189f-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

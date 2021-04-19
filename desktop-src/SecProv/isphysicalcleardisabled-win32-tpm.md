---
description: Win32 Tpm 類別的 IsPhysicalClearDisabled 方法 \_ 會指出只有裝置擁有者才能清除裝置。
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Win32_Tpm 類別的 IsPhysicalClearDisabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980412"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="20258-103">Win32 Tpm 類別的 IsPhysicalClearDisabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="20258-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="20258-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsPhysicalClearDisabled** 方法會指出只有裝置擁有者才能清除裝置。</span><span class="sxs-lookup"><span data-stu-id="20258-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="20258-105">語法</span><span class="sxs-lookup"><span data-stu-id="20258-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="20258-106">參數</span><span class="sxs-lookup"><span data-stu-id="20258-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20258-107">*IsPhysicalClearDisabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="20258-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20258-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="20258-108">Type: **boolean**</span></span>

<span data-ttu-id="20258-109">若 **為 true**，則只有裝置擁有者能夠清除裝置。</span><span class="sxs-lookup"><span data-stu-id="20258-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20258-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="20258-110">Return value</span></span>

<span data-ttu-id="20258-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="20258-111">Type: **uint32**</span></span>

<span data-ttu-id="20258-112">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="20258-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="20258-113">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="20258-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="20258-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="20258-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="20258-115">Description</span><span class="sxs-lookup"><span data-stu-id="20258-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="20258-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="20258-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="20258-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="20258-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="20258-118">備註</span><span class="sxs-lookup"><span data-stu-id="20258-118">Remarks</span></span>

<span data-ttu-id="20258-119">在每個啟動週期開始時，此值會重設為 **false** 。</span><span class="sxs-lookup"><span data-stu-id="20258-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="20258-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="20258-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20258-121">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="20258-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="20258-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="20258-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20258-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="20258-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20258-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="20258-124">Requirements</span></span>



| <span data-ttu-id="20258-125">需求</span><span class="sxs-lookup"><span data-stu-id="20258-125">Requirement</span></span> | <span data-ttu-id="20258-126">值</span><span class="sxs-lookup"><span data-stu-id="20258-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="20258-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20258-127">Minimum supported client</span></span><br/> | <span data-ttu-id="20258-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20258-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="20258-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20258-129">Minimum supported server</span></span><br/> | <span data-ttu-id="20258-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20258-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="20258-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="20258-131">Namespace</span></span><br/>                | <span data-ttu-id="20258-132">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="20258-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="20258-133">MOF</span><span class="sxs-lookup"><span data-stu-id="20258-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20258-134"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="20258-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="20258-135">DLL</span><span class="sxs-lookup"><span data-stu-id="20258-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20258-136"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20258-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20258-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20258-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20258-138">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="20258-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

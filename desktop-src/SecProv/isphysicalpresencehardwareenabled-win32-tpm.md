---
description: Win32 Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法會 \_ 指出是否可以使用硬體信號來設定平臺上的實體存在。
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Win32_Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386141"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="93a18-103">Win32 Tpm 類別的 IsPhysicalPresenceHardwareEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="93a18-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="93a18-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsPhysicalPresenceHardwareEnabled** 方法會指出是否可以使用硬體信號來設定平臺上的實體存在。</span><span class="sxs-lookup"><span data-stu-id="93a18-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="93a18-105">此值是由平臺製造商根據平臺設計來設定。</span><span class="sxs-lookup"><span data-stu-id="93a18-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="93a18-106">平臺製造商提供的檔可能會提供其他資訊。</span><span class="sxs-lookup"><span data-stu-id="93a18-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="93a18-107">語法</span><span class="sxs-lookup"><span data-stu-id="93a18-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="93a18-108">參數</span><span class="sxs-lookup"><span data-stu-id="93a18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93a18-109">*IsPhysicalPresenceHardwareEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93a18-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93a18-110">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="93a18-110">Type: **boolean**</span></span>

<span data-ttu-id="93a18-111">若 **為 true**，則平臺上的實體存在可以使用硬體信號來設定。</span><span class="sxs-lookup"><span data-stu-id="93a18-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93a18-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="93a18-112">Return value</span></span>

<span data-ttu-id="93a18-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93a18-113">Type: **uint32**</span></span>

<span data-ttu-id="93a18-114">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="93a18-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="93a18-115">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="93a18-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="93a18-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="93a18-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="93a18-117">Description</span><span class="sxs-lookup"><span data-stu-id="93a18-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="93a18-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="93a18-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="93a18-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="93a18-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93a18-120">備註</span><span class="sxs-lookup"><span data-stu-id="93a18-120">Remarks</span></span>

<span data-ttu-id="93a18-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="93a18-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93a18-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="93a18-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="93a18-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="93a18-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93a18-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="93a18-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93a18-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="93a18-125">Requirements</span></span>



| <span data-ttu-id="93a18-126">需求</span><span class="sxs-lookup"><span data-stu-id="93a18-126">Requirement</span></span> | <span data-ttu-id="93a18-127">值</span><span class="sxs-lookup"><span data-stu-id="93a18-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="93a18-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93a18-128">Minimum supported client</span></span><br/> | <span data-ttu-id="93a18-129">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a18-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="93a18-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93a18-130">Minimum supported server</span></span><br/> | <span data-ttu-id="93a18-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93a18-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="93a18-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="93a18-132">Namespace</span></span><br/>                | <span data-ttu-id="93a18-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="93a18-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="93a18-134">MOF</span><span class="sxs-lookup"><span data-stu-id="93a18-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93a18-135"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="93a18-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="93a18-136">DLL</span><span class="sxs-lookup"><span data-stu-id="93a18-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93a18-137"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93a18-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93a18-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93a18-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93a18-139">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="93a18-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

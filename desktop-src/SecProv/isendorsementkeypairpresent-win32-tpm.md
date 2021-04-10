---
description: Win32 Tpm 類別的 IsEndorsementKeyPairPresent 方法 \_ 指出簽署金鑰組是否存在於裝置上。
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Win32_Tpm 類別的 IsEndorsementKeyPairPresent 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115872"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a><span data-ttu-id="7056e-103">Win32 Tpm 類別的 IsEndorsementKeyPairPresent 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7056e-103">IsEndorsementKeyPairPresent method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7056e-104">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **IsEndorsementKeyPairPresent** 方法指出簽署金鑰組是否存在於裝置上。</span><span class="sxs-lookup"><span data-stu-id="7056e-104">The **IsEndorsementKeyPairPresent** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the endorsement key pair exists on the device.</span></span> <span data-ttu-id="7056e-105">必須要有簽署金鑰組，才可擁有裝置。</span><span class="sxs-lookup"><span data-stu-id="7056e-105">The endorsement key pair is required before the device can be owned.</span></span> <span data-ttu-id="7056e-106">[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)方法可以建立這個金鑰組。</span><span class="sxs-lookup"><span data-stu-id="7056e-106">This key pair can be created by the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span>

<span data-ttu-id="7056e-107">必須啟用並啟用裝置，此方法才能成功。</span><span class="sxs-lookup"><span data-stu-id="7056e-107">The device must be enabled and activated for this method to succeed.</span></span> <span data-ttu-id="7056e-108">若要啟用和啟用無人擁有的裝置，請參閱 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7056e-108">To enable and activate an unowned device, see the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7056e-109">語法</span><span class="sxs-lookup"><span data-stu-id="7056e-109">Syntax</span></span>


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a><span data-ttu-id="7056e-110">參數</span><span class="sxs-lookup"><span data-stu-id="7056e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7056e-111">*IsEndorsementKeyPairPresent* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7056e-111">*IsEndorsementKeyPairPresent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7056e-112">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="7056e-112">Type: **boolean**</span></span>

<span data-ttu-id="7056e-113">若 **為 true**，表示簽署金鑰組存在於裝置上。</span><span class="sxs-lookup"><span data-stu-id="7056e-113">If **true**, the endorsement key pair exists on the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7056e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7056e-114">Return value</span></span>

<span data-ttu-id="7056e-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7056e-115">Type: **uint32**</span></span>

<span data-ttu-id="7056e-116">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7056e-116">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7056e-117">常見的傳回碼如下所示。</span><span class="sxs-lookup"><span data-stu-id="7056e-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="7056e-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7056e-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="7056e-119">Description</span><span class="sxs-lookup"><span data-stu-id="7056e-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="7056e-120"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7056e-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="7056e-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="7056e-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7056e-122">備註</span><span class="sxs-lookup"><span data-stu-id="7056e-122">Remarks</span></span>

<span data-ttu-id="7056e-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7056e-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7056e-124">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7056e-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7056e-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7056e-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7056e-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="7056e-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7056e-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="7056e-127">Requirements</span></span>



| <span data-ttu-id="7056e-128">需求</span><span class="sxs-lookup"><span data-stu-id="7056e-128">Requirement</span></span> | <span data-ttu-id="7056e-129">值</span><span class="sxs-lookup"><span data-stu-id="7056e-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7056e-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7056e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7056e-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7056e-131">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7056e-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7056e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7056e-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7056e-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7056e-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="7056e-134">Namespace</span></span><br/>                | <span data-ttu-id="7056e-135">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="7056e-135">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7056e-136">MOF</span><span class="sxs-lookup"><span data-stu-id="7056e-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7056e-137"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="7056e-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7056e-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7056e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7056e-139"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7056e-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7056e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7056e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7056e-141">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="7056e-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7056e-142">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="7056e-142">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7056e-143">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="7056e-143">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 

---
description: 停用或暫停與此磁片區相關聯的所有金鑰保護裝置。
ms.assetid: 19eed858-a116-4ec8-937a-2eea7aadbdc6
title: Win32_EncryptableVolume 類別的 DisableKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1de392c50f6665d793883582e2679cd502efbe37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983663"
---
# <a name="disablekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e1b44-103">Win32 EncryptableVolume 類別的 DisableKeyProtectors 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e1b44-103">DisableKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e1b44-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DisableKeyProtectors** 方法會停用或暫停與此磁片區相關聯的所有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="e1b44-104">The **DisableKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class disables or suspends all key protectors associated with this volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b44-105">語法</span><span class="sxs-lookup"><span data-stu-id="e1b44-105">Syntax</span></span>


```mof
uint32 DisableKeyProtectors(
  [in, optional] uint32 DisableCount
);
```



## <a name="parameters"></a><span data-ttu-id="e1b44-106">參數</span><span class="sxs-lookup"><span data-stu-id="e1b44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1b44-107">*DisableCount* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="e1b44-107">*DisableCount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e1b44-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e1b44-108">Type: **uint32**</span></span>

<span data-ttu-id="e1b44-109">整數，指定將停用金鑰保護裝置的重新開機次數。</span><span class="sxs-lookup"><span data-stu-id="e1b44-109">Integer that specifies the number of reboots for which the key protectors will be disabled.</span></span> <span data-ttu-id="e1b44-110">此參數僅適用于 OS 磁片區。</span><span class="sxs-lookup"><span data-stu-id="e1b44-110">This parameter is only available on OS volumes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1b44-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1b44-111">Return value</span></span>

<span data-ttu-id="e1b44-112">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e1b44-112">Type: **uint32**</span></span>

<span data-ttu-id="e1b44-113">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e1b44-113">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e1b44-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e1b44-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="e1b44-115">Description</span><span class="sxs-lookup"><span data-stu-id="e1b44-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e1b44-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b44-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="e1b44-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="e1b44-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="e1b44-118"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b44-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="e1b44-119">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="e1b44-119">The volume is locked.</span></span><br/>      |



 

## <a name="security-considerations"></a><span data-ttu-id="e1b44-120">安全性考量</span><span class="sxs-lookup"><span data-stu-id="e1b44-120">Security Considerations</span></span>

<span data-ttu-id="e1b44-121">這個方法會在硬碟上以純文字公開磁片區的加密金鑰，並關閉任何磁片區保護。</span><span class="sxs-lookup"><span data-stu-id="e1b44-121">This method exposes the volume's encryption key in the clear on the hard disk, turning off any volume protection.</span></span> <span data-ttu-id="e1b44-122">我們建議您不要以純文字格式輸入任何密碼或加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="e1b44-122">We recommend against having any password or encryption key in plaintext.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1b44-123">備註</span><span class="sxs-lookup"><span data-stu-id="e1b44-123">Remarks</span></span>

<span data-ttu-id="e1b44-124">即使已停用或暫停金鑰保護裝置，也可以新增金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="e1b44-124">New key protectors can be added even when key protectors are disabled or suspended.</span></span> <span data-ttu-id="e1b44-125">除非呼叫 [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) ，否則這些金鑰保護裝置將維持停用狀態。</span><span class="sxs-lookup"><span data-stu-id="e1b44-125">These key protectors will remain disabled unless [**EnableKeyProtectors**](enablekeyprotectors-win32-encryptablevolume.md) is called.</span></span>

<span data-ttu-id="e1b44-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e1b44-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e1b44-127">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e1b44-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e1b44-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e1b44-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e1b44-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="e1b44-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1b44-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1b44-130">Requirements</span></span>



| <span data-ttu-id="e1b44-131">需求</span><span class="sxs-lookup"><span data-stu-id="e1b44-131">Requirement</span></span> | <span data-ttu-id="e1b44-132">值</span><span class="sxs-lookup"><span data-stu-id="e1b44-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b44-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1b44-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e1b44-134">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1b44-134">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e1b44-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1b44-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e1b44-136">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1b44-136">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e1b44-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="e1b44-137">Namespace</span></span><br/>                | <span data-ttu-id="e1b44-138">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="e1b44-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e1b44-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e1b44-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1b44-140"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1b44-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b44-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1b44-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b44-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="e1b44-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="e1b44-143">**EnableKeyProtectors**</span><span class="sxs-lookup"><span data-stu-id="e1b44-143">**EnableKeyProtectors**</span></span>](enablekeyprotectors-win32-encryptablevolume.md)
</dt> </dl>

 

 

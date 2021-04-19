---
description: 指出是否可從 Windows 存取磁片區的內容。
ms.assetid: 54b2a41b-11c6-40ec-97fa-74996c15554e
title: Win32_EncryptableVolume 類別的 GetLockStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetLockStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3e81f77c37904f26e87f22b8e2b3b88763fe86cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970787"
---
# <a name="getlockstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="a4081-103">Win32 EncryptableVolume 類別的 GetLockStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a4081-103">GetLockStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="a4081-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetLockStatus** 方法會指出是否可以從 Windows 存取磁片區的內容。</span><span class="sxs-lookup"><span data-stu-id="a4081-104">The **GetLockStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the contents of the volume are accessible from Windows.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4081-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4081-105">Syntax</span></span>


```mof
uint32 GetLockStatus(
  [out] uint32 LockStatus
);
```



## <a name="parameters"></a><span data-ttu-id="a4081-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4081-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4081-107">*LockStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a4081-107">*LockStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4081-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4081-108">Type: **uint32**</span></span>

<span data-ttu-id="a4081-109">指定是否可從 Windows 存取磁片區的內容。</span><span class="sxs-lookup"><span data-stu-id="a4081-109">Specifies whether the contents of the volume are accessible from Windows.</span></span>



| <span data-ttu-id="a4081-110">值</span><span class="sxs-lookup"><span data-stu-id="a4081-110">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="a4081-111">意義</span><span class="sxs-lookup"><span data-stu-id="a4081-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unlocked"></span><span id="unlocked"></span><span id="UNLOCKED"></span><dl> <span data-ttu-id="a4081-112">已 <dt>**解除鎖定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4081-112"><dt>**Unlocked**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="a4081-113">針對標準 HDD：</span><span class="sxs-lookup"><span data-stu-id="a4081-113">For a standard HDD:</span></span><br/> <span data-ttu-id="a4081-114">可以存取磁片區的完整內容。</span><span class="sxs-lookup"><span data-stu-id="a4081-114">The full contents of the volume are accessible.</span></span> <span data-ttu-id="a4081-115">已解除鎖定的磁片區可能已完全解密，或有可在磁片上清除的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4081-115">An unlocked volume is either fully decrypted or has the encryption key available in the clear on disk.</span></span> <span data-ttu-id="a4081-116">包含目前正在執行之作業系統的磁片區 (例如，執行中的 Windows 磁片區) 一律可供存取且無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="a4081-116">The volume containing the current running operating system (for example, the running Windows volume) is always accessible and cannot be locked.</span></span><br/> <span data-ttu-id="a4081-117">針對 EHDD：</span><span class="sxs-lookup"><span data-stu-id="a4081-117">For an EHDD:</span></span><br/> <span data-ttu-id="a4081-118">頻外永久解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="a4081-118">The band is perpetually unlocked.</span></span><br/> |
| <span id="Locked"></span><span id="locked"></span><span id="LOCKED"></span><dl> <span data-ttu-id="a4081-119"><dt>**鎖定**</dt>的 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a4081-119"><dt>**Locked**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="a4081-120">針對標準 HDD：</span><span class="sxs-lookup"><span data-stu-id="a4081-120">For a standard HDD:</span></span><br/> <span data-ttu-id="a4081-121">無法存取磁片區的所有或部分內容。</span><span class="sxs-lookup"><span data-stu-id="a4081-121">All or a portion of the contents of the volume are not accessible.</span></span> <span data-ttu-id="a4081-122">鎖定的磁片區必須部分或完整加密，且不能在磁片上的純文字中提供加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a4081-122">A locked volume must be partially or fully encrypted and must not have the encryption key available in the clear on disk.</span></span><br/> <span data-ttu-id="a4081-123">針對 EHDD：</span><span class="sxs-lookup"><span data-stu-id="a4081-123">For an EHDD:</span></span><br/> <span data-ttu-id="a4081-124">頻外已解除鎖定或鎖定。</span><span class="sxs-lookup"><span data-stu-id="a4081-124">The band is unlocked or locked.</span></span><br/>                                                                                                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4081-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4081-125">Return value</span></span>

<span data-ttu-id="a4081-126">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a4081-126">Type: **uint32**</span></span>

<span data-ttu-id="a4081-127">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a4081-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="a4081-128">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a4081-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="a4081-129">Description</span><span class="sxs-lookup"><span data-stu-id="a4081-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a4081-130"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a4081-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="a4081-131">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="a4081-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4081-132">備註</span><span class="sxs-lookup"><span data-stu-id="a4081-132">Remarks</span></span>

<span data-ttu-id="a4081-133">使用 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 和 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 來取得磁片區內容的存取權。</span><span class="sxs-lookup"><span data-stu-id="a4081-133">Use the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) and [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) to get access to the volume contents.</span></span> <span data-ttu-id="a4081-134">使用 [**鎖定**](lock-win32-encryptablevolume.md) 方法來放棄存取磁片區內容。</span><span class="sxs-lookup"><span data-stu-id="a4081-134">Use the [**Lock**](lock-win32-encryptablevolume.md) method to relinquish access to volume contents.</span></span>

<span data-ttu-id="a4081-135">包含目前執行之作業系統的磁片區永遠可供存取且無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="a4081-135">The volume that contains the currently running operating system is always accessible and cannot be locked.</span></span>

<span data-ttu-id="a4081-136">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a4081-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a4081-137">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a4081-137">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a4081-138">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a4081-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a4081-139">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="a4081-139">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a4081-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4081-140">Requirements</span></span>



| <span data-ttu-id="a4081-141">需求</span><span class="sxs-lookup"><span data-stu-id="a4081-141">Requirement</span></span> | <span data-ttu-id="a4081-142">值</span><span class="sxs-lookup"><span data-stu-id="a4081-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4081-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4081-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a4081-144">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4081-144">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a4081-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4081-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a4081-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4081-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4081-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="a4081-147">Namespace</span></span><br/>                | <span data-ttu-id="a4081-148">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="a4081-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="a4081-149">MOF</span><span class="sxs-lookup"><span data-stu-id="a4081-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4081-150"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4081-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4081-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4081-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4081-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="a4081-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

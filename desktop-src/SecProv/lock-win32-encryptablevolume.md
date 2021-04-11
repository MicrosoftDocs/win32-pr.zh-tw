---
description: 卸下磁片區，並從系統記憶體移除磁片區的加密金鑰。
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Win32_EncryptableVolume 類別的鎖定方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847875"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="95c1c-103">Win32 EncryptableVolume 類別的 Lock 方法 \_</span><span class="sxs-lookup"><span data-stu-id="95c1c-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="95c1c-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **鎖定** 方法會卸載磁片區，並從系統記憶體中移除磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="95c1c-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="95c1c-105">磁片區的內容會一直變成無法存取，直到 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 方法或 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 方法解除鎖定為止。</span><span class="sxs-lookup"><span data-stu-id="95c1c-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="95c1c-106">無法針對目前正在執行的作業系統磁片區成功執行此方法。</span><span class="sxs-lookup"><span data-stu-id="95c1c-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="95c1c-107">如果光碟支援硬體加密，則會將此波段設定為 [已鎖定]。</span><span class="sxs-lookup"><span data-stu-id="95c1c-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="95c1c-108">語法</span><span class="sxs-lookup"><span data-stu-id="95c1c-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="95c1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="95c1c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95c1c-110">*ForceDismount* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="95c1c-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="95c1c-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="95c1c-111">Type: **boolean**</span></span>

<span data-ttu-id="95c1c-112">若 **為 true** ，則會強制卸載磁片。</span><span class="sxs-lookup"><span data-stu-id="95c1c-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95c1c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="95c1c-113">Return value</span></span>

<span data-ttu-id="95c1c-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="95c1c-114">Type: **uint32**</span></span>

<span data-ttu-id="95c1c-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="95c1c-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="95c1c-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="95c1c-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="95c1c-117">Description</span><span class="sxs-lookup"><span data-stu-id="95c1c-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="95c1c-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="95c1c-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="95c1c-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="95c1c-120"><dt>**E \_\_拒絕存取**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="95c1c-121">應用程式正在存取此磁片區。</span><span class="sxs-lookup"><span data-stu-id="95c1c-121">Applications are accessing this volume.</span></span> <span data-ttu-id="95c1c-122">如果所有存取都是非獨佔的，則將 *ForceDismount* 參數指定為 true，可讓方法順利執行。</span><span class="sxs-lookup"><span data-stu-id="95c1c-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="95c1c-123"><dt>**FVE \_E \_ 未 \_ 加密**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="95c1c-124">磁片區已完全解密且無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="95c1c-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="95c1c-125"><dt>**FVE \_E \_ 保護 \_ 停用**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="95c1c-126">磁片區的加密金鑰會在磁片上以純文字方式提供，使磁片區無法鎖定。</span><span class="sxs-lookup"><span data-stu-id="95c1c-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="95c1c-127"><dt>**FVE \_E \_ 修復 \_ 金鑰 \_ 需要**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="95c1c-128">磁片區沒有將磁片區解除鎖定所需之類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="95c1c-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="95c1c-129">備註</span><span class="sxs-lookup"><span data-stu-id="95c1c-129">Remarks</span></span>

<span data-ttu-id="95c1c-130">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="95c1c-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="95c1c-131">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="95c1c-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="95c1c-132">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="95c1c-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="95c1c-133">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="95c1c-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95c1c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="95c1c-134">Requirements</span></span>



| <span data-ttu-id="95c1c-135">需求</span><span class="sxs-lookup"><span data-stu-id="95c1c-135">Requirement</span></span> | <span data-ttu-id="95c1c-136">值</span><span class="sxs-lookup"><span data-stu-id="95c1c-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95c1c-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95c1c-137">Minimum supported client</span></span><br/> | <span data-ttu-id="95c1c-138">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95c1c-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="95c1c-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95c1c-139">Minimum supported server</span></span><br/> | <span data-ttu-id="95c1c-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="95c1c-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="95c1c-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="95c1c-141">Namespace</span></span><br/>                | <span data-ttu-id="95c1c-142">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="95c1c-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="95c1c-143">MOF</span><span class="sxs-lookup"><span data-stu-id="95c1c-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95c1c-144"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="95c1c-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95c1c-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95c1c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c1c-146">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="95c1c-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 移除儲存在目前正在執行的作業系統磁片區上的所有外部金鑰和相關資訊，以用來自動解除鎖定資料磁片區。
ms.assetid: a5fef793-0634-493d-b62d-cb842844b1e8
title: Win32_EncryptableVolume 類別的 ClearAllAutoUnlockKeys 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ClearAllAutoUnlockKeys
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b7f7e68891865893c1444a2c5de2370799b74426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974022"
---
# <a name="clearallautounlockkeys-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="dfe08-103">Win32 EncryptableVolume 類別的 ClearAllAutoUnlockKeys 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dfe08-103">ClearAllAutoUnlockKeys method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="dfe08-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ClearAllAutoUnlockKeys** 方法會移除所有儲存在目前執行之作業系統磁片區的外部金鑰和相關資訊，以用來自動解除鎖定資料磁片區。</span><span class="sxs-lookup"><span data-stu-id="dfe08-104">The **ClearAllAutoUnlockKeys** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes all external keys and related information saved onto the currently running operating system volume that are used to automatically unlock data volumes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfe08-105">語法</span><span class="sxs-lookup"><span data-stu-id="dfe08-105">Syntax</span></span>


```mof
uint32 ClearAllAutoUnlockKeys();
```



## <a name="parameters"></a><span data-ttu-id="dfe08-106">參數</span><span class="sxs-lookup"><span data-stu-id="dfe08-106">Parameters</span></span>

<span data-ttu-id="dfe08-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dfe08-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dfe08-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfe08-108">Return value</span></span>

<span data-ttu-id="dfe08-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dfe08-109">Type: **uint32**</span></span>

<span data-ttu-id="dfe08-110">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dfe08-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="dfe08-111">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="dfe08-111">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="dfe08-112">Description</span><span class="sxs-lookup"><span data-stu-id="dfe08-112">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dfe08-113"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe08-113"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="dfe08-114">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="dfe08-114">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="dfe08-115"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe08-115"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="dfe08-116">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="dfe08-116">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="dfe08-117">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="dfe08-117">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="dfe08-118"><dt>**FVE \_E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="dfe08-118"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="dfe08-119">方法只能針對目前正在執行的作業系統磁片區執行。</span><span class="sxs-lookup"><span data-stu-id="dfe08-119">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="dfe08-120">備註</span><span class="sxs-lookup"><span data-stu-id="dfe08-120">Remarks</span></span>

<span data-ttu-id="dfe08-121">**ClearAllAutoUnlockKeys** 與目前正在執行的作業系統相關聯的每個資料磁片區（甚至是目前尚未連線到該電腦的資料磁片區），可達到與執行 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 相同的功能。</span><span class="sxs-lookup"><span data-stu-id="dfe08-121">**ClearAllAutoUnlockKeys** achieves the same functionality as running [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) for every data volume that has ever been associated with the currently running operating system, even data volumes that are not currently connected to the computer.</span></span> <span data-ttu-id="dfe08-122">它也會移除與不再存在之資料磁片區相關聯的任何過時解除鎖定資訊。</span><span class="sxs-lookup"><span data-stu-id="dfe08-122">It also removes any stale unlocking information associated with data volumes that no longer exist.</span></span>

<span data-ttu-id="dfe08-123">在目前執行中的作業系統磁片區上呼叫 [**解密**](decrypt-win32-encryptablevolume.md) 之前，請使用 **ClearAllAutoUnlockKeys** 來確保放置在作業系統登錄中的資訊可自動解除鎖定資料磁片區，而無法在磁片上清除。</span><span class="sxs-lookup"><span data-stu-id="dfe08-123">Before calling [**Decrypt**](decrypt-win32-encryptablevolume.md) on the currently running operating system volume, use **ClearAllAutoUnlockKeys** to ensure that information placed in the operating system registry to automatically unlock data volumes is not accessible in the clear on disk.</span></span>

<span data-ttu-id="dfe08-124">順利執行 **ClearAllAutoUnlockKeys** 之後，就可以使用 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 或 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 方法來解除鎖定這部電腦上的所有資料磁片區。</span><span class="sxs-lookup"><span data-stu-id="dfe08-124">After **ClearAllAutoUnlockKeys** runs successfully, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) can be used to unlock all data volumes on this computer.</span></span> <span data-ttu-id="dfe08-125">使用 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) 重新啟用資料磁片區的自動解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="dfe08-125">Use [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) to re-enable automatic unlocking of a data volume.</span></span>

<span data-ttu-id="dfe08-126">如果未傳回任何其他錯誤， **ClearAllAutoUnlockKeys** 會從登錄中移除任何磁片區保護程式識別碼，以及用來自動解除鎖定目前正在執行之作業系統磁片區的任何資料磁片區的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="dfe08-126">If no other errors are returned, **ClearAllAutoUnlockKeys** removes from the registry any volume protector IDs and external keys used to automatically unlock any data volume that has ever been associated with the currently running operating system volume.</span></span>

<span data-ttu-id="dfe08-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="dfe08-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dfe08-128">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dfe08-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dfe08-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="dfe08-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dfe08-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="dfe08-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfe08-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfe08-131">Requirements</span></span>



| <span data-ttu-id="dfe08-132">需求</span><span class="sxs-lookup"><span data-stu-id="dfe08-132">Requirement</span></span> | <span data-ttu-id="dfe08-133">值</span><span class="sxs-lookup"><span data-stu-id="dfe08-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe08-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfe08-134">Minimum supported client</span></span><br/> | <span data-ttu-id="dfe08-135">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfe08-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dfe08-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfe08-136">Minimum supported server</span></span><br/> | <span data-ttu-id="dfe08-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dfe08-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dfe08-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfe08-138">Namespace</span></span><br/>                | <span data-ttu-id="dfe08-139">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="dfe08-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="dfe08-140">MOF</span><span class="sxs-lookup"><span data-stu-id="dfe08-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfe08-141"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfe08-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfe08-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfe08-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfe08-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="dfe08-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

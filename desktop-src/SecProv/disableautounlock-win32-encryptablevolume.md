---
description: 移除儲存在目前正在執行之作業系統磁片區上的外部金鑰。
ms.assetid: a8c4bb3b-6566-4173-b550-e89740f1cba6
title: Win32_EncryptableVolume 類別的 DisableAutoUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DisableAutoUnlock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6dd4e11e2ff4906627c2d790987500062136d56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849449"
---
# <a name="disableautounlock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="eef7d-103">Win32 EncryptableVolume 類別的 DisableAutoUnlock 方法 \_</span><span class="sxs-lookup"><span data-stu-id="eef7d-103">DisableAutoUnlock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="eef7d-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DisableAutoUnlock** 方法會移除儲存在目前正在執行之作業系統磁片區上的外部金鑰，如此一來，當資料磁片區掛接時就不會自動解除鎖定，例如，當卸載式記憶體裝置連接到電腦時。</span><span class="sxs-lookup"><span data-stu-id="eef7d-104">The **DisableAutoUnlock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class removes the external key saved onto the currently running operating system volume so that a data volume is not automatically unlocked when it is mounted, such as when removable memory devices are connected to the computer.</span></span>

<span data-ttu-id="eef7d-105">如果已停用或暫停自動解除鎖定，則必須使用 [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) 或 [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) 方法來解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="eef7d-105">If automatic unlocking is disabled or suspended, the methods [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) or [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) must be used to unlock the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="eef7d-106">語法</span><span class="sxs-lookup"><span data-stu-id="eef7d-106">Syntax</span></span>


```mof
uint32 DisableAutoUnlock();
```



## <a name="parameters"></a><span data-ttu-id="eef7d-107">參數</span><span class="sxs-lookup"><span data-stu-id="eef7d-107">Parameters</span></span>

<span data-ttu-id="eef7d-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="eef7d-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eef7d-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="eef7d-109">Return value</span></span>

<span data-ttu-id="eef7d-110">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="eef7d-110">Type: **uint32**</span></span>

<span data-ttu-id="eef7d-111">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="eef7d-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="eef7d-112">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="eef7d-112">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="eef7d-113">Description</span><span class="sxs-lookup"><span data-stu-id="eef7d-113">Description</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eef7d-114"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eef7d-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                       | <span data-ttu-id="eef7d-115">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="eef7d-115">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="eef7d-116"><dt> **FVE \_ E \_ 磁片 \_ 區 \_ 未**</dt>系結 <dt>2150694935 (0x80310017)</dt></span><span class="sxs-lookup"><span data-stu-id="eef7d-116"><dt>**FVE\_E\_VOLUME\_NOT\_BOUND** </dt> <dt>2150694935 (0x80310017)</dt></span></span> </dl> | <span data-ttu-id="eef7d-117">磁片區上的自動解除鎖定已停用。</span><span class="sxs-lookup"><span data-stu-id="eef7d-117">Automatic unlocking on the volume is disabled.</span></span><br/>                                   |
| <dl> <span data-ttu-id="eef7d-118"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="eef7d-118"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>      | <span data-ttu-id="eef7d-119">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="eef7d-119">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="eef7d-120">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="eef7d-120">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="eef7d-121"><dt>**FVE \_E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="eef7d-121"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl>   | <span data-ttu-id="eef7d-122">無法針對目前正在執行的作業系統磁片區執行此方法。</span><span class="sxs-lookup"><span data-stu-id="eef7d-122">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="eef7d-123">備註</span><span class="sxs-lookup"><span data-stu-id="eef7d-123">Remarks</span></span>

<span data-ttu-id="eef7d-124">如果未傳回任何錯誤，這個方法會從登錄中移除任何磁片區保護裝置識別碼，以及用來自動解除鎖定磁片區的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="eef7d-124">If no errors are returned, this method removes from the registry any volume protector IDs and external keys used to automatically unlock the volume.</span></span>

<span data-ttu-id="eef7d-125">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="eef7d-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eef7d-126">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="eef7d-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eef7d-127">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="eef7d-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eef7d-128">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="eef7d-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eef7d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="eef7d-129">Requirements</span></span>



| <span data-ttu-id="eef7d-130">需求</span><span class="sxs-lookup"><span data-stu-id="eef7d-130">Requirement</span></span> | <span data-ttu-id="eef7d-131">值</span><span class="sxs-lookup"><span data-stu-id="eef7d-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eef7d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eef7d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="eef7d-133">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eef7d-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="eef7d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eef7d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="eef7d-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eef7d-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eef7d-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="eef7d-136">Namespace</span></span><br/>                | <span data-ttu-id="eef7d-137">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="eef7d-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="eef7d-138">MOF</span><span class="sxs-lookup"><span data-stu-id="eef7d-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eef7d-139"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="eef7d-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eef7d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eef7d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eef7d-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="eef7d-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

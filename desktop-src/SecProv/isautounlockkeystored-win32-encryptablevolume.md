---
description: 指出是否有任何可用來自動解除鎖定資料磁片區的外部金鑰或相關資訊，是否存在於目前正在執行的作業系統磁片區中。
ms.assetid: 37e7fe85-312d-49ff-aa6b-8c76c4fc4bba
title: Win32_EncryptableVolume 類別的 IsAutoUnlockKeyStored 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockKeyStored
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: aedb834bdfd26ce4b348a41b4046c0c4e2c7e260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990373"
---
# <a name="isautounlockkeystored-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b631c-103">Win32 EncryptableVolume 類別的 IsAutoUnlockKeyStored 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b631c-103">IsAutoUnlockKeyStored method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b631c-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsAutoUnlockKeyStored** 方法會指出是否有任何可用來自動解除鎖定資料磁片區的外部金鑰或相關資訊，是否存在於目前正在執行的作業系統磁片區中。</span><span class="sxs-lookup"><span data-stu-id="b631c-104">The **IsAutoUnlockKeyStored** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether any external keys or related information that may be used to automatically unlock data volumes exist in the currently running operating system volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="b631c-105">語法</span><span class="sxs-lookup"><span data-stu-id="b631c-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockKeyStored(
  [out] boolean IsAutoUnlockKeyStored
);
```



## <a name="parameters"></a><span data-ttu-id="b631c-106">參數</span><span class="sxs-lookup"><span data-stu-id="b631c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b631c-107">*IsAutoUnlockKeyStored* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b631c-107">*IsAutoUnlockKeyStored* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b631c-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="b631c-108">Type: **boolean**</span></span>

<span data-ttu-id="b631c-109">如果可用來自動解除鎖定資料磁片區的任何資訊都儲存在目前正在執行的作業系統磁片區的登錄中，則為 **true** 。</span><span class="sxs-lookup"><span data-stu-id="b631c-109">Is **true** if any information that can be used to automatically unlock data volumes is stored in the registry of the currently running operating system volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b631c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="b631c-110">Return value</span></span>

<span data-ttu-id="b631c-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b631c-111">Type: **uint32**</span></span>

<span data-ttu-id="b631c-112">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b631c-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b631c-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b631c-113">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="b631c-114">Description</span><span class="sxs-lookup"><span data-stu-id="b631c-114">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b631c-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b631c-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="b631c-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="b631c-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b631c-117"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b631c-117"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="b631c-118">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b631c-118">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b631c-119">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b631c-119">Add a key protector to enable BitLocker.</span></span> <br/> |
| <dl> <span data-ttu-id="b631c-120"><dt>**FVE \_E \_ NOT \_ OS \_ VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span><span class="sxs-lookup"><span data-stu-id="b631c-120"><dt>**FVE\_E\_NOT\_OS\_VOLUME**</dt> <dt>2150694952 (0x80310028)</dt></span></span> </dl> | <span data-ttu-id="b631c-121">方法只能針對目前正在執行的作業系統磁片區執行。</span><span class="sxs-lookup"><span data-stu-id="b631c-121">The method can only be run for the currently running operating system volume.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b631c-122">備註</span><span class="sxs-lookup"><span data-stu-id="b631c-122">Remarks</span></span>

<span data-ttu-id="b631c-123">使用 [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) 從目前正在執行的作業系統磁片區中移除所有解除鎖定的資訊。</span><span class="sxs-lookup"><span data-stu-id="b631c-123">Use [**ClearAllAutoUnlockKeys**](clearallautounlockkeys-win32-encryptablevolume.md) to remove all unlocking information from the currently running operating system volume.</span></span>

<span data-ttu-id="b631c-124">當目前執行中的作業系統磁片區正在執行時，系統會在針對資料磁片區執行 [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) 時，儲存用來解除鎖定磁片區的資訊。</span><span class="sxs-lookup"><span data-stu-id="b631c-124">Information used to unlock a volume is stored when [**EnableAutoUnlock**](enableautounlock-win32-encryptablevolume.md) is run for a data volume while the currently running operating system volume is running.</span></span>

<span data-ttu-id="b631c-125">**IsAutoUnlockKeyStored** 與 [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) 的不同之處在于，即使已針對目前連線到電腦的所有資料磁片區停用自動解除鎖定，仍可能會有與已中斷連線的資料磁片區或已不存在的資料磁片區相關聯的解除鎖定資訊。</span><span class="sxs-lookup"><span data-stu-id="b631c-125">**IsAutoUnlockKeyStored** differs from [**IsAutoUnlockEnabled**](isautounlockenabled-win32-encryptablevolume.md) in that even if automatic unlocking is disabled for all data volumes currently connected to the computer, there may still be unlocking information associated with disconnected data volumes or data volumes that no longer exist.</span></span>

<span data-ttu-id="b631c-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b631c-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b631c-127">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b631c-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b631c-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b631c-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b631c-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="b631c-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b631c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b631c-130">Requirements</span></span>



| <span data-ttu-id="b631c-131">需求</span><span class="sxs-lookup"><span data-stu-id="b631c-131">Requirement</span></span> | <span data-ttu-id="b631c-132">值</span><span class="sxs-lookup"><span data-stu-id="b631c-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b631c-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b631c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b631c-134">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b631c-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b631c-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b631c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b631c-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b631c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b631c-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="b631c-137">Namespace</span></span><br/>                | <span data-ttu-id="b631c-138">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b631c-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b631c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b631c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b631c-140"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="b631c-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b631c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b631c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b631c-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b631c-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

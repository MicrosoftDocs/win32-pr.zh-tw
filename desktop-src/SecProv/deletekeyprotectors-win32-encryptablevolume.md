---
description: 刪除磁片區的所有金鑰保護裝置。
ms.assetid: 46f61899-87ff-4e86-8409-635117cff4de
title: Win32_EncryptableVolume 類別的 DeleteKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.DeleteKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0195a89884dcd9f9288cab020d9804dcc81b7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981592"
---
# <a name="deletekeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6d581-103">Win32 EncryptableVolume 類別的 DeleteKeyProtectors 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6d581-103">DeleteKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6d581-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **DeleteKeyProtectors** 方法會刪除磁片區的所有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6d581-104">The **DeleteKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class deletes all key protectors for the volume.</span></span>

<span data-ttu-id="6d581-105">如果未加密的磁片區具有金鑰保護裝置，則當 **DeleteKeyProtectors** 執行成功時，磁片區會還原成標準 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="6d581-105">If an unencrypted volume has key protectors, when **DeleteKeyProtectors** is run successfully the volume reverts to a standard NTFS file system.</span></span>

<span data-ttu-id="6d581-106">如果磁片區尚未完整解密，請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再執行 **DeleteKeyProtectors** ，以確保磁片區的加密部分仍然可供存取。</span><span class="sxs-lookup"><span data-stu-id="6d581-106">If the volume is not yet fully decrypted, use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before running **DeleteKeyProtectors** to ensure that encrypted portions of the volume remain accessible.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d581-107">語法</span><span class="sxs-lookup"><span data-stu-id="6d581-107">Syntax</span></span>


```mof
uint32 DeleteKeyProtectors();
```



## <a name="parameters"></a><span data-ttu-id="6d581-108">參數</span><span class="sxs-lookup"><span data-stu-id="6d581-108">Parameters</span></span>

<span data-ttu-id="6d581-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6d581-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d581-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d581-110">Return value</span></span>

<span data-ttu-id="6d581-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6d581-111">Type: **uint32**</span></span>

<span data-ttu-id="6d581-112">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6d581-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6d581-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6d581-113">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="6d581-114">Description</span><span class="sxs-lookup"><span data-stu-id="6d581-114">Description</span></span>                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d581-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6d581-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                          | <span data-ttu-id="6d581-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6d581-116">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6d581-117"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6d581-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>         | <span data-ttu-id="6d581-118">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="6d581-118">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="6d581-119"><dt>**FVE \_\_ \_ 需要 E 鍵**</dt> <dt>2150694941 (0x8031001D)</dt></span><span class="sxs-lookup"><span data-stu-id="6d581-119"><dt>**FVE\_E\_KEY\_REQUIRED**</dt> <dt>2150694941 (0x8031001D)</dt></span></span> </dl>          | <span data-ttu-id="6d581-120">如果啟用金鑰保護裝置，則無法移除部分或完整加密磁片區的最後一個金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6d581-120">The last key protector for a partially or fully encrypted volume cannot be removed if key protectors are enabled.</span></span> <span data-ttu-id="6d581-121">請先使用 [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) 再移除此最後一個金鑰保護裝置，以確保磁片區的加密部分仍然可供存取。</span><span class="sxs-lookup"><span data-stu-id="6d581-121">Use [**DisableKeyProtectors**](disablekeyprotectors-win32-encryptablevolume.md) before removing this last key protector to ensure that encrypted portions of the volume remain accessible.</span></span> <br/> |
| <dl> <span data-ttu-id="6d581-122"><dt>**FVE \_E \_ 磁片 \_ \_**</dt>區系結已在 <dt>2150694943 (0x8031001F)</dt></span><span class="sxs-lookup"><span data-stu-id="6d581-122"><dt>**FVE\_E\_VOLUME\_BOUND\_ALREADY**</dt> <dt>2150694943 (0x8031001F)</dt></span></span> </dl> | <span data-ttu-id="6d581-123">無法刪除金鑰保護裝置，因為其中一個金鑰保護裝置會用來自動解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="6d581-123">Key protectors cannot be deleted because one of them is being used to automatically unlock the volume.</span></span> <br/> <span data-ttu-id="6d581-124">在執行此方法之前，請先使用 [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) 停用自動解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="6d581-124">Use [**DisableAutoUnlock**](disableautounlock-win32-encryptablevolume.md) to disable automatic unlocking before running this method.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="6d581-125">備註</span><span class="sxs-lookup"><span data-stu-id="6d581-125">Remarks</span></span>

<span data-ttu-id="6d581-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6d581-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d581-127">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6d581-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6d581-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6d581-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d581-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="6d581-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d581-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d581-130">Requirements</span></span>



| <span data-ttu-id="6d581-131">需求</span><span class="sxs-lookup"><span data-stu-id="6d581-131">Requirement</span></span> | <span data-ttu-id="6d581-132">值</span><span class="sxs-lookup"><span data-stu-id="6d581-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d581-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d581-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6d581-134">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d581-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6d581-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d581-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6d581-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d581-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6d581-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="6d581-137">Namespace</span></span><br/>                | <span data-ttu-id="6d581-138">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6d581-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6d581-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6d581-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d581-140"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d581-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d581-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d581-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d581-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6d581-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

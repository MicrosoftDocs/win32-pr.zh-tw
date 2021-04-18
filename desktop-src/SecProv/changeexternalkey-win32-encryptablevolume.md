---
description: 變更與加密磁片區相關聯的外部金鑰。
ms.assetid: 14c7e643-f685-40bb-be86-aabc5b883d7e
title: Win32_EncryptableVolume 類別的 ChangeExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangeExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7441666ded1acc2234df84fc98ce6d02a117167d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971527"
---
# <a name="changeexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4c3f1-103">Win32 EncryptableVolume 類別的 ChangeExternalKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4c3f1-103">ChangeExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4c3f1-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangeExternalKey** 方法會變更與加密磁片區相關聯的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-104">The **ChangeExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class changes an external key that is associated with an encrypted volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3f1-105">語法</span><span class="sxs-lookup"><span data-stu-id="4c3f1-105">Syntax</span></span>


```mof
uint32 ChangeExternalKey(
  [in]           string VolumeKeyProtectorID,
  [in, optional] uint8   NewExternalKey[],
  [out]          string NewVolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="4c3f1-106">參數</span><span class="sxs-lookup"><span data-stu-id="4c3f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c3f1-107">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3f1-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-108">Type: **string**</span></span>

<span data-ttu-id="4c3f1-109">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

 <span data-ttu-id="4c3f1-110">*NewExternalKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-110">*NewExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3f1-111">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="4c3f1-112">位元組陣列，指定用來解除鎖定磁片區的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-112">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

</dd> <dt>

<span data-ttu-id="4c3f1-113">*NewVolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-113">*NewVolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c3f1-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-114">Type: **string**</span></span>

<span data-ttu-id="4c3f1-115">更新的唯一字串識別碼，可用來管理加密的磁片區金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-115">An updated unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c3f1-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c3f1-116">Return value</span></span>

<span data-ttu-id="4c3f1-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-117">Type: **uint32**</span></span>

<span data-ttu-id="4c3f1-118">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4c3f1-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4c3f1-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="4c3f1-120">Description</span><span class="sxs-lookup"><span data-stu-id="4c3f1-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4c3f1-121"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="4c3f1-122">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-122">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="4c3f1-123"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                    | <span data-ttu-id="4c3f1-124">*NewExternalKey* 參數不是大小為32的陣列。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-124">The *NewExternalKey* parameter is not an array of size 32.</span></span><br/>                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="4c3f1-125"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-125"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="4c3f1-126">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-126">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="4c3f1-127"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="4c3f1-128">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4c3f1-129">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="4c3f1-130"><dt>**FVE \_E \_ 可 \_**</dt>開機的 CDDVD <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-130"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>          | <span data-ttu-id="4c3f1-131">在這部電腦上找到可開機的 CD/DVD。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-131">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="4c3f1-132">移除 CD/DVD 並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-132">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="4c3f1-133"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="4c3f1-134">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="4c3f1-135"><dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="4c3f1-136">*VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="4c3f1-137">您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4c3f1-138">備註</span><span class="sxs-lookup"><span data-stu-id="4c3f1-138">Remarks</span></span>

<span data-ttu-id="4c3f1-139">這個方法可以用來變更使用外部金鑰之任何金鑰保護裝置的外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="4c3f1-139">This method can be used to change the external key for any key protector that uses an external key.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c3f1-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c3f1-140">Requirements</span></span>



| <span data-ttu-id="4c3f1-141">需求</span><span class="sxs-lookup"><span data-stu-id="4c3f1-141">Requirement</span></span> | <span data-ttu-id="4c3f1-142">值</span><span class="sxs-lookup"><span data-stu-id="4c3f1-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3f1-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c3f1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4c3f1-144">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c3f1-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c3f1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4c3f1-146">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c3f1-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c3f1-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c3f1-147">Namespace</span></span><br/>                | <span data-ttu-id="4c3f1-148">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4c3f1-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4c3f1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4c3f1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c3f1-150"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c3f1-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3f1-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c3f1-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3f1-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4c3f1-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





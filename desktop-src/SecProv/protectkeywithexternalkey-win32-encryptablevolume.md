---
description: 使用256位的外部金鑰保護磁片區的加密金鑰。
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Win32_EncryptableVolume 類別的 ProtectKeyWithExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971371"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ac61c-103">Win32 EncryptableVolume 類別的 ProtectKeyWithExternalKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ac61c-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ac61c-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithExternalKey** 方法會使用256位的外部金鑰保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="ac61c-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="ac61c-105">此外部金鑰可以用來從其他金鑰保護裝置的驗證失敗中復原 (例如 TPM) 。</span><span class="sxs-lookup"><span data-stu-id="ac61c-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="ac61c-106">使用 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) 方法，將此外部金鑰儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="ac61c-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="ac61c-107">當電腦啟動時，包含此外部金鑰的 USB 記憶體裝置可以用來做為啟動金鑰或修復金鑰。</span><span class="sxs-lookup"><span data-stu-id="ac61c-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="ac61c-108">為磁片區建立「外部金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="ac61c-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac61c-109">語法</span><span class="sxs-lookup"><span data-stu-id="ac61c-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="ac61c-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac61c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac61c-111">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac61c-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac61c-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac61c-112">Type: **string**</span></span>

<span data-ttu-id="ac61c-113">字串，指定此金鑰保護裝置的使用者指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac61c-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="ac61c-114">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="ac61c-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="ac61c-115">*ExternalKey* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ac61c-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ac61c-116">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ac61c-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="ac61c-117">位元組陣列，指定用來解除鎖定磁片區的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="ac61c-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="ac61c-118">如果未指定外部索引鍵，則會隨機產生一個索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ac61c-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="ac61c-119">使用 [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) 方法來取得隨機產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="ac61c-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="ac61c-120">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac61c-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac61c-121">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="ac61c-121">Type: **string**</span></span>

<span data-ttu-id="ac61c-122">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac61c-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="ac61c-123">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ac61c-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac61c-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac61c-124">Return value</span></span>

<span data-ttu-id="ac61c-125">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="ac61c-125">Type: **uint32**</span></span>

<span data-ttu-id="ac61c-126">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ac61c-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ac61c-127">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ac61c-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="ac61c-128">Description</span><span class="sxs-lookup"><span data-stu-id="ac61c-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac61c-129"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ac61c-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="ac61c-130">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ac61c-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="ac61c-131"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="ac61c-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="ac61c-132">提供 *ExternalKey* 參數，但不是大小為4的陣列。</span><span class="sxs-lookup"><span data-stu-id="ac61c-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="ac61c-133"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ac61c-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="ac61c-134">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="ac61c-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ac61c-135"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="ac61c-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="ac61c-136">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="ac61c-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="ac61c-137">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="ac61c-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="ac61c-138">備註</span><span class="sxs-lookup"><span data-stu-id="ac61c-138">Remarks</span></span>

<span data-ttu-id="ac61c-139">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ac61c-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ac61c-140">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ac61c-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ac61c-141">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ac61c-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ac61c-142">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="ac61c-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac61c-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac61c-143">Requirements</span></span>



| <span data-ttu-id="ac61c-144">需求</span><span class="sxs-lookup"><span data-stu-id="ac61c-144">Requirement</span></span> | <span data-ttu-id="ac61c-145">值</span><span class="sxs-lookup"><span data-stu-id="ac61c-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac61c-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac61c-146">Minimum supported client</span></span><br/> | <span data-ttu-id="ac61c-147">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac61c-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ac61c-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac61c-148">Minimum supported server</span></span><br/> | <span data-ttu-id="ac61c-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac61c-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac61c-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac61c-150">Namespace</span></span><br/>                | <span data-ttu-id="ac61c-151">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ac61c-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ac61c-152">MOF</span><span class="sxs-lookup"><span data-stu-id="ac61c-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac61c-153"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac61c-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac61c-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac61c-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac61c-155">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="ac61c-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

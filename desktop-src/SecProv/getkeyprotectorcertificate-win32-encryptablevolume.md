---
description: 捕獲公開金鑰保護裝置的公開金鑰和憑證指紋。
ms.assetid: 86fd0562-feb9-4b85-b27b-30270f864d8e
title: Win32_EncryptableVolume 類別的 GetKeyProtectorCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3954d3c55c4695e501d486f309598569b1facfc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975220"
---
# <a name="getkeyprotectorcertificate-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1d380-103">Win32 EncryptableVolume 類別的 GetKeyProtectorCertificate 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1d380-103">GetKeyProtectorCertificate method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1d380-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorCertificate** 方法會抓取公開金鑰保護裝置的 [*公開金鑰*](../secgloss/p-gly.md)和 [*憑證*](../secgloss/c-gly.md)指紋。</span><span class="sxs-lookup"><span data-stu-id="1d380-104">The **GetKeyProtectorCertificate** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the [*public key*](../secgloss/p-gly.md) and [*certificate*](../secgloss/c-gly.md) thumbprint for a public key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d380-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d380-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PublicKey[],
  [out] string CertThumbprint,
  [out] uint32 CertType
);
```



## <a name="parameters"></a><span data-ttu-id="1d380-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d380-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d380-107">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d380-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d380-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d380-108">Type: **string**</span></span>

<span data-ttu-id="1d380-109">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d380-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="1d380-110">*PublicKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d380-110">*PublicKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d380-111">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="1d380-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="1d380-112">指定公開金鑰的位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="1d380-112">An array of bytes that specifies the public key.</span></span>

</dd> <dt>

<span data-ttu-id="1d380-113">*CertThumbprint* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d380-113">*CertThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d380-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1d380-114">Type: **string**</span></span>

<span data-ttu-id="1d380-115">指定憑證指紋的字串。</span><span class="sxs-lookup"><span data-stu-id="1d380-115">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="1d380-116">*CertType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1d380-116">*CertType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d380-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1d380-117">Type: **uint32**</span></span>

<span data-ttu-id="1d380-118">指定金鑰保護裝置類型的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="1d380-118">An unsigned integer that specifies the type of the key protector.</span></span> <span data-ttu-id="1d380-119">此整數可用來區分資料修復代理 (DRA) 和使用者憑證。</span><span class="sxs-lookup"><span data-stu-id="1d380-119">This integer is used to differentiate between data recovery agent (DRA) and user certificates.</span></span>



| <span data-ttu-id="1d380-120">值</span><span class="sxs-lookup"><span data-stu-id="1d380-120">Value</span></span>                                                                        | <span data-ttu-id="1d380-121">意義</span><span class="sxs-lookup"><span data-stu-id="1d380-121">Meaning</span></span>                                  |
|------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="1d380-122"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-122"><dt>1</dt></span></span> </dl> | <span data-ttu-id="1d380-123">憑證是 DRA。</span><span class="sxs-lookup"><span data-stu-id="1d380-123">The certificate is a DRA.</span></span><br/>     |
| <dl> <span data-ttu-id="1d380-124"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-124"><dt>2</dt></span></span> </dl> | <span data-ttu-id="1d380-125">憑證不是 DRA。</span><span class="sxs-lookup"><span data-stu-id="1d380-125">The certificate is not a DRA.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d380-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d380-126">Return value</span></span>

<span data-ttu-id="1d380-127">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1d380-127">Type: **uint32**</span></span>

<span data-ttu-id="1d380-128">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1d380-128">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1d380-129">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1d380-129">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="1d380-130">Description</span><span class="sxs-lookup"><span data-stu-id="1d380-130">Description</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d380-131"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-131"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="1d380-132">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1d380-132">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="1d380-133"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-133"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                               | <span data-ttu-id="1d380-134">指定的金鑰保護裝置不是金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1d380-134">The specified key protector is not a key protector.</span></span> <span data-ttu-id="1d380-135">您必須輸入其他金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1d380-135">You must enter another key protector.</span></span><br/>            |
| <dl> <span data-ttu-id="1d380-136"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="1d380-137">此磁片磁碟機已由 BitLocker 磁碟機加密鎖定。</span><span class="sxs-lookup"><span data-stu-id="1d380-137">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="1d380-138">您必須將此磁片區從主控台解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="1d380-138">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="1d380-139"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-139"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="1d380-140">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1d380-140">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1d380-141">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1d380-141">Add a key protector to enable BitLocker.</span></span> <br/>                    |
| <dl> <span data-ttu-id="1d380-142"><dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 需要**</dt> <dt>2150695027 (0x80310073)</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-142"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_REQUIRED**</dt> <dt>2150695027 (0x80310073)</dt></span></span> </dl> | <span data-ttu-id="1d380-143">群組原則需要使用使用者憑證（例如智慧卡）。</span><span class="sxs-lookup"><span data-stu-id="1d380-143">Group Policy requires the use of a user certificate, such as a smart card.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="1d380-144">備註</span><span class="sxs-lookup"><span data-stu-id="1d380-144">Remarks</span></span>

<span data-ttu-id="1d380-145">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1d380-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1d380-146">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1d380-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1d380-147">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1d380-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1d380-148">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1d380-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d380-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d380-149">Requirements</span></span>



| <span data-ttu-id="1d380-150">需求</span><span class="sxs-lookup"><span data-stu-id="1d380-150">Requirement</span></span> | <span data-ttu-id="1d380-151">值</span><span class="sxs-lookup"><span data-stu-id="1d380-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d380-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d380-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1d380-153">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d380-153">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1d380-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d380-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1d380-155">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d380-155">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1d380-156">命名空間</span><span class="sxs-lookup"><span data-stu-id="1d380-156">Namespace</span></span><br/>                | <span data-ttu-id="1d380-157">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1d380-157">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1d380-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1d380-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d380-159"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d380-159"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d380-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d380-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d380-161">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1d380-161">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

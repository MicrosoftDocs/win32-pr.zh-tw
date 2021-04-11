---
description: 驗證所提供憑證的 (EKU) 物件識別碼 (OID) 的增強金鑰使用方法。
ms.assetid: cc716524-f976-4d75-84f3-693e277030e6
title: Win32_EncryptableVolume 類別的 ProtectKeyWithCertificateFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 86d9557506dc9ff3c465bcb956391b3e4cf33791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847872"
---
# <a name="protectkeywithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6eb73-103">Win32 EncryptableVolume 類別的 ProtectKeyWithCertificateFile 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6eb73-103">ProtectKeyWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6eb73-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithCertificateFile** 方法會驗證所提供憑證 (OID) 的增強金鑰使用方法 (EKU) [*物件識別碼*](../secgloss/o-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="6eb73-104">The **ProtectKeyWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eb73-105">語法</span><span class="sxs-lookup"><span data-stu-id="6eb73-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateFile(
  [in, optional] string FriendlyName,
  [in]           string FileName,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="6eb73-106">參數</span><span class="sxs-lookup"><span data-stu-id="6eb73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eb73-107">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6eb73-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb73-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6eb73-108">Type: **string**</span></span>

<span data-ttu-id="6eb73-109">字串，指定此金鑰保護裝置的使用者指派字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="6eb73-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="6eb73-110">如果未指定此參數，則會使用憑證中的主體名稱來建立 *FriendlyName* 參數。</span><span class="sxs-lookup"><span data-stu-id="6eb73-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="6eb73-111">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eb73-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb73-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6eb73-112">Type: **string**</span></span>

<span data-ttu-id="6eb73-113">字串，指定用來啟用 BitLocker 之 .cer 檔案的位置和名稱。</span><span class="sxs-lookup"><span data-stu-id="6eb73-113">A string that specifies the location and name of the .cer file used to enable BitLocker.</span></span> <span data-ttu-id="6eb73-114">加密憑證必須以 .cer 格式匯出 ([*可辨別編碼規則*](../secgloss/d-gly.md) (DER) 編碼的二進位 [*x.509*](../secgloss/x-gly.md) 或 Base-64 編碼的 x.509) 。</span><span class="sxs-lookup"><span data-stu-id="6eb73-114">An encryption certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="6eb73-115">您可以從 Microsoft PKI、協力廠商 PKI 或自我簽署來產生加密憑證。</span><span class="sxs-lookup"><span data-stu-id="6eb73-115">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="6eb73-116">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6eb73-116">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6eb73-117">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6eb73-117">Type: **string**</span></span>

<span data-ttu-id="6eb73-118">唯一識別已建立金鑰保護裝置的字串，可用來管理此金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6eb73-118">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="6eb73-119">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="6eb73-119">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eb73-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eb73-120">Return value</span></span>

<span data-ttu-id="6eb73-121">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6eb73-121">Type: **uint32**</span></span>

<span data-ttu-id="6eb73-122">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6eb73-122">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6eb73-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6eb73-123">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="6eb73-124">Description</span><span class="sxs-lookup"><span data-stu-id="6eb73-124">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6eb73-125"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="6eb73-126">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6eb73-126">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="6eb73-127"><dt>**FVE \_E \_ 非 \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="6eb73-128">指定之憑證的 EKU 屬性不允許它用於 BitLocker 磁碟機加密。</span><span class="sxs-lookup"><span data-stu-id="6eb73-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="6eb73-129">BitLocker 不需要憑證擁有 EKU 屬性，但如果有設定，則必須將它設定為與 BitLocker 設定的 oid 相符的 OID。</span><span class="sxs-lookup"><span data-stu-id="6eb73-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="6eb73-130"><dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 不 \_ 允許**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="6eb73-131">群組原則不允許搭配 BitLocker 使用使用者憑證（例如智慧卡）。</span><span class="sxs-lookup"><span data-stu-id="6eb73-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="6eb73-132"><dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 必須 \_ 是 \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="6eb73-133">群組原則要求您提供智慧卡來使用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="6eb73-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="6eb73-134"><dt>**FVE \_E \_ 原則會 \_ 禁止 \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="6eb73-135">群組原則不允許使用自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="6eb73-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="6eb73-136"><dt>**錯誤 \_\_找不 \_ 到**</dt>檔案 <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-136"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                                | <span data-ttu-id="6eb73-137">系統找不到指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="6eb73-137">The system cannot find the specified file.</span></span><br/>                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="6eb73-138">備註</span><span class="sxs-lookup"><span data-stu-id="6eb73-138">Remarks</span></span>

<span data-ttu-id="6eb73-139">如果 OID 與登錄中服務控制器相關聯的 OID 不相符，則此方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="6eb73-139">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="6eb73-140">這可防止使用者在磁片區上手動設定資料修復代理 (DRA) 保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6eb73-140">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="6eb73-141">Dra 只能由服務設定。</span><span class="sxs-lookup"><span data-stu-id="6eb73-141">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eb73-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eb73-142">Requirements</span></span>



| <span data-ttu-id="6eb73-143">需求</span><span class="sxs-lookup"><span data-stu-id="6eb73-143">Requirement</span></span> | <span data-ttu-id="6eb73-144">值</span><span class="sxs-lookup"><span data-stu-id="6eb73-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6eb73-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6eb73-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6eb73-146">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eb73-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6eb73-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6eb73-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6eb73-148">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eb73-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6eb73-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="6eb73-149">Namespace</span></span><br/>                | <span data-ttu-id="6eb73-150">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6eb73-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6eb73-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6eb73-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6eb73-152"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="6eb73-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6eb73-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eb73-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eb73-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6eb73-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

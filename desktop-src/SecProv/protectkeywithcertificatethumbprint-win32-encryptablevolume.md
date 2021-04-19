---
description: 驗證所提供憑證的 (EKU) 物件識別碼 (OID) 的增強金鑰使用方法。
ms.assetid: 7096cead-c44a-404c-b1e1-3e0ab27070f8
title: Win32_EncryptableVolume 類別的 ProtectKeyWithCertificateThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e0b47aabccaacfb3ab81968b8a93037aad304f8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987698"
---
# <a name="protectkeywithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="da02f-103">Win32 EncryptableVolume 類別的 ProtectKeyWithCertificateThumbprint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="da02f-103">ProtectKeyWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="da02f-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithCertificateThumbprint** 方法會驗證所提供憑證 (OID) 的增強金鑰使用方法 (EKU) [*物件識別碼*](../secgloss/o-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="da02f-104">The **ProtectKeyWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class validates the Enhanced Key Usage (EKU) [*object identifier*](../secgloss/o-gly.md) (OID) of the provided certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="da02f-105">語法</span><span class="sxs-lookup"><span data-stu-id="da02f-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithCertificateThumbprint(
  [in, optional] string FriendlyName,
  [in]           string CertThumbprint,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="da02f-106">參數</span><span class="sxs-lookup"><span data-stu-id="da02f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da02f-107">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="da02f-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="da02f-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="da02f-108">Type: **string**</span></span>

<span data-ttu-id="da02f-109">字串，指定此金鑰保護裝置的使用者指派字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="da02f-109">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="da02f-110">如果未指定此參數，則會使用憑證中的主體名稱來建立 *FriendlyName* 參數。</span><span class="sxs-lookup"><span data-stu-id="da02f-110">If this parameter is not specified, the *FriendlyName* parameter is created by using the Subject Name in the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="da02f-111">*CertThumbprint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="da02f-111">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da02f-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="da02f-112">Type: **string**</span></span>

<span data-ttu-id="da02f-113">指定憑證指紋的字串。</span><span class="sxs-lookup"><span data-stu-id="da02f-113">A string that specifies the certificate thumbprint.</span></span>

</dd> <dt>

<span data-ttu-id="da02f-114">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="da02f-114">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da02f-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="da02f-115">Type: **string**</span></span>

<span data-ttu-id="da02f-116">唯一識別已建立金鑰保護裝置的字串，可用來管理此金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="da02f-116">A string that uniquely identifies the created key protector that can be used to manage this key protector.</span></span>

<span data-ttu-id="da02f-117">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="da02f-117">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da02f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="da02f-118">Return value</span></span>

<span data-ttu-id="da02f-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="da02f-119">Type: **uint32**</span></span>

<span data-ttu-id="da02f-120">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="da02f-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="da02f-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="da02f-121">Return code/value</span></span>                                                                                                                                                                                           | <span data-ttu-id="da02f-122">Description</span><span class="sxs-lookup"><span data-stu-id="da02f-122">Description</span></span>                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="da02f-123"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                           | <span data-ttu-id="da02f-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="da02f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="da02f-125"><dt>**錯誤 \_不正確 \_ DATA**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-125"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>                                           | <span data-ttu-id="da02f-126">資料無效。</span><span class="sxs-lookup"><span data-stu-id="da02f-126">The data is not valid.</span></span><br/>                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="da02f-127"><dt>**FVE \_E \_ 非 \_ BITLOCKER \_ OID**</dt> <dt>2150695022 (0x8031006E)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-127"><dt>**FVE\_E\_NON\_BITLOCKER\_OID**</dt> <dt>2150695022 (0x8031006E)</dt></span></span> </dl>                     | <span data-ttu-id="da02f-128">指定之憑證的 EKU 屬性不允許它用於 BitLocker 磁碟機加密。</span><span class="sxs-lookup"><span data-stu-id="da02f-128">The EKU attribute of the specified certificate does not permit it to be used for BitLocker Drive Encryption.</span></span> <span data-ttu-id="da02f-129">BitLocker 不需要憑證擁有 EKU 屬性，但如果有設定，則必須將它設定為與 BitLocker 設定的 oid 相符的 OID。</span><span class="sxs-lookup"><span data-stu-id="da02f-129">BitLocker does not require that a certificate have an EKU attribute, but if one is configured, it must be set to an OID that matches the OID configured for BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="da02f-130"><dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 不 \_ 允許**</dt> <dt>2150695026 (0x80310072)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-130"><dt>**FVE\_E\_POLICY\_USER\_CERTIFICATE\_NOT\_ALLOWED**</dt> <dt>2150695026 (0x80310072)</dt></span></span> </dl> | <span data-ttu-id="da02f-131">群組原則不允許搭配 BitLocker 使用使用者憑證（例如智慧卡）。</span><span class="sxs-lookup"><span data-stu-id="da02f-131">Group Policy does not permit user certificates, such as smart cards, to be used with BitLocker.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="da02f-132"><dt>**FVE \_E \_ 原則 \_ 使用者 \_ 憑證 \_ 必須 \_ 是 \_ HW**</dt> <dt>2150695028 (0x80310074)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-132"><dt>**FVE\_E\_POLICY\_USER\_CERT\_MUST\_BE\_HW**</dt> <dt>2150695028 (0x80310074)</dt></span></span> </dl>        | <span data-ttu-id="da02f-133">群組原則要求您提供智慧卡來使用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="da02f-133">Group Policy requires that you supply a smart card to use BitLocker.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="da02f-134"><dt>**FVE \_E \_ 原則會 \_ 禁止 \_ SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-134"><dt>**FVE\_E\_POLICY\_PROHIBITS\_SELFSIGNED**</dt> <dt>2150695046 (0x80310086)</dt></span></span> </dl>           | <span data-ttu-id="da02f-135">群組原則不允許使用自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="da02f-135">Group Policy does not permit the use of self-signed certificates.</span></span><br/>                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="da02f-136">備註</span><span class="sxs-lookup"><span data-stu-id="da02f-136">Remarks</span></span>

<span data-ttu-id="da02f-137">如果 OID 與登錄中服務控制器相關聯的 OID 不相符，則此方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="da02f-137">If the OID does not match the one associated with the service controller in the registry, this method fails.</span></span> <span data-ttu-id="da02f-138">這可防止使用者在磁片區上手動設定資料修復代理 (DRA) 保護裝置。</span><span class="sxs-lookup"><span data-stu-id="da02f-138">This prevents the user from setting data recovery agent (DRA) protectors manually on the volume.</span></span> <span data-ttu-id="da02f-139">Dra 只能由服務設定。</span><span class="sxs-lookup"><span data-stu-id="da02f-139">DRAs are only to be set by the service.</span></span>

## <a name="requirements"></a><span data-ttu-id="da02f-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="da02f-140">Requirements</span></span>



| <span data-ttu-id="da02f-141">需求</span><span class="sxs-lookup"><span data-stu-id="da02f-141">Requirement</span></span> | <span data-ttu-id="da02f-142">值</span><span class="sxs-lookup"><span data-stu-id="da02f-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da02f-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da02f-143">Minimum supported client</span></span><br/> | <span data-ttu-id="da02f-144">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da02f-144">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="da02f-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da02f-145">Minimum supported server</span></span><br/> | <span data-ttu-id="da02f-146">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da02f-146">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="da02f-147">命名空間</span><span class="sxs-lookup"><span data-stu-id="da02f-147">Namespace</span></span><br/>                | <span data-ttu-id="da02f-148">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="da02f-148">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="da02f-149">MOF</span><span class="sxs-lookup"><span data-stu-id="da02f-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da02f-150"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="da02f-150"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da02f-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da02f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da02f-152">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="da02f-152">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: Win32_EncryptableVolume 類別的 ProtectKeyWithPassphrase 方法-使用複雜密碼來取得衍生金鑰。
ms.assetid: 62b070ec-4788-47cc-bfa4-6811a712ddbd
title: Win32_EncryptableVolume 類別的 ProtectKeyWithPassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a7772b1b65890fedbdbb8dcced1ad851f3845b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098346"
---
# <a name="protectkeywithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b59de-103">Win32 EncryptableVolume 類別的 ProtectKeyWithPassphrase 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b59de-103">ProtectKeyWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b59de-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithPassphrase** 方法會使用複雜密碼來取得衍生金鑰。</span><span class="sxs-lookup"><span data-stu-id="b59de-104">The **ProtectKeyWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="b59de-105">計算衍生金鑰之後，會使用衍生金鑰來保護加密磁片區的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="b59de-105">After the derived key is calculated, the derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59de-106">語法</span><span class="sxs-lookup"><span data-stu-id="b59de-106">Syntax</span></span>


```mof
uint32 ProtectKeyWithPassphrase(
  [in, optional] string FriendlyName,
  [in]           string Passphrase,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="b59de-107">參數</span><span class="sxs-lookup"><span data-stu-id="b59de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b59de-108">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b59de-108">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b59de-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b59de-109">Type: **string**</span></span>

<span data-ttu-id="b59de-110">字串，指定此金鑰保護裝置的使用者指派字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="b59de-110">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="b59de-111">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="b59de-111">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="b59de-112">複雜 *密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b59de-112">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b59de-113">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b59de-113">Type: **string**</span></span>

<span data-ttu-id="b59de-114">指定複雜密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="b59de-114">A string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="b59de-115">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b59de-115">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b59de-116">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b59de-116">Type: **string**</span></span>

<span data-ttu-id="b59de-117">可唯一識別已建立金鑰保護裝置的字串。</span><span class="sxs-lookup"><span data-stu-id="b59de-117">A string that uniquely identifies the created key protector.</span></span>

<span data-ttu-id="b59de-118">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b59de-118">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b59de-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="b59de-119">Return value</span></span>

<span data-ttu-id="b59de-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b59de-120">Type: **uint32**</span></span>

<span data-ttu-id="b59de-121">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b59de-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b59de-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b59de-122">Return code/value</span></span>                                                                                                                                                                                        | <span data-ttu-id="b59de-123">Description</span><span class="sxs-lookup"><span data-stu-id="b59de-123">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b59de-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                        | <span data-ttu-id="b59de-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="b59de-125">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="b59de-126"><dt>**FVE \_E \_ 不 \_ 允許 \_ 在 \_ 安全 \_ 模式2150694976中**</dt> <dt> (0x80310040)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-126"><dt>**FVE\_E\_NOT\_ALLOWED\_IN\_SAFE\_MODE**</dt> <dt>2150694976 (0x80310040)</dt></span></span> </dl>         | <span data-ttu-id="b59de-127">在安全模式中使用 BitLocker 磁碟機加密只能用於復原用途。</span><span class="sxs-lookup"><span data-stu-id="b59de-127">BitLocker Drive Encryption can only be used for recovery purposes when used in Safe Mode.</span></span><br/>                     |
| <dl> <span data-ttu-id="b59de-128"><dt>**FVE \_E \_ 原則複雜 \_ 密碼 \_ 不 \_ 允許**</dt> <dt>2150695018 (0x8031006A)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-128"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695018 (0x8031006A)</dt></span></span> </dl>     | <span data-ttu-id="b59de-129">群組原則不允許建立複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="b59de-129">Group policy does not permit the creation of a passphrase.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b59de-130"><dt>**FVE \_E \_ FIPS \_ 可防止複雜 \_ 密碼**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-130"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>           | <span data-ttu-id="b59de-131">需要 FIPS 合規性的群組原則設定導致無法產生或使用複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="b59de-131">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span><br/> |
| <dl> <span data-ttu-id="b59de-132"><dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-132"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl>  | <span data-ttu-id="b59de-133">提供的複雜密碼不符合最小或最大長度需求。</span><span class="sxs-lookup"><span data-stu-id="b59de-133">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                             |
| <dl> <span data-ttu-id="b59de-134"><dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-134"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>      | <span data-ttu-id="b59de-135">複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="b59de-135">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>            |
| <dl> <span data-ttu-id="b59de-136"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-136"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                       | <span data-ttu-id="b59de-137">磁片區已被 BitLocker 磁碟機加密鎖定。</span><span class="sxs-lookup"><span data-stu-id="b59de-137">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="b59de-138">您必須從主控台解除鎖定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="b59de-138">You must unlock the drive from Control Panel.</span></span><br/>     |
| <dl> <span data-ttu-id="b59de-139"><dt>**FVE \_E \_ \_**</dt>重迭的更新 <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-139"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                   | <span data-ttu-id="b59de-140">已由另一個執行緒更新加密磁片區的控制區塊。</span><span class="sxs-lookup"><span data-stu-id="b59de-140">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                     |
| <dl> <span data-ttu-id="b59de-141"><dt>**FVE \_E \_ KEY \_ 保護裝置 \_ 不 \_ 支援**</dt> <dt>2150695017 (0x80310069)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-141"><dt>**FVE\_E\_KEY\_PROTECTOR\_NOT\_SUPPORTED**</dt> <dt>2150695017 (0x80310069)</dt></span></span> </dl>       | <span data-ttu-id="b59de-142">目前在磁片區上的 BitLocker 磁碟機加密版本不支援金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b59de-142">The key protector is not supported by the version of BitLocker Drive Encryption currently on the volume.</span></span><br/>      |
| <dl> <span data-ttu-id="b59de-143"><dt>**FVE \_\_ \_ \_ \_ 不 \_ 允許使用 E OS 磁片**</dt>區複雜密碼 <dt>2150695021 (0x8031006D)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-143"><dt>**FVE\_E\_OS\_VOLUME\_PASSPHRASE\_NOT\_ALLOWED**</dt> <dt>2150695021 (0x8031006D)</dt></span></span> </dl> | <span data-ttu-id="b59de-144">複雜密碼無法新增至作業系統磁片區。</span><span class="sxs-lookup"><span data-stu-id="b59de-144">The passphrase cannot be added to the operating system volume.</span></span> <br/>                                               |
| <dl> <span data-ttu-id="b59de-145"><dt>**FVE \_E \_ 保護裝置 \_ 存在**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-145"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>                    | <span data-ttu-id="b59de-146">提供的金鑰保護裝置已經存在於此磁片區上。</span><span class="sxs-lookup"><span data-stu-id="b59de-146">The provided key protector already exists on this volume.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="b59de-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="b59de-147">Requirements</span></span>



| <span data-ttu-id="b59de-148">需求</span><span class="sxs-lookup"><span data-stu-id="b59de-148">Requirement</span></span> | <span data-ttu-id="b59de-149">值</span><span class="sxs-lookup"><span data-stu-id="b59de-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b59de-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b59de-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b59de-151">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b59de-151">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b59de-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b59de-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b59de-153">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b59de-153">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b59de-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="b59de-154">Namespace</span></span><br/>                | <span data-ttu-id="b59de-155">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b59de-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b59de-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b59de-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b59de-157"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="b59de-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b59de-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b59de-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b59de-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b59de-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





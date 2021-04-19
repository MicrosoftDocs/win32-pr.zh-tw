---
description: 使用提供的憑證檔案來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 41811d38-5c89-4372-9dbc-3de45b05011f
title: Win32_EncryptableVolume 類別的 UnlockWithCertificateFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d7ce1705c0ec457f64eb825e49334e76a14c184c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971587"
---
# <a name="unlockwithcertificatefile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3b67f-103">Win32 EncryptableVolume 類別的 UnlockWithCertificateFile 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3b67f-103">UnlockWithCertificateFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3b67f-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithCertificateFile** 方法會使用提供的 [*憑證*](../secgloss/c-gly.md)檔案來取得衍生金鑰，並解除鎖定加密的磁片區。</span><span class="sxs-lookup"><span data-stu-id="3b67f-104">The **UnlockWithCertificateFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) file to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="3b67f-105">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="3b67f-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3b67f-106">語法</span><span class="sxs-lookup"><span data-stu-id="3b67f-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateFile(
  [in] string FileName,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="3b67f-107">參數</span><span class="sxs-lookup"><span data-stu-id="3b67f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b67f-108">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b67f-108">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b67f-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b67f-109">Type: **string**</span></span>

<span data-ttu-id="3b67f-110">字串，指定用來取出憑證指紋之 .cer 檔案的位置和名稱。</span><span class="sxs-lookup"><span data-stu-id="3b67f-110">A string that specifies the location and name of the .cer file used to retrieve the certificate thumbprint.</span></span> <span data-ttu-id="3b67f-111">[*加密*](../secgloss/e-gly.md)憑證必須以 .cer 格式匯出 ([*可辨別編碼規則*](../secgloss/d-gly.md) (DER) 編碼的二進位 [*x.509*](../secgloss/x-gly.md)或 Base-64 編碼的 x.509) 。</span><span class="sxs-lookup"><span data-stu-id="3b67f-111">An [*encryption*](../secgloss/e-gly.md) certificate must be exported in .cer format ([*Distinguished Encoding Rules*](../secgloss/d-gly.md) (DER)-encoded binary [*X.509*](../secgloss/x-gly.md) or Base-64 encoded X.509).</span></span> <span data-ttu-id="3b67f-112">您可以從 Microsoft PKI、協力廠商 PKI 或自我簽署來產生加密憑證。</span><span class="sxs-lookup"><span data-stu-id="3b67f-112">The encryption certificate may be generated from Microsoft PKI, third-party PKI, or self-signed.</span></span>

</dd> <dt>

<span data-ttu-id="3b67f-113">*PIN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b67f-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b67f-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="3b67f-114">Type: **string**</span></span>

<span data-ttu-id="3b67f-115">使用者指定的個人識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="3b67f-115">A user-specified personal identification string.</span></span> <span data-ttu-id="3b67f-116">此字串必須包含4到20位數的序列。</span><span class="sxs-lookup"><span data-stu-id="3b67f-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="3b67f-117">這個字串是用來以無訊息方式驗證 [*金鑰儲存提供者*](../secgloss/k-gly.md) ， (KSP) 搭配 [*智慧卡*](../secgloss/s-gly.md)使用。</span><span class="sxs-lookup"><span data-stu-id="3b67f-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b67f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b67f-118">Return value</span></span>

<span data-ttu-id="3b67f-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3b67f-119">Type: **uint32**</span></span>

<span data-ttu-id="3b67f-120">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3b67f-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3b67f-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3b67f-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3b67f-122">Description</span><span class="sxs-lookup"><span data-stu-id="3b67f-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3b67f-123"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="3b67f-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="3b67f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="3b67f-125"><dt>**錯誤 \_\_找不 \_ 到**</dt>檔案 <dt>0000000002 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-125"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>0000000002 (0x2)</dt></span></span> </dl>                 | <span data-ttu-id="3b67f-126">系統無法提出指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="3b67f-126">The system cannot file the specified file.</span></span><br/>                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="3b67f-127"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="3b67f-128">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="3b67f-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3b67f-129">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="3b67f-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="3b67f-130"><dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-130"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="3b67f-131">無法使用所提供的資訊來解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="3b67f-131">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="3b67f-132"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-132"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="3b67f-133">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="3b67f-133">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="3b67f-134">您必須輸入其他金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="3b67f-134">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="3b67f-135"><dt>**FVE \_E \_ PRI加值稅EKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-135"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="3b67f-136">無法授權與指定憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="3b67f-136">The [*private key*](../secgloss/p-gly.md), associated with the specified certificate, could not be authorized.</span></span> <span data-ttu-id="3b67f-137">未提供私密金鑰授權，或提供的授權無效。</span><span class="sxs-lookup"><span data-stu-id="3b67f-137">The private key authorization was either not provided or the provided authorization was invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b67f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b67f-138">Requirements</span></span>



| <span data-ttu-id="3b67f-139">需求</span><span class="sxs-lookup"><span data-stu-id="3b67f-139">Requirement</span></span> | <span data-ttu-id="3b67f-140">值</span><span class="sxs-lookup"><span data-stu-id="3b67f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b67f-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3b67f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3b67f-142">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b67f-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3b67f-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3b67f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3b67f-144">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3b67f-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3b67f-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="3b67f-145">Namespace</span></span><br/>                | <span data-ttu-id="3b67f-146">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="3b67f-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3b67f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="3b67f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b67f-148"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b67f-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b67f-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b67f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b67f-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="3b67f-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 使用提供的憑證指紋來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 41c25d17-db1b-427e-907b-a547483927e0
title: Win32_EncryptableVolume 類別的 UnlockWithCertificateThumbprint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithCertificateThumbprint
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 5955334b6c147feea43d5e0a2c83a8e00050d900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690091"
---
# <a name="unlockwithcertificatethumbprint-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="faf67-103">Win32 EncryptableVolume 類別的 UnlockWithCertificateThumbprint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="faf67-103">UnlockWithCertificateThumbprint method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="faf67-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithCertificateThumbprint** 方法會使用提供的 [*憑證*](../secgloss/c-gly.md)指紋來取得衍生金鑰，並解除鎖定加密的磁片區。</span><span class="sxs-lookup"><span data-stu-id="faf67-104">The **UnlockWithCertificateThumbprint** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided [*certificate*](../secgloss/c-gly.md) thumbprint to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="faf67-105">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="faf67-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="faf67-106">語法</span><span class="sxs-lookup"><span data-stu-id="faf67-106">Syntax</span></span>


```mof
uint32 UnlockWithCertificateThumbprint(
  [in] string CertThumbprint,
  [in] string PIN
);
```



## <a name="parameters"></a><span data-ttu-id="faf67-107">參數</span><span class="sxs-lookup"><span data-stu-id="faf67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="faf67-108">*CertThumbprint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="faf67-108">*CertThumbprint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf67-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="faf67-109">Type: **string**</span></span>

<span data-ttu-id="faf67-110">憑證指紋值為0，因此會搜尋本機存放區以取得適當的憑證。</span><span class="sxs-lookup"><span data-stu-id="faf67-110">A thumbprint value of 0 is accepted and results in a search of the local store for the appropriate certificate.</span></span> <span data-ttu-id="faf67-111">如果找到單一 BitLocker 憑證，搜尋便會成功。</span><span class="sxs-lookup"><span data-stu-id="faf67-111">If a single BitLocker certificate is found, the search is successful.</span></span> <span data-ttu-id="faf67-112">如果找不到一個或多個憑證，方法將會失敗。</span><span class="sxs-lookup"><span data-stu-id="faf67-112">If none or more than one certificate is found, the method fails.</span></span>

</dd> <dt>

<span data-ttu-id="faf67-113">*PIN* \[在\]</span><span class="sxs-lookup"><span data-stu-id="faf67-113">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="faf67-114">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="faf67-114">Type: **string**</span></span>

<span data-ttu-id="faf67-115">使用者指定的個人識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="faf67-115">A user-specified personal identification string.</span></span> <span data-ttu-id="faf67-116">此字串必須包含4到20位數的序列。</span><span class="sxs-lookup"><span data-stu-id="faf67-116">This string must consist of a sequence of 4 to 20 digits.</span></span> <span data-ttu-id="faf67-117">這個字串是用來以無訊息方式驗證 [*金鑰儲存提供者*](../secgloss/k-gly.md) ， (KSP) 搭配 [*智慧卡*](../secgloss/s-gly.md)使用。</span><span class="sxs-lookup"><span data-stu-id="faf67-117">This string is used to silently authenticate the [*key storage provider*](../secgloss/k-gly.md) (KSP) when used with a [*smart card*](../secgloss/s-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="faf67-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="faf67-118">Return value</span></span>

<span data-ttu-id="faf67-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="faf67-119">Type: **uint32**</span></span>

<span data-ttu-id="faf67-120">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="faf67-120">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="faf67-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="faf67-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="faf67-122">Description</span><span class="sxs-lookup"><span data-stu-id="faf67-122">Description</span></span>                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="faf67-123"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="faf67-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="faf67-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="faf67-125"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="faf67-126">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="faf67-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="faf67-127">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="faf67-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                             |
| <dl> <span data-ttu-id="faf67-128"><dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>   | <span data-ttu-id="faf67-129">無法使用所提供的資訊來解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="faf67-129">The volume cannot be unlocked by using the provided information.</span></span> <br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="faf67-130"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="faf67-131">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="faf67-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="faf67-132">您必須輸入其他金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="faf67-132">You must enter another key protector.</span></span><br/>                                                                                                                                                                |
| <dl> <span data-ttu-id="faf67-133"><dt>**FVE \_E \_ PRI加值稅EKEY \_ AUTH \_ FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-133"><dt>**FVE\_E\_PRIVATEKEY\_AUTH\_FAILED**</dt> <dt>2150695060 (0x80310094)</dt></span></span> </dl> | <span data-ttu-id="faf67-134">無法授權與指定憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="faf67-134">The [*private key*](../secgloss/p-gly.md) associated with the specified certificate could not be authorized.</span></span> <span data-ttu-id="faf67-135">未提供私密金鑰授權，或提供的授權無效。</span><span class="sxs-lookup"><span data-stu-id="faf67-135">The private key authorization was either not provided or the provided authorization was not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="faf67-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="faf67-136">Requirements</span></span>



| <span data-ttu-id="faf67-137">需求</span><span class="sxs-lookup"><span data-stu-id="faf67-137">Requirement</span></span> | <span data-ttu-id="faf67-138">值</span><span class="sxs-lookup"><span data-stu-id="faf67-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faf67-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="faf67-139">Minimum supported client</span></span><br/> | <span data-ttu-id="faf67-140">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="faf67-140">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="faf67-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="faf67-141">Minimum supported server</span></span><br/> | <span data-ttu-id="faf67-142">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="faf67-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="faf67-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="faf67-143">Namespace</span></span><br/>                | <span data-ttu-id="faf67-144">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="faf67-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="faf67-145">MOF</span><span class="sxs-lookup"><span data-stu-id="faf67-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="faf67-146"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="faf67-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faf67-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="faf67-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faf67-148">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="faf67-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

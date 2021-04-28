---
description: Win32_EncryptableVolume 類別的 UnlockWithPassphrase 方法-使用複雜密碼來取得衍生金鑰。
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Win32_EncryptableVolume 類別的 UnlockWithPassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0206bf7884ffa204bc768ddfcf5a4a590bf25b60
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116456"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d1d61-103">Win32 EncryptableVolume 類別的 UnlockWithPassphrase 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d1d61-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d1d61-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithPassphrase** 方法會使用複雜密碼來取得衍生金鑰。</span><span class="sxs-lookup"><span data-stu-id="d1d61-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="d1d61-105">匯出衍生金鑰之後，會使用衍生金鑰來解除鎖定加密的磁片區主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="d1d61-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="d1d61-106">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="d1d61-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d1d61-107">語法</span><span class="sxs-lookup"><span data-stu-id="d1d61-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="d1d61-108">參數</span><span class="sxs-lookup"><span data-stu-id="d1d61-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1d61-109">複雜 *密碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1d61-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1d61-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1d61-110">Type: **string**</span></span>

<span data-ttu-id="d1d61-111">指定複雜密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="d1d61-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1d61-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1d61-112">Return value</span></span>

<span data-ttu-id="d1d61-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1d61-113">Type: **uint32**</span></span>

<span data-ttu-id="d1d61-114">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1d61-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="d1d61-115">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d1d61-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="d1d61-116">Description</span><span class="sxs-lookup"><span data-stu-id="d1d61-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1d61-117"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="d1d61-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="d1d61-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d1d61-119"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="d1d61-120">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="d1d61-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="d1d61-121">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="d1d61-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="d1d61-122"><dt>**FVE \_E \_ FIPS \_ 可防止複雜 \_ 密碼**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="d1d61-123">需要 FIPS 合規性的群組原則設定導致無法產生或使用複雜密碼。</span><span class="sxs-lookup"><span data-stu-id="d1d61-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="d1d61-124"><dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="d1d61-125">提供的複雜密碼不符合最小或最大長度需求。</span><span class="sxs-lookup"><span data-stu-id="d1d61-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="d1d61-126"><dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="d1d61-127">複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="d1d61-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="d1d61-128"><dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="d1d61-129">無法使用所提供的資訊來解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="d1d61-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="d1d61-130"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="d1d61-131">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="d1d61-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="d1d61-132">您必須輸入其他金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="d1d61-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="d1d61-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1d61-133">Requirements</span></span>



| <span data-ttu-id="d1d61-134">需求</span><span class="sxs-lookup"><span data-stu-id="d1d61-134">Requirement</span></span> | <span data-ttu-id="d1d61-135">值</span><span class="sxs-lookup"><span data-stu-id="d1d61-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d61-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1d61-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d61-137">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1d61-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d1d61-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1d61-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d61-139">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d1d61-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d1d61-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1d61-140">Namespace</span></span><br/>                | <span data-ttu-id="d1d61-141">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="d1d61-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d1d61-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d1d61-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1d61-143"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1d61-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d61-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1d61-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d61-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="d1d61-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





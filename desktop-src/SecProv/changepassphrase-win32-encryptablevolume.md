---
description: 使用新的複雜密碼來取得新的衍生金鑰。
ms.assetid: 89398bae-a2a2-466c-8a1e-a702018d679f
title: Win32_EncryptableVolume 類別的 ChangePassphrase 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ChangePassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: f28a78c6cb923b4f8934ec5cc8962b91b7f5139f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988927"
---
# <a name="changepassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="9796d-103">Win32 EncryptableVolume 類別的 ChangePassphrase 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9796d-103">ChangePassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="9796d-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ChangePassphrase** 方法會使用新的複雜密碼來取得新的衍生金鑰。</span><span class="sxs-lookup"><span data-stu-id="9796d-104">The **ChangePassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the new passphrase to obtain a new derived key.</span></span> <span data-ttu-id="9796d-105">計算衍生金鑰之後，會使用新的衍生金鑰來保護加密磁片區的主要金鑰。</span><span class="sxs-lookup"><span data-stu-id="9796d-105">After the derived key is calculated, the new derived key is used to secure the encrypted volume's master key.</span></span>

## <a name="syntax"></a><span data-ttu-id="9796d-106">語法</span><span class="sxs-lookup"><span data-stu-id="9796d-106">Syntax</span></span>


```mof
uint32 ChangePassphrase(
  [in]  string VolumeKeyProtectorID,
  [in]  string NewPassphrase,
  [out] string NewProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="9796d-107">參數</span><span class="sxs-lookup"><span data-stu-id="9796d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9796d-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9796d-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9796d-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9796d-109">Type: **string**</span></span>

<span data-ttu-id="9796d-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="9796d-110">A unique string identifier that is used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="9796d-111">*NewPassphrase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9796d-111">*NewPassphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9796d-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9796d-112">Type: **string**</span></span>

<span data-ttu-id="9796d-113">指定複雜密碼的更新字串。</span><span class="sxs-lookup"><span data-stu-id="9796d-113">An updated string that specifies the passphrase.</span></span>

</dd> <dt>

<span data-ttu-id="9796d-114">*NewProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9796d-114">*NewProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9796d-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9796d-115">Type: **string**</span></span>

<span data-ttu-id="9796d-116">用來管理加密磁片區金鑰保護裝置的更新唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="9796d-116">An updated unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9796d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="9796d-117">Return value</span></span>

<span data-ttu-id="9796d-118">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9796d-118">Type: **uint32**</span></span>

<span data-ttu-id="9796d-119">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9796d-119">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="9796d-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9796d-120">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="9796d-121">Description</span><span class="sxs-lookup"><span data-stu-id="9796d-121">Description</span></span>                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9796d-122"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="9796d-123">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="9796d-123">The method was successful.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="9796d-124"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-124"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>                      | <span data-ttu-id="9796d-125">磁片區已被 BitLocker 磁碟機加密鎖定。</span><span class="sxs-lookup"><span data-stu-id="9796d-125">The volume is already locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="9796d-126">您必須從主控台解除鎖定磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="9796d-126">You must unlock the drive from Control Panel.</span></span><br/>   |
| <dl> <span data-ttu-id="9796d-127"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="9796d-128">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="9796d-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="9796d-129">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="9796d-129">Add a key protector to enable BitLocker.</span></span> <br/>                           |
| <dl> <span data-ttu-id="9796d-130"><dt>**FVE \_E \_ \_**</dt>重迭的更新 <dt>2150694948 (0x80310024)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-130"><dt>**FVE\_E\_OVERLAPPED\_UPDATE**</dt> <dt>2150694948 (0x80310024)</dt></span></span> </dl>                  | <span data-ttu-id="9796d-131">已由另一個執行緒更新加密磁片區的控制區塊。</span><span class="sxs-lookup"><span data-stu-id="9796d-131">The control block for the encrypted volume was updated by another thread.</span></span><br/>                                   |
| <dl> <span data-ttu-id="9796d-132"><dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-132"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl>            | <span data-ttu-id="9796d-133">指定的金鑰保護裝置不是正確的類型。</span><span class="sxs-lookup"><span data-stu-id="9796d-133">The specified key protector is not of the correct type.</span></span> <br/>                                                    |
| <dl> <span data-ttu-id="9796d-134"><dt>**FVE \_E \_ 原則 \_ 不正確複雜 \_ 密碼 \_ 長度**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-134"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="9796d-135">提供的更新複雜密碼不符合最小或最大長度需求。</span><span class="sxs-lookup"><span data-stu-id="9796d-135">The updated passphrase provided does not meet the minimum or maximum length requirements.</span></span> <br/>                  |
| <dl> <span data-ttu-id="9796d-136"><dt>**FVE \_E \_ 原則 \_ \_ \_ 複雜密碼太簡單**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-136"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="9796d-137">更新的複雜密碼不符合系統管理員在群組原則中設定的複雜性需求。</span><span class="sxs-lookup"><span data-stu-id="9796d-137">The updated passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9796d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="9796d-138">Requirements</span></span>



| <span data-ttu-id="9796d-139">需求</span><span class="sxs-lookup"><span data-stu-id="9796d-139">Requirement</span></span> | <span data-ttu-id="9796d-140">值</span><span class="sxs-lookup"><span data-stu-id="9796d-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9796d-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9796d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9796d-142">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9796d-142">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9796d-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9796d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9796d-144">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9796d-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9796d-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="9796d-145">Namespace</span></span><br/>                | <span data-ttu-id="9796d-146">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="9796d-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="9796d-147">MOF</span><span class="sxs-lookup"><span data-stu-id="9796d-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9796d-148"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="9796d-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9796d-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9796d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9796d-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="9796d-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





---
description: 列出用來保護磁片區加密金鑰的保護裝置。
ms.assetid: ea88f128-c835-49e3-a395-c5ba472fff4b
title: Win32_EncryptableVolume 類別的 GetKeyProtectors 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectors
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 3a7d6a4110953d905b10eb4f7ef9a255af77897a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970151"
---
# <a name="getkeyprotectors-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="430d2-103">Win32 EncryptableVolume 類別的 GetKeyProtectors 方法 \_</span><span class="sxs-lookup"><span data-stu-id="430d2-103">GetKeyProtectors method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="430d2-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectors** 方法會列出用來保護磁片區加密金鑰的保護裝置。</span><span class="sxs-lookup"><span data-stu-id="430d2-104">The **GetKeyProtectors** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class lists the protectors used to secure the volume's encryption key.</span></span> <span data-ttu-id="430d2-105">如果提供保護裝置類型，則只會傳回指定類型的磁片區金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="430d2-105">If a protector type is provided, then only volume key protectors of the specified type are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="430d2-106">語法</span><span class="sxs-lookup"><span data-stu-id="430d2-106">Syntax</span></span>


```mof
uint32 GetKeyProtectors(
  [in, optional] uint32 KeyProtectorType,
  [out]          string VolumeKeyProtectorID[]
);
```



## <a name="parameters"></a><span data-ttu-id="430d2-107">參數</span><span class="sxs-lookup"><span data-stu-id="430d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="430d2-108">*KeyProtectorType* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="430d2-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="430d2-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="430d2-109">Type: **uint32**</span></span>

<span data-ttu-id="430d2-110">不帶正負號的整數，指定要傳回的金鑰保護裝置類型。</span><span class="sxs-lookup"><span data-stu-id="430d2-110">An unsigned integer that specifies the type of key protector to return.</span></span>

<span data-ttu-id="430d2-111">如果未指定此參數，則會傳回磁片區的所有可用金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="430d2-111">If this parameter is not specified, all available key protectors of the volume are returned.</span></span>



| <span data-ttu-id="430d2-112">值</span><span class="sxs-lookup"><span data-stu-id="430d2-112">Value</span></span>                                                                         | <span data-ttu-id="430d2-113">意義</span><span class="sxs-lookup"><span data-stu-id="430d2-113">Meaning</span></span>                                                           |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="430d2-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="430d2-115">所有類型。</span><span class="sxs-lookup"><span data-stu-id="430d2-115">All types.</span></span><br/> <span data-ttu-id="430d2-116">系統會傳回所有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="430d2-116">All key protectors are returned.</span></span><br/> |
| <dl> <span data-ttu-id="430d2-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="430d2-118">信賴平臺模組 (TPM) 。</span><span class="sxs-lookup"><span data-stu-id="430d2-118">Trusted Platform Module (TPM).</span></span><br/>                         |
| <dl> <span data-ttu-id="430d2-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="430d2-120">外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="430d2-120">External key.</span></span><br/>                                          |
| <dl> <span data-ttu-id="430d2-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="430d2-122">數值密碼。</span><span class="sxs-lookup"><span data-stu-id="430d2-122">Numeric password.</span></span><br/>                                      |
| <dl> <span data-ttu-id="430d2-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="430d2-124">TPM 和 PIN。</span><span class="sxs-lookup"><span data-stu-id="430d2-124">TPM And PIN.</span></span><br/>                                           |
| <dl> <span data-ttu-id="430d2-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="430d2-126">TPM 和啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="430d2-126">TPM And Startup Key.</span></span><br/>                                   |
| <dl> <span data-ttu-id="430d2-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="430d2-128">TPM 和 PIN 和啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="430d2-128">TPM And PIN And Startup Key.</span></span><br/>                           |
| <dl> <span data-ttu-id="430d2-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="430d2-130">公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="430d2-130">Public Key.</span></span><br/>                                            |
| <dl> <span data-ttu-id="430d2-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="430d2-132">密碼。</span><span class="sxs-lookup"><span data-stu-id="430d2-132">Passphrase.</span></span><br/>                                            |
| <dl> <span data-ttu-id="430d2-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="430d2-134">TPM 憑證</span><span class="sxs-lookup"><span data-stu-id="430d2-134">TPM Certificate</span></span><br/>                                        |
| <dl> <span data-ttu-id="430d2-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="430d2-136"> (SID) 的安全識別碼</span><span class="sxs-lookup"><span data-stu-id="430d2-136">Security Identifier (SID)</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="430d2-137">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="430d2-137">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="430d2-138">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="430d2-138">Type: **string\[\]**</span></span>

<span data-ttu-id="430d2-139">字串陣列，識別用來保護磁片區加密金鑰的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="430d2-139">An array of strings that identify the key protectors used to secure the volume's encryption key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="430d2-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="430d2-140">Return value</span></span>

<span data-ttu-id="430d2-141">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="430d2-141">Type: **uint32**</span></span>

<span data-ttu-id="430d2-142">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="430d2-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="430d2-143">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="430d2-143">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="430d2-144">Description</span><span class="sxs-lookup"><span data-stu-id="430d2-144">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="430d2-145"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="430d2-146">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="430d2-146">The method was successful.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="430d2-147"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="430d2-148">已指定 *VolumeKeyProtectorID* 參數，但未參考有效的 *KeyProtectorType*。</span><span class="sxs-lookup"><span data-stu-id="430d2-148">The *VolumeKeyProtectorID* parameter is specified but does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="430d2-149"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-149"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="430d2-150">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="430d2-150">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="430d2-151">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="430d2-151">Add a key protector to enable BitLocker.</span></span> <br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="430d2-152">備註</span><span class="sxs-lookup"><span data-stu-id="430d2-152">Remarks</span></span>

<span data-ttu-id="430d2-153">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="430d2-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="430d2-154">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="430d2-154">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="430d2-155">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="430d2-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="430d2-156">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="430d2-156">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="430d2-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="430d2-157">Requirements</span></span>



| <span data-ttu-id="430d2-158">需求</span><span class="sxs-lookup"><span data-stu-id="430d2-158">Requirement</span></span> | <span data-ttu-id="430d2-159">值</span><span class="sxs-lookup"><span data-stu-id="430d2-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="430d2-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="430d2-160">Minimum supported client</span></span><br/> | <span data-ttu-id="430d2-161">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="430d2-161">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="430d2-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="430d2-162">Minimum supported server</span></span><br/> | <span data-ttu-id="430d2-163">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="430d2-163">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="430d2-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="430d2-164">Namespace</span></span><br/>                | <span data-ttu-id="430d2-165">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="430d2-165">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="430d2-166">MOF</span><span class="sxs-lookup"><span data-stu-id="430d2-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="430d2-167"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="430d2-167"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="430d2-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="430d2-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="430d2-169">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="430d2-169">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 表示指定金鑰保護裝置的類型。
ms.assetid: 17cdde18-3979-4a19-b36e-aa71994148c9
title: Win32_EncryptableVolume 類別的 GetKeyProtectorType 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorType
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 483394f2e1c80f97442a9e6758f604093d513c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513852"
---
# <a name="getkeyprotectortype-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="cc4b4-103">Win32 EncryptableVolume 類別的 GetKeyProtectorType 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cc4b4-103">GetKeyProtectorType method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="cc4b4-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorType** 方法表示指定金鑰保護裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-104">The **GetKeyProtectorType** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the type of a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4b4-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc4b4-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorType(
  [in]  string VolumeKeyProtectorID,
  [out] uint32 KeyProtectorType
);
```



## <a name="parameters"></a><span data-ttu-id="cc4b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc4b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc4b4-107">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cc4b4-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc4b4-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="cc4b4-108">Type: **string**</span></span>

<span data-ttu-id="cc4b4-109">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="cc4b4-110">*KeyProtectorType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cc4b4-110">*KeyProtectorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc4b4-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cc4b4-111">Type: **uint32**</span></span>

<span data-ttu-id="cc4b4-112">指定金鑰保護裝置類型的不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-112">An unsigned integer that specifies the type of the key protector.</span></span>



| <span data-ttu-id="cc4b4-113">值</span><span class="sxs-lookup"><span data-stu-id="cc4b4-113">Value</span></span>                                                                         | <span data-ttu-id="cc4b4-114">意義</span><span class="sxs-lookup"><span data-stu-id="cc4b4-114">Meaning</span></span>                                              |
|-------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="cc4b4-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-115"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-116">未知或其他保護裝置類型</span><span class="sxs-lookup"><span data-stu-id="cc4b4-116">Unknown or other protector type</span></span><br/>           |
| <dl> <span data-ttu-id="cc4b4-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-118">信賴平台模組 (TPM)</span><span class="sxs-lookup"><span data-stu-id="cc4b4-118">Trusted Platform Module (TPM)</span></span><br/>             |
| <dl> <span data-ttu-id="cc4b4-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-120">外部金鑰</span><span class="sxs-lookup"><span data-stu-id="cc4b4-120">External key</span></span><br/>                              |
| <dl> <span data-ttu-id="cc4b4-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-122">數值密碼</span><span class="sxs-lookup"><span data-stu-id="cc4b4-122">Numerical password</span></span><br/>                        |
| <dl> <span data-ttu-id="cc4b4-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-124">TPM 和 PIN</span><span class="sxs-lookup"><span data-stu-id="cc4b4-124">TPM And PIN</span></span><br/>                               |
| <dl> <span data-ttu-id="cc4b4-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-126">TPM 和啟動金鑰</span><span class="sxs-lookup"><span data-stu-id="cc4b4-126">TPM And Startup Key</span></span><br/>                       |
| <dl> <span data-ttu-id="cc4b4-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-128">TPM 和 PIN 和啟動金鑰</span><span class="sxs-lookup"><span data-stu-id="cc4b4-128">TPM And PIN And Startup Key</span></span><br/>               |
| <dl> <span data-ttu-id="cc4b4-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-130">公開金鑰</span><span class="sxs-lookup"><span data-stu-id="cc4b4-130">Public Key</span></span><br/>                                |
| <dl> <span data-ttu-id="cc4b4-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-132">複雜密碼</span><span class="sxs-lookup"><span data-stu-id="cc4b4-132">Passphrase</span></span><br/>                                |
| <dl> <span data-ttu-id="cc4b4-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="cc4b4-134">TPM 憑證</span><span class="sxs-lookup"><span data-stu-id="cc4b4-134">TPM Certificate</span></span><br/>                           |
| <dl> <span data-ttu-id="cc4b4-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="cc4b4-136">CryptoAPI 下一代 (CNG) 保護裝置</span><span class="sxs-lookup"><span data-stu-id="cc4b4-136">CryptoAPI Next Generation (CNG) Protector</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc4b4-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc4b4-137">Return value</span></span>

<span data-ttu-id="cc4b4-138">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="cc4b4-138">Type: **uint32**</span></span>

<span data-ttu-id="cc4b4-139">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-139">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="cc4b4-140">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cc4b4-140">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="cc4b4-141">Description</span><span class="sxs-lookup"><span data-stu-id="cc4b4-141">Description</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc4b4-142"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-142"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="cc4b4-143">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-143">The method was successful.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="cc4b4-144"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-144"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="cc4b4-145">*VolumeKeyProtectorID* 參數未參考有效的 *KeyProtectorType*。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-145">The *VolumeKeyProtectorID* parameter does not refer to a valid *KeyProtectorType*.</span></span><br/> |
| <dl> <span data-ttu-id="cc4b4-146"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-146"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="cc4b4-147">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-147">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="cc4b4-148">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-148">Add a key protector to enable BitLocker.</span></span> <br/>  |



 

## <a name="remarks"></a><span data-ttu-id="cc4b4-149">備註</span><span class="sxs-lookup"><span data-stu-id="cc4b4-149">Remarks</span></span>

<span data-ttu-id="cc4b4-150">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cc4b4-151">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cc4b4-152">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cc4b4-153">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="cc4b4-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4b4-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc4b4-154">Requirements</span></span>



| <span data-ttu-id="cc4b4-155">需求</span><span class="sxs-lookup"><span data-stu-id="cc4b4-155">Requirement</span></span> | <span data-ttu-id="cc4b4-156">值</span><span class="sxs-lookup"><span data-stu-id="cc4b4-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4b4-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cc4b4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="cc4b4-158">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4b4-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cc4b4-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cc4b4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="cc4b4-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cc4b4-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc4b4-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="cc4b4-161">Namespace</span></span><br/>                | <span data-ttu-id="cc4b4-162">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="cc4b4-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="cc4b4-163">MOF</span><span class="sxs-lookup"><span data-stu-id="cc4b4-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc4b4-164"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc4b4-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4b4-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc4b4-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4b4-166">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="cc4b4-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 指出磁片區上所使用的加密演算法和金鑰大小。
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Win32_EncryptableVolume 類別的 GetEncryptionMethod 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987711"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c5ce8-103">Win32 EncryptableVolume 類別的 GetEncryptionMethod 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c5ce8-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c5ce8-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetEncryptionMethod** 方法會指出磁片區上所使用的加密演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ce8-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5ce8-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="c5ce8-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5ce8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ce8-107">*EncryptionMethod* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ce8-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-108">Type: **uint32**</span></span>

<span data-ttu-id="c5ce8-109">不帶正負號的整數，指定磁片區上所使用的加密演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="c5ce8-110">值</span><span class="sxs-lookup"><span data-stu-id="c5ce8-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="c5ce8-111">意義</span><span class="sxs-lookup"><span data-stu-id="c5ce8-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="c5ce8-112"><dt>**無**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="c5ce8-113">磁片區未加密。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="c5ce8-114"><dt>**AES \_ 128 \_ 與 \_ 擴散**</dt>器 <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="c5ce8-115">磁片區已完全或部分加密，使用以擴散器層增強的進階加密標準 (AES) 演算法（使用 AES 金鑰大小128位）。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="c5ce8-116">在執行 Windows 8.1 或更高版本的裝置上，將無法再使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="c5ce8-117"><dt>**AES \_ 256 \_ 與 \_ 擴散**</dt>器 <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="c5ce8-118">磁片區已完全或部分加密，使用以擴散器層增強的進階加密標準 (AES) 演算法（使用 AES 金鑰大小256位）。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="c5ce8-119">在執行 Windows 8.1 或更高版本的裝置上，將無法再使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="c5ce8-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="c5ce8-121">磁片區已使用進階加密標準 (AES) 演算法完整或部分加密，使用 AES 金鑰大小128位。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="c5ce8-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="c5ce8-123">磁片區已使用進階加密標準 (AES) 演算法完整或部分加密，使用 AES 金鑰大小256位。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="c5ce8-124"><dt>**硬體 \_加密**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="c5ce8-125">磁片區已使用磁片磁碟機的硬體功能完全或部分加密。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="c5ce8-126"><dt>**XTS \_AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="c5ce8-127">磁片區已使用進階加密標準 (AES) 和 AES 金鑰大小128位，以完整或部分加密的方式使用 XTS。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="c5ce8-128">此方法僅適用于執行 Windows 10 1511 或更高版本的裝置。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="c5ce8-129"><dt>**XTS \_AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="c5ce8-130">磁片區已使用進階加密標準 (AES) 和 AES 金鑰大小256位，以完整或部分加密的方式使用 XTS。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="c5ce8-131">此方法僅適用于執行 Windows 10 1511 或更高版本的裝置。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="c5ce8-132"><dt> (uint32) –1</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="c5ce8-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="c5ce8-133">UNKNOWN</span></span><br/> <span data-ttu-id="c5ce8-134">磁片區已完全或部分加密，但有未知的演算法和金鑰大小。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="c5ce8-135">*SelfEncryptionDriveEncryptionMethod* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ce8-136">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-136">Type: **string**</span></span>

<span data-ttu-id="c5ce8-137">加密演算法是在自我加密磁片磁碟機上設定的。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="c5ce8-138">Null 字串表示 BitLocker 正在使用軟體加密，或未報告任何加密方法。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ce8-139">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5ce8-139">Return value</span></span>

<span data-ttu-id="c5ce8-140">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-140">Type: **uint32**</span></span>

<span data-ttu-id="c5ce8-141">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c5ce8-142">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c5ce8-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c5ce8-143">Description</span><span class="sxs-lookup"><span data-stu-id="c5ce8-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c5ce8-144"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c5ce8-145">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c5ce8-146">備註</span><span class="sxs-lookup"><span data-stu-id="c5ce8-146">Remarks</span></span>

<span data-ttu-id="c5ce8-147">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c5ce8-148">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c5ce8-149">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c5ce8-150">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ce8-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ce8-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ce8-151">Requirements</span></span>



| <span data-ttu-id="c5ce8-152">需求</span><span class="sxs-lookup"><span data-stu-id="c5ce8-152">Requirement</span></span> | <span data-ttu-id="c5ce8-153">值</span><span class="sxs-lookup"><span data-stu-id="c5ce8-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ce8-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5ce8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ce8-155">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5ce8-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5ce8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ce8-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5ce8-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c5ce8-158">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5ce8-158">Namespace</span></span><br/>                | <span data-ttu-id="c5ce8-159">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c5ce8-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c5ce8-160">MOF</span><span class="sxs-lookup"><span data-stu-id="c5ce8-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5ce8-161"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5ce8-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ce8-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5ce8-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ce8-163">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="c5ce8-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 指出磁片區是否可供磁片區使用。
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Win32_EncryptableVolume 類別的 IsKeyProtectorAvailable 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191256"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="68377-103">Win32 EncryptableVolume 類別的 IsKeyProtectorAvailable 方法 \_</span><span class="sxs-lookup"><span data-stu-id="68377-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="68377-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsKeyProtectorAvailable** 方法會指出磁片區是否有可用的保護裝置。</span><span class="sxs-lookup"><span data-stu-id="68377-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="68377-105">如果提供保護裝置類型，則此方法會指出指定類型的保護裝置是否可供磁片區使用。</span><span class="sxs-lookup"><span data-stu-id="68377-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="68377-106">語法</span><span class="sxs-lookup"><span data-stu-id="68377-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="68377-107">參數</span><span class="sxs-lookup"><span data-stu-id="68377-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68377-108">*KeyProtectorType* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="68377-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="68377-109">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68377-109">Type: **uint32**</span></span>

<span data-ttu-id="68377-110">不帶正負號的整數，表示所查詢之磁片區金鑰保護裝置的類型。</span><span class="sxs-lookup"><span data-stu-id="68377-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="68377-111">如果未指定此參數，則會查詢磁片區的所有可用金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="68377-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="68377-112">值</span><span class="sxs-lookup"><span data-stu-id="68377-112">Value</span></span>                                                                         | <span data-ttu-id="68377-113">意義</span><span class="sxs-lookup"><span data-stu-id="68377-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="68377-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="68377-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="68377-115">所有類型。</span><span class="sxs-lookup"><span data-stu-id="68377-115">All types.</span></span><br/> <span data-ttu-id="68377-116">系統會查詢所有金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="68377-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="68377-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="68377-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="68377-118">信賴平臺模組 (TPM) 。</span><span class="sxs-lookup"><span data-stu-id="68377-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="68377-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="68377-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="68377-120">外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="68377-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="68377-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="68377-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="68377-122">數位密碼。</span><span class="sxs-lookup"><span data-stu-id="68377-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="68377-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="68377-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="68377-124">TPM 和 PIN。</span><span class="sxs-lookup"><span data-stu-id="68377-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="68377-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="68377-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="68377-126">TPM 和啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="68377-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="68377-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="68377-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="68377-128">TPM 和 PIN 和啟動金鑰。</span><span class="sxs-lookup"><span data-stu-id="68377-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="68377-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="68377-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="68377-130">公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="68377-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="68377-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="68377-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="68377-132">密碼。</span><span class="sxs-lookup"><span data-stu-id="68377-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="68377-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="68377-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="68377-134">TPM 憑證</span><span class="sxs-lookup"><span data-stu-id="68377-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="68377-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="68377-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="68377-136"> (SID) 的安全識別碼</span><span class="sxs-lookup"><span data-stu-id="68377-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="68377-137">*IsKeyProtectorAvailable* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="68377-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68377-138">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="68377-138">Type: **boolean**</span></span>

<span data-ttu-id="68377-139">布林值，指出磁片區上是否存在指定類型的磁片區金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="68377-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68377-140">傳回值</span><span class="sxs-lookup"><span data-stu-id="68377-140">Return value</span></span>

<span data-ttu-id="68377-141">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="68377-141">Type: **uint32**</span></span>

<span data-ttu-id="68377-142">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="68377-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="68377-143">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="68377-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="68377-144">Description</span><span class="sxs-lookup"><span data-stu-id="68377-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68377-145"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="68377-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="68377-146">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="68377-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="68377-147"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="68377-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="68377-148">已指定 *KeyProtectorType* 參數，但未參考有效的金鑰保護裝置類型。</span><span class="sxs-lookup"><span data-stu-id="68377-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68377-149">備註</span><span class="sxs-lookup"><span data-stu-id="68377-149">Remarks</span></span>

<span data-ttu-id="68377-150">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="68377-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="68377-151">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="68377-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="68377-152">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="68377-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="68377-153">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="68377-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68377-154">規格需求</span><span class="sxs-lookup"><span data-stu-id="68377-154">Requirements</span></span>



| <span data-ttu-id="68377-155">需求</span><span class="sxs-lookup"><span data-stu-id="68377-155">Requirement</span></span> | <span data-ttu-id="68377-156">值</span><span class="sxs-lookup"><span data-stu-id="68377-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68377-157">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68377-157">Minimum supported client</span></span><br/> | <span data-ttu-id="68377-158">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68377-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="68377-159">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68377-159">Minimum supported server</span></span><br/> | <span data-ttu-id="68377-160">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="68377-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="68377-161">命名空間</span><span class="sxs-lookup"><span data-stu-id="68377-161">Namespace</span></span><br/>                | <span data-ttu-id="68377-162">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="68377-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="68377-163">MOF</span><span class="sxs-lookup"><span data-stu-id="68377-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68377-164"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="68377-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68377-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68377-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68377-166">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="68377-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

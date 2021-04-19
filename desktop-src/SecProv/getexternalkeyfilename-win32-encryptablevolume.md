---
description: 傳回包含外部索引鍵的檔案名。
ms.assetid: c02d8dca-f30b-4ab5-a770-1ec6ac0b81c6
title: Win32_EncryptableVolume 類別的 GetExternalKeyFileName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFileName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bf8de41befa7414c9970ac451d34ee7c5f40dd84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985405"
---
# <a name="getexternalkeyfilename-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6c7ea-103">Win32 EncryptableVolume 類別的 GetExternalKeyFileName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6c7ea-103">GetExternalKeyFileName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6c7ea-104">如果此外部索引鍵是使用 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)方法儲存到檔案位置，則 [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetExternalKeyFileName** 方法會傳回包含外部索引鍵的檔案名。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-104">The **GetExternalKeyFileName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the name of the file that contains the external key, if this external key is saved to a file location by using the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="6c7ea-105">此方法僅適用于類型為「外部金鑰」、「TPM 和 PIN 和啟動金鑰」或「TPM 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-105">This method is only applicable for key protectors of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="6c7ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="6c7ea-106">Syntax</span></span>


```mof
uint32 GetExternalKeyFileName(
  [in]  string VolumeKeyProtectorID,
  [out] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="6c7ea-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c7ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c7ea-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c7ea-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7ea-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c7ea-109">Type: **string**</span></span>

<span data-ttu-id="6c7ea-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="6c7ea-111">*檔案名* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c7ea-111">*FileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c7ea-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6c7ea-112">Type: **string**</span></span>

<span data-ttu-id="6c7ea-113">字串，指定包含外部金鑰之檔案的副檔名，但不包含檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-113">A string that specifies the name with extension but without the file path, of the file that contains the external key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c7ea-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c7ea-114">Return value</span></span>

<span data-ttu-id="6c7ea-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6c7ea-115">Type: **uint32**</span></span>

<span data-ttu-id="6c7ea-116">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6c7ea-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6c7ea-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6c7ea-118">Description</span><span class="sxs-lookup"><span data-stu-id="6c7ea-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c7ea-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6c7ea-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="6c7ea-121"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-121"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="6c7ea-122">*VolumeKeyProtectorID* 參數未參考「外部金鑰」、「tpm 和 PIN 和啟動金鑰」或「Tpm 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-122">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="6c7ea-123"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="6c7ea-124">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-124">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="6c7ea-125"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="6c7ea-126">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6c7ea-127">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="6c7ea-128">備註</span><span class="sxs-lookup"><span data-stu-id="6c7ea-128">Remarks</span></span>

<span data-ttu-id="6c7ea-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6c7ea-130">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6c7ea-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6c7ea-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="6c7ea-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c7ea-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c7ea-133">Requirements</span></span>



| <span data-ttu-id="6c7ea-134">需求</span><span class="sxs-lookup"><span data-stu-id="6c7ea-134">Requirement</span></span> | <span data-ttu-id="6c7ea-135">值</span><span class="sxs-lookup"><span data-stu-id="6c7ea-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c7ea-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c7ea-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6c7ea-137">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7ea-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c7ea-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c7ea-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6c7ea-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7ea-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6c7ea-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="6c7ea-140">Namespace</span></span><br/>                | <span data-ttu-id="6c7ea-141">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6c7ea-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6c7ea-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6c7ea-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c7ea-143"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c7ea-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c7ea-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c7ea-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c7ea-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6c7ea-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="6c7ea-146">**SaveExternalKeyToFile**</span><span class="sxs-lookup"><span data-stu-id="6c7ea-146">**SaveExternalKeyToFile**</span></span>](saveexternalkeytofile-win32-encryptablevolume.md)
</dt> </dl>

 

 

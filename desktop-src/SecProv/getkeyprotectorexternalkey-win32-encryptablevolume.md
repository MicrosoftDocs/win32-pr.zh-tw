---
description: 抓取指定金鑰保護裝置的外部金鑰。
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Win32_EncryptableVolume 類別的 GetKeyProtectorExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191259"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="52ca5-103">Win32 EncryptableVolume 類別的 GetKeyProtectorExternalKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="52ca5-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="52ca5-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorExternalKey** 方法會針對適當類型的指定金鑰保護裝置，抓取外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="52ca5-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="52ca5-105">金鑰保護裝置識別碼必須參考「外部金鑰」、「TPM 和 PIN 和啟動金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="52ca5-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="52ca5-106">語法</span><span class="sxs-lookup"><span data-stu-id="52ca5-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="52ca5-107">參數</span><span class="sxs-lookup"><span data-stu-id="52ca5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52ca5-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="52ca5-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52ca5-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="52ca5-109">Type: **string**</span></span>

<span data-ttu-id="52ca5-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="52ca5-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="52ca5-111">*ExternalKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="52ca5-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="52ca5-112">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="52ca5-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="52ca5-113">位元組陣列，指定可以用來解除鎖定對應磁片區的256位外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="52ca5-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52ca5-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="52ca5-114">Return value</span></span>

<span data-ttu-id="52ca5-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="52ca5-115">Type: **uint32**</span></span>

<span data-ttu-id="52ca5-116">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="52ca5-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="52ca5-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="52ca5-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="52ca5-118">Description</span><span class="sxs-lookup"><span data-stu-id="52ca5-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="52ca5-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="52ca5-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="52ca5-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="52ca5-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="52ca5-121"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="52ca5-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="52ca5-122">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="52ca5-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="52ca5-123"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="52ca5-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="52ca5-124">*VolumeKeyProtectorID* 參數未參考「外部金鑰」、「tpm 和 PIN 和啟動金鑰」或「Tpm 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="52ca5-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="52ca5-125"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="52ca5-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="52ca5-126">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="52ca5-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="52ca5-127">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="52ca5-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="52ca5-128">備註</span><span class="sxs-lookup"><span data-stu-id="52ca5-128">Remarks</span></span>

<span data-ttu-id="52ca5-129">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="52ca5-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="52ca5-130">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="52ca5-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="52ca5-131">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="52ca5-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="52ca5-132">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="52ca5-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52ca5-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="52ca5-133">Requirements</span></span>



| <span data-ttu-id="52ca5-134">需求</span><span class="sxs-lookup"><span data-stu-id="52ca5-134">Requirement</span></span> | <span data-ttu-id="52ca5-135">值</span><span class="sxs-lookup"><span data-stu-id="52ca5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52ca5-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="52ca5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="52ca5-137">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52ca5-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="52ca5-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="52ca5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="52ca5-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="52ca5-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52ca5-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="52ca5-140">Namespace</span></span><br/>                | <span data-ttu-id="52ca5-141">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="52ca5-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="52ca5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="52ca5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52ca5-143"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="52ca5-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52ca5-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="52ca5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52ca5-145">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="52ca5-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 使用提供的外部索引鍵來存取資料磁片區的內容。
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Win32_EncryptableVolume 類別的 UnlockWithExternalKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975279"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="db037-103">Win32 EncryptableVolume 類別的 UnlockWithExternalKey 方法 \_</span><span class="sxs-lookup"><span data-stu-id="db037-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="db037-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithExternalKey** 方法會使用提供的外部索引鍵來存取資料磁片區的內容。</span><span class="sxs-lookup"><span data-stu-id="db037-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="db037-105">您必須使用 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法，透過此方法將磁片區解除鎖定，才能使用類型為「外部金鑰」的一或多個金鑰保護裝置來保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="db037-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="db037-106">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="db037-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="db037-107">語法</span><span class="sxs-lookup"><span data-stu-id="db037-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="db037-108">參數</span><span class="sxs-lookup"><span data-stu-id="db037-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db037-109">*ExternalKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="db037-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db037-110">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="db037-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="db037-111">位元組陣列，指定用來解除鎖定磁片區的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="db037-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="db037-112">您可以藉由呼叫 [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) 方法來取得此金鑰。</span><span class="sxs-lookup"><span data-stu-id="db037-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db037-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="db037-113">Return value</span></span>

<span data-ttu-id="db037-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="db037-114">Type: **uint32**</span></span>

<span data-ttu-id="db037-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="db037-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="db037-116">如果磁片區已解除鎖定，這個方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="db037-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="db037-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="db037-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="db037-118">Description</span><span class="sxs-lookup"><span data-stu-id="db037-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="db037-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="db037-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="db037-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="db037-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="db037-121"><dt>**錯誤 \_\_找不到**</dt><dt>指定的值 (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="db037-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="db037-122">磁片區沒有類型為「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="db037-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="db037-123"><dt>**錯誤 \_不正確 \_ 密碼**</dt><dt>未指定任何值 (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="db037-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="db037-124">存在一或多個類型為「外部金鑰」的金鑰保護裝置，但指定的 *ExternalKey* 參數無法解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="db037-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="db037-125"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="db037-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="db037-126">*ExternalKey* 參數不是大小為4的陣列。</span><span class="sxs-lookup"><span data-stu-id="db037-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="db037-127"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="db037-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="db037-128">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="db037-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="db037-129">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="db037-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="db037-130">備註</span><span class="sxs-lookup"><span data-stu-id="db037-130">Remarks</span></span>

<span data-ttu-id="db037-131">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="db037-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="db037-132">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="db037-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="db037-133">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="db037-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="db037-134">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="db037-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db037-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="db037-135">Requirements</span></span>



| <span data-ttu-id="db037-136">需求</span><span class="sxs-lookup"><span data-stu-id="db037-136">Requirement</span></span> | <span data-ttu-id="db037-137">值</span><span class="sxs-lookup"><span data-stu-id="db037-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db037-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db037-138">Minimum supported client</span></span><br/> | <span data-ttu-id="db037-139">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db037-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="db037-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db037-140">Minimum supported server</span></span><br/> | <span data-ttu-id="db037-141">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db037-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db037-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="db037-142">Namespace</span></span><br/>                | <span data-ttu-id="db037-143">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="db037-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="db037-144">MOF</span><span class="sxs-lookup"><span data-stu-id="db037-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db037-145"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="db037-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db037-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db037-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db037-147">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="db037-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

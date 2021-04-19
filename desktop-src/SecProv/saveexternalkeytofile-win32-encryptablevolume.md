---
description: 將與指定之磁片區金鑰保護裝置相關聯的外部金鑰寫入指定資料夾中的系統、隱藏、唯讀檔案。
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Win32_EncryptableVolume 類別的 SaveExternalKeyToFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985469"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1e077-103">Win32 EncryptableVolume 類別的 SaveExternalKeyToFile 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1e077-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1e077-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **SaveExternalKeyToFile** 方法會將與指定之磁片區金鑰保護裝置相關聯的外部金鑰，寫入指定之資料夾中的系統、隱藏的唯讀檔案。</span><span class="sxs-lookup"><span data-stu-id="1e077-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="1e077-105">此方法僅適用于類型為「外部金鑰」或「TPM 和啟動金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1e077-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="1e077-106">語法</span><span class="sxs-lookup"><span data-stu-id="1e077-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="1e077-107">參數</span><span class="sxs-lookup"><span data-stu-id="1e077-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e077-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e077-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e077-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e077-109">Type: **string**</span></span>

<span data-ttu-id="1e077-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="1e077-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="1e077-111">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1e077-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e077-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1e077-112">Type: **string**</span></span>

<span data-ttu-id="1e077-113">字串，其中包含要儲存與指定金鑰保護裝置相關聯的外部金鑰之磁片區或資料夾位置。</span><span class="sxs-lookup"><span data-stu-id="1e077-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="1e077-114">這個路徑不包含檔案的名稱，它是內部版本，可能會從版本變更為版本。</span><span class="sxs-lookup"><span data-stu-id="1e077-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="1e077-115">使用 **GetExternalKeyFileName** 來取得檔案名。</span><span class="sxs-lookup"><span data-stu-id="1e077-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e077-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e077-116">Return value</span></span>

<span data-ttu-id="1e077-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1e077-117">Type: **uint32**</span></span>

<span data-ttu-id="1e077-118">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1e077-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="1e077-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1e077-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="1e077-120">Description</span><span class="sxs-lookup"><span data-stu-id="1e077-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1e077-121"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="1e077-122">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1e077-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="1e077-123"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="1e077-124">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="1e077-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="1e077-125"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="1e077-126">*VolumeKeyProtectorID* 參數未參考「外部金鑰」或「TPM 和啟動金鑰」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="1e077-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="1e077-127"><dt>**錯誤 \_\_找不 \_ 到路徑**</dt> <dt>2147942403 (0x80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="1e077-128">*Path* 參數未參考有效的位置。</span><span class="sxs-lookup"><span data-stu-id="1e077-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="1e077-129">確定檔案名未包含在 *Path* 參數中。</span><span class="sxs-lookup"><span data-stu-id="1e077-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="1e077-130"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="1e077-131">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1e077-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1e077-132">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1e077-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="1e077-133">備註</span><span class="sxs-lookup"><span data-stu-id="1e077-133">Remarks</span></span>

<span data-ttu-id="1e077-134">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1e077-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1e077-135">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1e077-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1e077-136">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1e077-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1e077-137">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1e077-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e077-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e077-138">Requirements</span></span>



| <span data-ttu-id="1e077-139">需求</span><span class="sxs-lookup"><span data-stu-id="1e077-139">Requirement</span></span> | <span data-ttu-id="1e077-140">值</span><span class="sxs-lookup"><span data-stu-id="1e077-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e077-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e077-141">Minimum supported client</span></span><br/> | <span data-ttu-id="1e077-142">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e077-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="1e077-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e077-143">Minimum supported server</span></span><br/> | <span data-ttu-id="1e077-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e077-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e077-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="1e077-145">Namespace</span></span><br/>                | <span data-ttu-id="1e077-146">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1e077-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1e077-147">MOF</span><span class="sxs-lookup"><span data-stu-id="1e077-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e077-148"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e077-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e077-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e077-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e077-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1e077-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

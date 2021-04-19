---
description: 匯出可能會在磁片磁碟機嚴重損壞且不存在資料備份檔時，協助搶救加密資料的資訊。
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Win32_EncryptableVolume 類別的 GetKeyPackage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979970"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c128b-103">Win32 EncryptableVolume 類別的 GetKeyPackage 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c128b-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c128b-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyPackage** 方法會匯出資訊，當磁片磁碟機嚴重損毀且沒有資料備份檔時，可能有助於搶救加密資料。</span><span class="sxs-lookup"><span data-stu-id="c128b-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="c128b-105">匯出的資訊包含由類型為「數位密碼」或「外部金鑰」的金鑰保護裝置所保護的磁片區加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c128b-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="c128b-106">若要使用此封裝，您也必須儲存對應的數值密碼或外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="c128b-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c128b-107">如果您選擇匯出金鑰封裝，請務必將這項資訊保存在妥善保護的位置。</span><span class="sxs-lookup"><span data-stu-id="c128b-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="c128b-108">請勿將此資訊與您的電腦搭配使用。</span><span class="sxs-lookup"><span data-stu-id="c128b-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="c128b-109">如果此金鑰封裝遺失或遭竊，您將需要使用新的金鑰來解密磁片區並加以重新加密。</span><span class="sxs-lookup"><span data-stu-id="c128b-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="c128b-110">當磁片磁碟機失敗時，BitLocker 修復工具有助回收可用的資料。</span><span class="sxs-lookup"><span data-stu-id="c128b-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="c128b-111">如需此工具如何使用金鑰封裝的詳細資訊，請參閱 [如何使用 BitLocker 修復工具協助從 Windows Vista 中的加密磁片區復原資料](https://support.microsoft.com/kb/928201)。</span><span class="sxs-lookup"><span data-stu-id="c128b-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="c128b-112">語法</span><span class="sxs-lookup"><span data-stu-id="c128b-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="c128b-113">參數</span><span class="sxs-lookup"><span data-stu-id="c128b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c128b-114">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c128b-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c128b-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="c128b-115">Type: **string**</span></span>

<span data-ttu-id="c128b-116">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="c128b-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="c128b-117">若要匯出金鑰封裝，您必須使用類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c128b-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="c128b-118">*\[ KeyPackage \]*\[out\]</span><span class="sxs-lookup"><span data-stu-id="c128b-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c128b-119">類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="c128b-119">Type: **uint8**</span></span>

<span data-ttu-id="c128b-120">包含磁片區之加密金鑰的位元組資料流程，受指定金鑰保護裝置的保護。</span><span class="sxs-lookup"><span data-stu-id="c128b-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c128b-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="c128b-121">Return value</span></span>

<span data-ttu-id="c128b-122">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="c128b-122">Type: **uint32**</span></span>

<span data-ttu-id="c128b-123">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c128b-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c128b-124">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="c128b-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="c128b-125">Description</span><span class="sxs-lookup"><span data-stu-id="c128b-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c128b-126"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="c128b-127">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="c128b-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="c128b-128"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="c128b-129">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="c128b-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="c128b-130"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="c128b-131">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c128b-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="c128b-132">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="c128b-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="c128b-133"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="c128b-134">提供的金鑰保護裝置不存在於磁片區上。</span><span class="sxs-lookup"><span data-stu-id="c128b-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="c128b-135"><dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="c128b-136">*VolumeKeyProtectorID* 參數未參考類型為「數位密碼」或「外部金鑰」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c128b-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="c128b-137">您可以使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 或 [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) 方法來建立適當類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="c128b-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c128b-138">備註</span><span class="sxs-lookup"><span data-stu-id="c128b-138">Remarks</span></span>

<span data-ttu-id="c128b-139">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="c128b-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c128b-140">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c128b-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c128b-141">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="c128b-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c128b-142">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="c128b-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c128b-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="c128b-143">Requirements</span></span>



| <span data-ttu-id="c128b-144">需求</span><span class="sxs-lookup"><span data-stu-id="c128b-144">Requirement</span></span> | <span data-ttu-id="c128b-145">值</span><span class="sxs-lookup"><span data-stu-id="c128b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c128b-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c128b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="c128b-147">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c128b-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c128b-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c128b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="c128b-149">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c128b-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c128b-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="c128b-150">Namespace</span></span><br/>                | <span data-ttu-id="c128b-151">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c128b-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c128b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="c128b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c128b-153"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="c128b-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c128b-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c128b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c128b-155">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="c128b-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 使用特殊格式的48位數密碼來保護磁片區的加密金鑰。
ms.assetid: 23e0b79a-2feb-441a-9785-7ecd3bb4b6c6
title: Win32_EncryptableVolume 類別的 ProtectKeyWithNumericalPassword 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: fd17727bc71dbbe517b6424135e1205035027a00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850836"
---
# <a name="protectkeywithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fa4dd-103">Win32 EncryptableVolume 類別的 ProtectKeyWithNumericalPassword 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fa4dd-103">ProtectKeyWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fa4dd-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithNumericalPassword** 方法會使用特殊格式化的48位數密碼來保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-104">The **ProtectKeyWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a specially formatted 48-digit password.</span></span> <span data-ttu-id="fa4dd-105">您可以使用此數值密碼從其他金鑰保護裝置的驗證失敗中復原 (例如 TPM) 。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-105">This numerical password can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="fa4dd-106">為磁片區建立類型為「數位密碼」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-106">A key protector of type "Numerical Password" is created for the volume.</span></span>

<span data-ttu-id="fa4dd-107">使用 [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) 方法來驗證數值密碼的格式。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-107">Use the [**IsNumericalPasswordValid**](isnumericalpasswordvalid-win32-encryptablevolume.md) method to validate the format of the numerical password.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa4dd-108">語法</span><span class="sxs-lookup"><span data-stu-id="fa4dd-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithNumericalPassword(
  [in, optional] string FriendlyName,
  [in, optional] string NumericalPassword,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="fa4dd-109">參數</span><span class="sxs-lookup"><span data-stu-id="fa4dd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa4dd-110">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fa4dd-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4dd-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa4dd-111">Type: **string**</span></span>

<span data-ttu-id="fa4dd-112">字串，指定此金鑰保護裝置的使用者指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-112">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="fa4dd-113">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="fa4dd-114">*NumericalPassword* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="fa4dd-114">*NumericalPassword* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4dd-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa4dd-115">Type: **string**</span></span>

<span data-ttu-id="fa4dd-116">字串，指定特殊格式化的48位數數位密碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-116">A string that specifies the specially formatted 48-digit numerical password.</span></span>

<span data-ttu-id="fa4dd-117">數值密碼必須包含48位數。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-117">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="fa4dd-118">這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-118">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="fa4dd-119">6位數的每個群組都必須可以整除11個，且必須小於720896。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-119">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="fa4dd-120">假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-120">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="fa4dd-121">您可以選擇性地以空格或連字號分隔數位群組。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-121">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="fa4dd-122">因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-122">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

<span data-ttu-id="fa4dd-123">如果未指定任何數值密碼，則會隨機產生一個密碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-123">If no numerical password is specified, one is randomly generated.</span></span> <span data-ttu-id="fa4dd-124">使用 [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) 方法來取得隨機產生的密碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-124">Use the [**GetKeyProtectorNumericalPassword**](getkeyprotectornumericalpassword-win32-encryptablevolume.md) method to obtain the randomly generated password.</span></span>

</dd> <dt>

<span data-ttu-id="fa4dd-125">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fa4dd-125">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa4dd-126">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="fa4dd-126">Type: **string**</span></span>

<span data-ttu-id="fa4dd-127">字串，這個字串是與建立的保護裝置相關聯的唯一識別碼，可用於管理金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-127">A string that is the unique identifier associated with the created protector and that can be used to manage the key protector.</span></span>

<span data-ttu-id="fa4dd-128">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-128">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa4dd-129">傳回值</span><span class="sxs-lookup"><span data-stu-id="fa4dd-129">Return value</span></span>

<span data-ttu-id="fa4dd-130">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="fa4dd-130">Type: **uint32**</span></span>

<span data-ttu-id="fa4dd-131">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-131">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fa4dd-132">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="fa4dd-132">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="fa4dd-133">Description</span><span class="sxs-lookup"><span data-stu-id="fa4dd-133">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa4dd-134"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4dd-134"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="fa4dd-135">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-135">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="fa4dd-136"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4dd-136"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="fa4dd-137">*NumericalPassword* 參數的格式無效。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-137">The *NumericalPassword* parameter does not have a valid format.</span></span><br/> |
| <dl> <span data-ttu-id="fa4dd-138"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4dd-138"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="fa4dd-139">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-139">The volume is locked.</span></span><br/>                                           |
| <dl> <span data-ttu-id="fa4dd-140"><dt>**FVE \_E \_ 不正確 \_ 密碼 \_ 格式**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="fa4dd-140"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="fa4dd-141">*NumericalPassword* 參數的格式無效。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-141">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fa4dd-142">備註</span><span class="sxs-lookup"><span data-stu-id="fa4dd-142">Remarks</span></span>

<span data-ttu-id="fa4dd-143">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-143">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fa4dd-144">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-144">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fa4dd-145">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-145">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fa4dd-146">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="fa4dd-146">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa4dd-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa4dd-147">Requirements</span></span>



| <span data-ttu-id="fa4dd-148">需求</span><span class="sxs-lookup"><span data-stu-id="fa4dd-148">Requirement</span></span> | <span data-ttu-id="fa4dd-149">值</span><span class="sxs-lookup"><span data-stu-id="fa4dd-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa4dd-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa4dd-150">Minimum supported client</span></span><br/> | <span data-ttu-id="fa4dd-151">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa4dd-151">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fa4dd-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa4dd-152">Minimum supported server</span></span><br/> | <span data-ttu-id="fa4dd-153">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa4dd-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa4dd-154">命名空間</span><span class="sxs-lookup"><span data-stu-id="fa4dd-154">Namespace</span></span><br/>                | <span data-ttu-id="fa4dd-155">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="fa4dd-155">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fa4dd-156">MOF</span><span class="sxs-lookup"><span data-stu-id="fa4dd-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa4dd-157"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa4dd-157"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa4dd-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa4dd-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa4dd-159">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="fa4dd-159">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

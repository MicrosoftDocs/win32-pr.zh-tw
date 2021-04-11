---
description: 使用提供的數值密碼來存取資料磁片區的內容。
ms.assetid: ee968372-18a4-4748-ab18-2f1b8d297f0e
title: Win32_EncryptableVolume 類別的 UnlockWithNumericalPassword 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 09676e4a57e03f86b18259a7ffb472a6682eafd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847869"
---
# <a name="unlockwithnumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b8ab1-103">Win32 EncryptableVolume 類別的 UnlockWithNumericalPassword 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b8ab1-103">UnlockWithNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b8ab1-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithNumericalPassword** 方法會使用提供的數值密碼來存取資料磁片區的內容。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-104">The **UnlockWithNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided numerical password to access the contents of a data volume.</span></span>

<span data-ttu-id="b8ab1-105">磁片區的加密金鑰必須以「數位密碼」類型的一或多個金鑰保護裝置來保護 (使用 [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) 方法) ，才能使用此方法將磁片區解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-105">The volume's encryption key must have been secured with one or more key protectors of the type "Numerical Password" (by using the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) method) to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="b8ab1-106">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b8ab1-107">語法</span><span class="sxs-lookup"><span data-stu-id="b8ab1-107">Syntax</span></span>


```mof
uint32 UnlockWithNumericalPassword(
  [in] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="b8ab1-108">參數</span><span class="sxs-lookup"><span data-stu-id="b8ab1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8ab1-109">*NumericalPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-109">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8ab1-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b8ab1-110">Type: **string**</span></span>

<span data-ttu-id="b8ab1-111">指定數位密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-111">A string that specifies the numerical password.</span></span>

<span data-ttu-id="b8ab1-112">數值密碼必須包含48位數。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-112">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="b8ab1-113">這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-113">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="b8ab1-114">6位數的每個群組都必須可以整除11個，且必須小於65536。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-114">Each group of 6 digits must be divisible by 11 and must be less than 65536.</span></span> <span data-ttu-id="b8ab1-115">假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-115">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="b8ab1-116">您可以選擇性地以空格或連字號分隔數位群組。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-116">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="b8ab1-117">因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-117">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8ab1-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8ab1-118">Return value</span></span>

<span data-ttu-id="b8ab1-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b8ab1-119">Type: **uint32**</span></span>

<span data-ttu-id="b8ab1-120">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="b8ab1-121">如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回0。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-121">If the volume is already unlocked and no other errors occur, this method returns 0.</span></span>



| <span data-ttu-id="b8ab1-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b8ab1-122">Return code/value</span></span>                                                                                                                                                                             | <span data-ttu-id="b8ab1-123">Description</span><span class="sxs-lookup"><span data-stu-id="b8ab1-123">Description</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b8ab1-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                             | <span data-ttu-id="b8ab1-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-125">The method was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="b8ab1-126"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-126"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>            | <span data-ttu-id="b8ab1-127">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-127">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b8ab1-128">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-128">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                   |
| <dl> <span data-ttu-id="b8ab1-129"><dt>**FVE \_\_ \_ \_ 找不到電子保護**</dt>裝置 <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-129"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>     | <span data-ttu-id="b8ab1-130">磁片區沒有類型為「數位密碼」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-130">The volume does not have a key protector of the type "Numerical Password".</span></span><br/> <span data-ttu-id="b8ab1-131">*NumericalPassword* 參數的格式有效，但您無法使用數值密碼來解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-131">The *NumericalPassword* parameter has a valid format, but you cannot use a numerical password to unlock the volume.</span></span><br/>           |
| <dl> <span data-ttu-id="b8ab1-132"><dt>**FVE \_E \_ \_ 驗證失敗**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-132"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>    | <span data-ttu-id="b8ab1-133">*NumericalPassword* 參數無法解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-133">The *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> <span data-ttu-id="b8ab1-134">有一或多個類型為「數位密碼」的金鑰保護裝置存在，但指定的 *NumericalPassword* 參數無法解除鎖定磁片區。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-134">One or more key protectors of the type "Numerical Password" exist, but the specified *NumericalPassword* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="b8ab1-135"><dt>**FVE \_E \_ 不正確 \_ 密碼 \_ 格式**</dt> <dt>2150694965 (0x80310035)</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-135"><dt>**FVE\_E\_INVALID\_PASSWORD\_FORMAT**</dt> <dt>2150694965 (0x80310035)</dt></span></span> </dl> | <span data-ttu-id="b8ab1-136">*NumericalPassword* 參數的格式無效。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-136">The *NumericalPassword* parameter does not have a valid format.</span></span><br/>                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="b8ab1-137">備註</span><span class="sxs-lookup"><span data-stu-id="b8ab1-137">Remarks</span></span>

<span data-ttu-id="b8ab1-138">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b8ab1-139">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b8ab1-140">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b8ab1-141">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="b8ab1-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ab1-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8ab1-142">Requirements</span></span>



| <span data-ttu-id="b8ab1-143">需求</span><span class="sxs-lookup"><span data-stu-id="b8ab1-143">Requirement</span></span> | <span data-ttu-id="b8ab1-144">值</span><span class="sxs-lookup"><span data-stu-id="b8ab1-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ab1-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8ab1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ab1-146">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-146">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b8ab1-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8ab1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ab1-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b8ab1-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8ab1-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="b8ab1-149">Namespace</span></span><br/>                | <span data-ttu-id="b8ab1-150">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b8ab1-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b8ab1-151">MOF</span><span class="sxs-lookup"><span data-stu-id="b8ab1-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8ab1-152"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8ab1-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ab1-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8ab1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ab1-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b8ab1-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

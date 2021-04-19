---
description: 抓取指定金鑰保護裝置的數值密碼。
ms.assetid: 5c4663fb-285d-471c-b355-82d553a7e686
title: Win32_EncryptableVolume 類別的 GetKeyProtectorNumericalPassword 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorNumericalPassword
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 73a6c774386cd88195074092323969d97f4d7563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970152"
---
# <a name="getkeyprotectornumericalpassword-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2c6dc-103">Win32 EncryptableVolume 類別的 GetKeyProtectorNumericalPassword 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2c6dc-103">GetKeyProtectorNumericalPassword method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2c6dc-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorNumericalPassword** 方法會抓取適當類型之指定金鑰保護裝置的數值密碼。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-104">The **GetKeyProtectorNumericalPassword** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the numerical password for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="2c6dc-105">金鑰保護裝置識別碼必須參考「數位密碼」類型的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-105">The key protector identifier must refer to a key protector of type "Numerical Password".</span></span>

## <a name="syntax"></a><span data-ttu-id="2c6dc-106">語法</span><span class="sxs-lookup"><span data-stu-id="2c6dc-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorNumericalPassword(
  [in]  string VolumeKeyProtectorID,
  [out] string NumericalPassword
);
```



## <a name="parameters"></a><span data-ttu-id="2c6dc-107">參數</span><span class="sxs-lookup"><span data-stu-id="2c6dc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6dc-108">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c6dc-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6dc-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c6dc-109">Type: **string**</span></span>

<span data-ttu-id="2c6dc-110">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="2c6dc-111">*NumericalPassword* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c6dc-111">*NumericalPassword* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6dc-112">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="2c6dc-112">Type: **string**</span></span>

<span data-ttu-id="2c6dc-113">表示可以用來解除鎖定對應磁片區之密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-113">A string that represents the password that can be used to unlock the corresponding volume.</span></span>

<span data-ttu-id="2c6dc-114">數值密碼是48位數。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-114">The numerical password is 48 digits.</span></span> <span data-ttu-id="2c6dc-115">這些數位分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-115">These digits are divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="2c6dc-116">假設有六個數字的群組標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-116">Assuming that a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="2c6dc-117">數位群組以連字號分隔。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-117">The groups of digits are separated by a hyphen.</span></span> <span data-ttu-id="2c6dc-118">因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 是所傳回密碼的格式。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-118">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" is the format of the returned password.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c6dc-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c6dc-119">Return value</span></span>

<span data-ttu-id="2c6dc-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="2c6dc-120">Type: **uint32**</span></span>

<span data-ttu-id="2c6dc-121">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="2c6dc-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="2c6dc-122">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2c6dc-123">Description</span><span class="sxs-lookup"><span data-stu-id="2c6dc-123">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c6dc-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6dc-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2c6dc-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-125">The method was successful.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="2c6dc-126"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6dc-126"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2c6dc-127">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-127">The volume is locked.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="2c6dc-128"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6dc-128"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="2c6dc-129">*VolumeKeyProtectorID* 參數未參考類型為「數位密碼」的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-129">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password".</span></span><br/> |
| <dl> <span data-ttu-id="2c6dc-130"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="2c6dc-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="2c6dc-131">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="2c6dc-132">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-132">Add a key protector to enable BitLocker.</span></span> <br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="2c6dc-133">備註</span><span class="sxs-lookup"><span data-stu-id="2c6dc-133">Remarks</span></span>

<span data-ttu-id="2c6dc-134">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2c6dc-135">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2c6dc-136">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2c6dc-137">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="2c6dc-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c6dc-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c6dc-138">Requirements</span></span>



| <span data-ttu-id="2c6dc-139">需求</span><span class="sxs-lookup"><span data-stu-id="2c6dc-139">Requirement</span></span> | <span data-ttu-id="2c6dc-140">值</span><span class="sxs-lookup"><span data-stu-id="2c6dc-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c6dc-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c6dc-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2c6dc-142">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c6dc-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2c6dc-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c6dc-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2c6dc-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c6dc-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c6dc-145">命名空間</span><span class="sxs-lookup"><span data-stu-id="2c6dc-145">Namespace</span></span><br/>                | <span data-ttu-id="2c6dc-146">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2c6dc-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2c6dc-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2c6dc-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c6dc-148"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c6dc-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c6dc-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c6dc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c6dc-150">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="2c6dc-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

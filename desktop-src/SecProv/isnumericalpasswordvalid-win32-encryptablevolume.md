---
description: 指出數值密碼是否符合此驗證值的特殊格式需求。
ms.assetid: 3995405f-db4d-4f72-98dc-133a09f9cf65
title: Win32_EncryptableVolume 類別的 IsNumericalPasswordValid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsNumericalPasswordValid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7cec4aa31ae9ff6aee90c0f46ded935b3d553783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988318"
---
# <a name="isnumericalpasswordvalid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6e0e7-103">Win32 EncryptableVolume 類別的 IsNumericalPasswordValid 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6e0e7-103">IsNumericalPasswordValid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6e0e7-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsNumericalPasswordValid** 方法會指出數值密碼是否符合此驗證值的特殊格式需求。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-104">The **IsNumericalPasswordValid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the numerical password meets the special format requirements for this authentication value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e0e7-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e0e7-105">Syntax</span></span>


```mof
uint32 IsNumericalPasswordValid(
  [in]  string  NumericalPassword,
  [out] boolean IsNumericalPasswordValid
);
```



## <a name="parameters"></a><span data-ttu-id="6e0e7-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e0e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e0e7-107">*NumericalPassword* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e0e7-107">*NumericalPassword* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0e7-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="6e0e7-108">Type: **string**</span></span>

<span data-ttu-id="6e0e7-109">指定數位密碼的字串。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-109">A string that specifies the numerical password.</span></span>

<span data-ttu-id="6e0e7-110">數值密碼必須包含48位數。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-110">The numerical password must contain 48 digits.</span></span> <span data-ttu-id="6e0e7-111">這些數位可以分為6位數的8個群組，每個群組中的最後一個數位指出群組的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-111">These digits can be divided into 8 groups of 6 digits, with the last digit in each group indicating a checksum value for the group.</span></span> <span data-ttu-id="6e0e7-112">6位數的每個群組都必須可以整除11個，且必須小於720896。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-112">Each group of 6 digits must be divisible by 11 and must be less than 720896.</span></span> <span data-ttu-id="6e0e7-113">假設有一組六位數標示為 x1、x2、x3、x4、x5 和 x6，則總和檢查碼 x6 數位的計算方式為– x1 + x2 – x3 + x4 – x5 mod 11。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-113">Assuming a group of six digits is labeled as x1, x2, x3, x4, x5, and x6, the checksum x6 digit is calculated as –x1+x2–x3+x4–x5 mod 11.</span></span>

<span data-ttu-id="6e0e7-114">您可以選擇性地以空格或連字號分隔數位群組。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-114">The groups of digits can optionally be separated by a space or hyphen.</span></span> <span data-ttu-id="6e0e7-115">因此，"xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" 或 "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" 也可能包含有效的數值密碼。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-115">Therefore, "xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx-xxxxxx" or "xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx xxxxxx" may also contain valid numerical passwords.</span></span>

</dd> <dt>

<span data-ttu-id="6e0e7-116">*IsNumericalPasswordValid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6e0e7-116">*IsNumericalPasswordValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e0e7-117">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="6e0e7-117">Type: **boolean**</span></span>

<span data-ttu-id="6e0e7-118">如果數值密碼符合此驗證值的特殊格式需求，則布林值為 true，否則值為 false。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-118">A Boolean value that is true if the numerical password meets the special format requirements for this authentication value, otherwise the value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e0e7-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e0e7-119">Return value</span></span>

<span data-ttu-id="6e0e7-120">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="6e0e7-120">Type: **uint32**</span></span>

<span data-ttu-id="6e0e7-121">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-121">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6e0e7-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="6e0e7-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="6e0e7-123">Description</span><span class="sxs-lookup"><span data-stu-id="6e0e7-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6e0e7-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6e0e7-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="6e0e7-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e0e7-126">備註</span><span class="sxs-lookup"><span data-stu-id="6e0e7-126">Remarks</span></span>

<span data-ttu-id="6e0e7-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6e0e7-128">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6e0e7-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6e0e7-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="6e0e7-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6e0e7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e0e7-131">Requirements</span></span>



| <span data-ttu-id="6e0e7-132">需求</span><span class="sxs-lookup"><span data-stu-id="6e0e7-132">Requirement</span></span> | <span data-ttu-id="6e0e7-133">值</span><span class="sxs-lookup"><span data-stu-id="6e0e7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e0e7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e0e7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6e0e7-135">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e0e7-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6e0e7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e0e7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6e0e7-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e0e7-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e0e7-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="6e0e7-138">Namespace</span></span><br/>                | <span data-ttu-id="6e0e7-139">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6e0e7-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6e0e7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6e0e7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e0e7-141"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="6e0e7-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e0e7-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e0e7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e0e7-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="6e0e7-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

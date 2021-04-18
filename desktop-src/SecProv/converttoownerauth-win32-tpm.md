---
description: 將使用者提供的複雜密碼輸入轉譯為20位元組的擁有者授權，可用來與 TPM 互動。 TakeOwnership 和 ResetAuthLockOut 等方法都需要產生的擁有者授權值。
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Win32_Tpm 類別的 ConvertToOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971488"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="e3fe6-104">Win32 Tpm 類別的 ConvertToOwnerAuth 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e3fe6-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="e3fe6-105">[**Win32 \_ Tpm**](win32-tpm.md)類別的 **ConvertToOwnerAuth** 方法會將使用者提供的複雜密碼輸入轉譯為20位元組的擁有者授權，以用來與 Tpm 互動。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="e3fe6-106">[**TakeOwnership**](takeownership-win32-tpm.md)和 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)等方法都需要產生的擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="e3fe6-107">轉換程式會遵循來自 [信任運算群組](https://www.trustedcomputinggroup.org/)的規格。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3fe6-108">語法</span><span class="sxs-lookup"><span data-stu-id="e3fe6-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="e3fe6-109">參數</span><span class="sxs-lookup"><span data-stu-id="e3fe6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3fe6-110">*OwnerPassPhrase* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e3fe6-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3fe6-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3fe6-111">Type: **string**</span></span>

<span data-ttu-id="e3fe6-112">要轉換為擁有者授權值的字串。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="e3fe6-113">字串可以包含任何數目的英數位元。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="e3fe6-114">*OwnerAuth* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e3fe6-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3fe6-115">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="e3fe6-115">Type: **string**</span></span>

<span data-ttu-id="e3fe6-116">衍生自 *OwnerPassPhrase* 參數的字串。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="e3fe6-117">這個值是20位元組的二進位值，編碼為28位元組 base64 以 **null** 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3fe6-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3fe6-118">Return value</span></span>

<span data-ttu-id="e3fe6-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e3fe6-119">Type: **uint32**</span></span>

<span data-ttu-id="e3fe6-120">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="e3fe6-121">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="e3fe6-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e3fe6-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="e3fe6-123">Description</span><span class="sxs-lookup"><span data-stu-id="e3fe6-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e3fe6-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e3fe6-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e3fe6-125">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3fe6-126">備註</span><span class="sxs-lookup"><span data-stu-id="e3fe6-126">Remarks</span></span>

<span data-ttu-id="e3fe6-127">Unicode UTF-16LE 編碼的字串會藉由取得字串二進位標記法的 SHA-1 雜湊，轉換成20位元組的 TPM 擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="e3fe6-128">Unicode 字串的 **null** 終止不包含在雜湊中。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="e3fe6-129">SHA-1 雜湊中未使用 salt。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="e3fe6-130">例如，若要將 TPM 擁有者複雜密碼 "1Sample" 轉換成 TPM 擁有者授權值，則會從下列位元組資料流程取得 SHA-1 雜湊：</span><span class="sxs-lookup"><span data-stu-id="e3fe6-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="e3fe6-131">為了將零長度的複雜密碼轉換成擁有者授權值，會採用 **Null** 位元組資料流程的 sha-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="e3fe6-132">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e3fe6-133">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e3fe6-134">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e3fe6-135">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="e3fe6-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3fe6-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3fe6-136">Requirements</span></span>



| <span data-ttu-id="e3fe6-137">需求</span><span class="sxs-lookup"><span data-stu-id="e3fe6-137">Requirement</span></span> | <span data-ttu-id="e3fe6-138">值</span><span class="sxs-lookup"><span data-stu-id="e3fe6-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3fe6-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e3fe6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e3fe6-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3fe6-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e3fe6-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e3fe6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e3fe6-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e3fe6-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e3fe6-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="e3fe6-143">Namespace</span></span><br/>                | <span data-ttu-id="e3fe6-144">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="e3fe6-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="e3fe6-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e3fe6-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3fe6-146"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3fe6-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3fe6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e3fe6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3fe6-148"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3fe6-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3fe6-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3fe6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3fe6-150">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="e3fe6-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="e3fe6-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="e3fe6-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 

---
description: 安裝 TPM 的擁有者。
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Win32_Tpm 類別的 TakeOwnership 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027396"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="9610f-103">Win32 Tpm 類別的 TakeOwnership 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9610f-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9610f-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **TAKEOWNERSHIP** 方法會安裝 Tpm 的擁有者。</span><span class="sxs-lookup"><span data-stu-id="9610f-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="9610f-105">TPM 的擁有者可完全使用 TPM 功能。</span><span class="sxs-lookup"><span data-stu-id="9610f-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="9610f-106">設定擁有者之後，沒有其他使用者或軟體可以宣告 TPM 的擁有權。</span><span class="sxs-lookup"><span data-stu-id="9610f-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="9610f-107">[**IsEnabled**](isenabled-win32-tpm.md)、 [**IsActivated**](isactivated-win32-tpm.md)和 [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)方法都必須是 true，才能成功進行 **TakeOwnership** 方法。</span><span class="sxs-lookup"><span data-stu-id="9610f-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9610f-108">語法</span><span class="sxs-lookup"><span data-stu-id="9610f-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="9610f-109">參數</span><span class="sxs-lookup"><span data-stu-id="9610f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9610f-110">*OwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="9610f-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9610f-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="9610f-111">Type: **string**</span></span>

<span data-ttu-id="9610f-112">識別 TPM 擁有者的字串。</span><span class="sxs-lookup"><span data-stu-id="9610f-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="9610f-113">此字串必須是 base64 編碼的 null 終止字串，其中包含剛好20個位元組的二進位資料。</span><span class="sxs-lookup"><span data-stu-id="9610f-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="9610f-114">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼轉譯為此預期的格式。</span><span class="sxs-lookup"><span data-stu-id="9610f-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="9610f-115">如果未提供任何參數，則會從登錄讀取 *OwnerAuth* 參數。</span><span class="sxs-lookup"><span data-stu-id="9610f-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9610f-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="9610f-116">Return value</span></span>

<span data-ttu-id="9610f-117">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="9610f-117">Type: **uint32**</span></span>

<span data-ttu-id="9610f-118">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="9610f-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9610f-119">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="9610f-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="9610f-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="9610f-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="9610f-121">Description</span><span class="sxs-lookup"><span data-stu-id="9610f-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9610f-122"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="9610f-123">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="9610f-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="9610f-124"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="9610f-125">*OwnerAuth* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="9610f-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="9610f-126"><dt>**TPM \_E \_ 擁有者 \_ 設定**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="9610f-127">TPM 上已有擁有者。</span><span class="sxs-lookup"><span data-stu-id="9610f-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="9610f-128"><dt>**TPM \_E \_ NO \_ 背書**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="9610f-129">在 TPM 上找不到簽署金鑰。</span><span class="sxs-lookup"><span data-stu-id="9610f-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="9610f-130">若要在 TPM 上建立簽署金鑰組，請參閱 [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9610f-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="9610f-131"><dt>**TPM \_E \_ 安裝 \_ 已停用**</dt>的 <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="9610f-132">無法在此 TPM 上安裝擁有者。</span><span class="sxs-lookup"><span data-stu-id="9610f-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="9610f-133">如需如何允許安裝裝置擁有者的相關資訊，請參閱 [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)。</span><span class="sxs-lookup"><span data-stu-id="9610f-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="9610f-134"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="9610f-135">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="9610f-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="9610f-136">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9610f-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="9610f-137">備註</span><span class="sxs-lookup"><span data-stu-id="9610f-137">Remarks</span></span>

<span data-ttu-id="9610f-138">[**IsEnabled**](isenabled-win32-tpm.md)、 [**IsActivated**](isactivated-win32-tpm.md)和 [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)方法都必須為 true，才能成功完成 **TakeOwnership** 。</span><span class="sxs-lookup"><span data-stu-id="9610f-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="9610f-139">您應該使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將複雜密碼變更為用於 *OwnerAuth* 參數的輸入值。</span><span class="sxs-lookup"><span data-stu-id="9610f-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="9610f-140">如果已設定適當的群組原則設定， **TakeOwnership** 方法會將擁有者授權值備份至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="9610f-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="9610f-141">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9610f-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9610f-142">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9610f-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9610f-143">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9610f-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9610f-144">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="9610f-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9610f-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="9610f-145">Requirements</span></span>



| <span data-ttu-id="9610f-146">需求</span><span class="sxs-lookup"><span data-stu-id="9610f-146">Requirement</span></span> | <span data-ttu-id="9610f-147">值</span><span class="sxs-lookup"><span data-stu-id="9610f-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9610f-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9610f-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9610f-149">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9610f-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9610f-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9610f-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9610f-151">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9610f-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9610f-152">命名空間</span><span class="sxs-lookup"><span data-stu-id="9610f-152">Namespace</span></span><br/>                | <span data-ttu-id="9610f-153">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="9610f-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9610f-154">MOF</span><span class="sxs-lookup"><span data-stu-id="9610f-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9610f-155"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9610f-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9610f-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9610f-157"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9610f-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9610f-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9610f-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9610f-159">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="9610f-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

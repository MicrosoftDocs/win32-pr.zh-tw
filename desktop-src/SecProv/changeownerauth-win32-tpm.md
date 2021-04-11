---
description: 變更 TPM 擁有者授權值。
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Win32_Tpm 類別的 ChangeOwnerAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112644"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="0c75e-103">Win32 Tpm 類別的 ChangeOwnerAuth 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0c75e-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="0c75e-104">[**Win32 \_ tpm**](win32-tpm.md)類別的 **CHANGEOWNERAUTH** 方法會變更 Tpm 擁有者授權值。</span><span class="sxs-lookup"><span data-stu-id="0c75e-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c75e-105">語法</span><span class="sxs-lookup"><span data-stu-id="0c75e-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="0c75e-106">參數</span><span class="sxs-lookup"><span data-stu-id="0c75e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c75e-107">*OldOwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0c75e-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c75e-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c75e-108">Type: **string**</span></span>

<span data-ttu-id="0c75e-109">為裝置的目前 TPM 擁有者授權值命名的字串。</span><span class="sxs-lookup"><span data-stu-id="0c75e-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="0c75e-110">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將密碼轉譯為此授權值。</span><span class="sxs-lookup"><span data-stu-id="0c75e-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="0c75e-111">未提供 *OldOwnerAuth* 參數或提供空字串，這個方法會從登錄中取得值（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="0c75e-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="0c75e-112">*NewOwnerAuth* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="0c75e-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0c75e-113">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="0c75e-113">Type: **string**</span></span>

<span data-ttu-id="0c75e-114">為新的 TPM 擁有者授權值命名的字串。</span><span class="sxs-lookup"><span data-stu-id="0c75e-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="0c75e-115">使用 [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) 方法，將密碼轉譯為此授權值。</span><span class="sxs-lookup"><span data-stu-id="0c75e-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="0c75e-116">*NewOwnerAuth* 參數不可為空白或 **Null。**</span><span class="sxs-lookup"><span data-stu-id="0c75e-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c75e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="0c75e-117">Return value</span></span>

<span data-ttu-id="0c75e-118">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="0c75e-118">Type: **uint32**</span></span>

<span data-ttu-id="0c75e-119">您可以傳回所有 TPM 錯誤以及 TPM 基礎服務特定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="0c75e-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="0c75e-120">下表列出一些常見的傳回碼。</span><span class="sxs-lookup"><span data-stu-id="0c75e-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="0c75e-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="0c75e-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="0c75e-122">Description</span><span class="sxs-lookup"><span data-stu-id="0c75e-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0c75e-123"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="0c75e-124">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="0c75e-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="0c75e-125"><dt>**TPM \_E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="0c75e-126">目前的 TPM 擁有者授權值不正確。</span><span class="sxs-lookup"><span data-stu-id="0c75e-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="0c75e-127"><dt>**TPM \_E \_ a \_ 防護 \_ 鎖定**</dt>執行 <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="0c75e-128">TPM 會防禦字典攻擊，並在一段時間內進行。</span><span class="sxs-lookup"><span data-stu-id="0c75e-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="0c75e-129">如需詳細資訊，請參閱 [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="0c75e-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="0c75e-130"><dt>**FVE \_E \_ AD \_ 架構 \_ 未 \_ 安裝**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="0c75e-131">無法將修復資訊儲存到網路。</span><span class="sxs-lookup"><span data-stu-id="0c75e-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="0c75e-132">電腦已設定為將修復資訊儲存至 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="0c75e-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="0c75e-133">如需有關如何設定 Active Directory 的指示，請參閱 [BitLocker 磁碟機加密設定指南：將 BitLocker 和 TPM 修復資訊備份至 Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10))。</span><span class="sxs-lookup"><span data-stu-id="0c75e-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="0c75e-134"><dt>**連接失敗**</dt> <dt>2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="0c75e-135">無法將修復資訊儲存到網路。</span><span class="sxs-lookup"><span data-stu-id="0c75e-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="0c75e-136">電腦已設定為將修復資訊儲存至 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="0c75e-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="0c75e-137">需要網路連接才能繼續。</span><span class="sxs-lookup"><span data-stu-id="0c75e-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="0c75e-138">備註</span><span class="sxs-lookup"><span data-stu-id="0c75e-138">Remarks</span></span>

<span data-ttu-id="0c75e-139">如果已設定適當的群組原則設定， **ChangeOwnerAuth** 方法會將新的 TPM 擁有者授權備份至 Active Directory Domain Services。</span><span class="sxs-lookup"><span data-stu-id="0c75e-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="0c75e-140">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0c75e-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0c75e-141">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0c75e-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0c75e-142">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0c75e-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0c75e-143">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="0c75e-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c75e-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c75e-144">Requirements</span></span>



| <span data-ttu-id="0c75e-145">需求</span><span class="sxs-lookup"><span data-stu-id="0c75e-145">Requirement</span></span> | <span data-ttu-id="0c75e-146">值</span><span class="sxs-lookup"><span data-stu-id="0c75e-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c75e-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c75e-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0c75e-148">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c75e-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0c75e-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c75e-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0c75e-150">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c75e-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0c75e-151">命名空間</span><span class="sxs-lookup"><span data-stu-id="0c75e-151">Namespace</span></span><br/>                | <span data-ttu-id="0c75e-152">根 \\ CIMV2 \\ 安全性 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="0c75e-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="0c75e-153">MOF</span><span class="sxs-lookup"><span data-stu-id="0c75e-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c75e-154"><dt>Win32 \_ tpm。 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c75e-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0c75e-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c75e-156"><dt>Win32 \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c75e-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c75e-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c75e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c75e-158">**Win32 \_ Tpm**</span><span class="sxs-lookup"><span data-stu-id="0c75e-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 

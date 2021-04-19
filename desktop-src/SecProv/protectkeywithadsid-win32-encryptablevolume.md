---
description: 使用 Active Directory 的安全識別碼 (SID) 來保護磁片區的加密金鑰。
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Win32_EncryptableVolume 類別的 ProtectKeyWithAdSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990350"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="89bf4-103">Win32 EncryptableVolume 類別的 ProtectKeyWithAdSid 方法 \_</span><span class="sxs-lookup"><span data-stu-id="89bf4-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="89bf4-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ProtectKeyWithAdSid** 方法會使用 ACTIVE DIRECTORY 的安全識別碼 (SID) 來保護磁片區的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="89bf4-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="89bf4-105">語法</span><span class="sxs-lookup"><span data-stu-id="89bf4-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="89bf4-106">參數</span><span class="sxs-lookup"><span data-stu-id="89bf4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89bf4-107">*FriendlyName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="89bf4-108">字串，指定此金鑰保護裝置的使用者指派識別碼。</span><span class="sxs-lookup"><span data-stu-id="89bf4-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="89bf4-109">如果未指定此參數，則會使用空白值。</span><span class="sxs-lookup"><span data-stu-id="89bf4-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="89bf4-110">*SidString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89bf4-111">包含用來保護加密金鑰之 Active Directory SID 的字串。</span><span class="sxs-lookup"><span data-stu-id="89bf4-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="89bf4-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89bf4-113">變更函數行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="89bf4-113">Flags that change the function behavior.</span></span> <span data-ttu-id="89bf4-114">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="89bf4-114">This can be one of the following values.</span></span>



| <span data-ttu-id="89bf4-115">值</span><span class="sxs-lookup"><span data-stu-id="89bf4-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="89bf4-116">意義</span><span class="sxs-lookup"><span data-stu-id="89bf4-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="89bf4-117"><dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 無**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="89bf4-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="89bf4-118">沒有影響。</span><span class="sxs-lookup"><span data-stu-id="89bf4-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="89bf4-119"><dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 解除鎖定 \_ 為 \_ 服務 \_ 帳戶**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="89bf4-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="89bf4-120">指定以 SID 為基礎的保護裝置受到服務帳戶的保護。</span><span class="sxs-lookup"><span data-stu-id="89bf4-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="89bf4-121">如果指定此旗標，呼叫端應該先確認它是以適當的服務帳戶執行，然後再藉由暫時卸載模擬來呼叫 [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (，例如) 。</span><span class="sxs-lookup"><span data-stu-id="89bf4-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="89bf4-122">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89bf4-123">與建立的保護裝置相關聯的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="89bf4-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="89bf4-124">您可以使用此字串來管理金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="89bf4-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="89bf4-125">如果磁片磁碟機支援硬體加密，且 BitLocker 未採用頻外擁有權，則識別碼字串會設定為 "BitLocker"，且金鑰保護裝置會寫入每個頻外中繼資料。</span><span class="sxs-lookup"><span data-stu-id="89bf4-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89bf4-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="89bf4-126">Return value</span></span>

<span data-ttu-id="89bf4-127">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="89bf4-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="89bf4-128">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="89bf4-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="89bf4-129">Description</span><span class="sxs-lookup"><span data-stu-id="89bf4-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="89bf4-130"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="89bf4-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="89bf4-131">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="89bf4-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89bf4-132">備註</span><span class="sxs-lookup"><span data-stu-id="89bf4-132">Remarks</span></span>

<span data-ttu-id="89bf4-133">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="89bf4-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="89bf4-134">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="89bf4-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="89bf4-135">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="89bf4-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="89bf4-136">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)</span><span class="sxs-lookup"><span data-stu-id="89bf4-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="89bf4-137">根據預設，您無法從遠端新增 Active Directory 帳戶或群組保護裝置。</span><span class="sxs-lookup"><span data-stu-id="89bf4-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="89bf4-138">您必須在網域控制站和來源電腦上啟用限制委派。</span><span class="sxs-lookup"><span data-stu-id="89bf4-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="89bf4-139">在網域控制站上，執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="89bf4-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="89bf4-140">開啟伺服器管理員</span><span class="sxs-lookup"><span data-stu-id="89bf4-140">Open Server Manager</span></span>
2.  <span data-ttu-id="89bf4-141">選取 Active Directory 角色的電腦</span><span class="sxs-lookup"><span data-stu-id="89bf4-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="89bf4-142">選取目標用戶端電腦，然後以滑鼠右鍵按一下</span><span class="sxs-lookup"><span data-stu-id="89bf4-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="89bf4-143">選取 [委派] 索引標籤</span><span class="sxs-lookup"><span data-stu-id="89bf4-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="89bf4-144">選取 [信任這台電腦，但只委派指定的服務] 選項按鈕</span><span class="sxs-lookup"><span data-stu-id="89bf4-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="89bf4-145">選取 [僅使用 Kerberos] 選項按鈕</span><span class="sxs-lookup"><span data-stu-id="89bf4-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="89bf4-146">按一下 [新增]</span><span class="sxs-lookup"><span data-stu-id="89bf4-146">Click Add</span></span>
8.  <span data-ttu-id="89bf4-147">選取 [使用者或電腦]</span><span class="sxs-lookup"><span data-stu-id="89bf4-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="89bf4-148">選取主機/作為服務主體名稱</span><span class="sxs-lookup"><span data-stu-id="89bf4-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="89bf4-149">在來源電腦上執行步驟3到步驟9。</span><span class="sxs-lookup"><span data-stu-id="89bf4-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="89bf4-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="89bf4-150">Requirements</span></span>



| <span data-ttu-id="89bf4-151">需求</span><span class="sxs-lookup"><span data-stu-id="89bf4-151">Requirement</span></span> | <span data-ttu-id="89bf4-152">值</span><span class="sxs-lookup"><span data-stu-id="89bf4-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89bf4-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89bf4-153">Minimum supported client</span></span><br/> | <span data-ttu-id="89bf4-154">Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89bf4-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89bf4-155">Minimum supported server</span></span><br/> | <span data-ttu-id="89bf4-156">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="89bf4-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="89bf4-157">命名空間</span><span class="sxs-lookup"><span data-stu-id="89bf4-157">Namespace</span></span><br/>                | <span data-ttu-id="89bf4-158">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="89bf4-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="89bf4-159">MOF</span><span class="sxs-lookup"><span data-stu-id="89bf4-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89bf4-160"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="89bf4-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89bf4-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89bf4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89bf4-162">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="89bf4-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

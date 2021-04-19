---
description: 抓取用來保護金鑰的安全識別碼和旗標。
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Win32_EncryptableVolume 類別的 GetKeyProtectorAdSidInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106993690"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="19de1-103">Win32 EncryptableVolume 類別的 GetKeyProtectorAdSidInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="19de1-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="19de1-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorAdSidInformation** 方法會抓取用來保護金鑰的安全識別碼和旗標。</span><span class="sxs-lookup"><span data-stu-id="19de1-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="19de1-105">語法</span><span class="sxs-lookup"><span data-stu-id="19de1-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="19de1-106">參數</span><span class="sxs-lookup"><span data-stu-id="19de1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19de1-107">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19de1-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19de1-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19de1-108">Type: **string**</span></span>

<span data-ttu-id="19de1-109">可以用來管理加密磁片區金鑰保護裝置的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="19de1-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="19de1-110">*SidString* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19de1-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19de1-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="19de1-111">Type: **string**</span></span>

<span data-ttu-id="19de1-112">字串，其中包含 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="19de1-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="19de1-113">*旗標* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19de1-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19de1-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="19de1-114">Type: **uint32**</span></span>

<span data-ttu-id="19de1-115">變更函數行為的旗標。</span><span class="sxs-lookup"><span data-stu-id="19de1-115">Flags that change the function behavior.</span></span> <span data-ttu-id="19de1-116">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="19de1-116">This can be one of the following values.</span></span>



| <span data-ttu-id="19de1-117">值</span><span class="sxs-lookup"><span data-stu-id="19de1-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="19de1-118">意義</span><span class="sxs-lookup"><span data-stu-id="19de1-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="19de1-119"><dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 無**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="19de1-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="19de1-120">沒有影響。</span><span class="sxs-lookup"><span data-stu-id="19de1-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="19de1-121"><dt>**FVE \_DPAPI \_ NG \_ 旗標 \_ 解除鎖定 \_ 為 \_ 服務 \_ 帳戶**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="19de1-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="19de1-122">指定以 SID 為基礎的保護裝置受到服務帳戶的保護。</span><span class="sxs-lookup"><span data-stu-id="19de1-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="19de1-123">如果指定此旗標，呼叫端應該先確認它是以適當的服務帳戶執行，然後再藉由暫時卸載模擬來呼叫 [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (，例如) 。</span><span class="sxs-lookup"><span data-stu-id="19de1-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19de1-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="19de1-124">Return value</span></span>

<span data-ttu-id="19de1-125">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="19de1-125">Type: **uint32**</span></span>

<span data-ttu-id="19de1-126">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19de1-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="19de1-127">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="19de1-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="19de1-128">Description</span><span class="sxs-lookup"><span data-stu-id="19de1-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="19de1-129"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="19de1-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="19de1-130">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="19de1-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19de1-131">備註</span><span class="sxs-lookup"><span data-stu-id="19de1-131">Remarks</span></span>

<span data-ttu-id="19de1-132">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="19de1-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="19de1-133">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="19de1-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="19de1-134">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="19de1-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="19de1-135">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="19de1-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19de1-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="19de1-136">Requirements</span></span>



| <span data-ttu-id="19de1-137">需求</span><span class="sxs-lookup"><span data-stu-id="19de1-137">Requirement</span></span> | <span data-ttu-id="19de1-138">值</span><span class="sxs-lookup"><span data-stu-id="19de1-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19de1-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19de1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="19de1-140">Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19de1-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="19de1-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19de1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="19de1-142">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19de1-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19de1-143">命名空間</span><span class="sxs-lookup"><span data-stu-id="19de1-143">Namespace</span></span><br/>                | <span data-ttu-id="19de1-144">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="19de1-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="19de1-145">MOF</span><span class="sxs-lookup"><span data-stu-id="19de1-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19de1-146"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="19de1-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19de1-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19de1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19de1-148">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="19de1-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 指出磁片區載入時是否自動解除鎖定。
ms.assetid: cba04d77-1e7c-4191-8eb7-b8c43694193f
title: Win32_EncryptableVolume 類別的 IsAutoUnlockEnabled 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsAutoUnlockEnabled
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2a144d54ff4564fa322efadd521e44c2fa9a8173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972189"
---
# <a name="isautounlockenabled-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="93507-103">Win32 EncryptableVolume 類別的 IsAutoUnlockEnabled 方法 \_</span><span class="sxs-lookup"><span data-stu-id="93507-103">IsAutoUnlockEnabled method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="93507-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **IsAutoUnlockEnabled** 方法會指出磁片區掛接時是否自動解除鎖定 (例如，卸載式記憶體裝置連接到電腦) 時。</span><span class="sxs-lookup"><span data-stu-id="93507-104">The **IsAutoUnlockEnabled** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether the volume is automatically unlocked when it is mounted (for example, when removable memory devices are connected to the computer).</span></span>

## <a name="syntax"></a><span data-ttu-id="93507-105">語法</span><span class="sxs-lookup"><span data-stu-id="93507-105">Syntax</span></span>


```mof
uint32 IsAutoUnlockEnabled(
  [out] boolean IsAutoUnlockEnabled,
  [out] string  VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="93507-106">參數</span><span class="sxs-lookup"><span data-stu-id="93507-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93507-107">*IsAutoUnlockEnabled* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93507-107">*IsAutoUnlockEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93507-108">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="93507-108">Type: **boolean**</span></span>

<span data-ttu-id="93507-109">布林值，如果用來自動解除鎖定磁片區的外部金鑰存在，而且已儲存在目前正在執行的作業系統磁片區中，則為 true，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="93507-109">A Boolean value that is true if the external key used to automatically unlock the volume exists and has been stored in the currently running operating system volume, otherwise it is false.</span></span>

</dd> <dt>

<span data-ttu-id="93507-110">*VolumeKeyProtectorID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="93507-110">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="93507-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="93507-111">Type: **string**</span></span>

<span data-ttu-id="93507-112">唯一的字串識別碼，如果 *IsAutoUnlockEnabled* 為 true，則包含相關聯的加密磁片區金鑰保護裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="93507-112">A unique string identifier that contains the associated encrypted volume key protector ID if *IsAutoUnlockEnabled* is true.</span></span>

<span data-ttu-id="93507-113">如果 *IsAutoUnlockEnabled* 為 false，則 *VolumeKeyProtectorID* 為空字串。</span><span class="sxs-lookup"><span data-stu-id="93507-113">If *IsAutoUnlockEnabled* is false, *VolumeKeyProtectorID* is an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93507-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="93507-114">Return value</span></span>

<span data-ttu-id="93507-115">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="93507-115">Type: **uint32**</span></span>

<span data-ttu-id="93507-116">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="93507-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="93507-117">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="93507-117">Return code/value</span></span>                                                                                                                                                                     | <span data-ttu-id="93507-118">Description</span><span class="sxs-lookup"><span data-stu-id="93507-118">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93507-119"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="93507-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                     | <span data-ttu-id="93507-120">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="93507-120">The method was successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="93507-121"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="93507-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>    | <span data-ttu-id="93507-122">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="93507-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="93507-123">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="93507-123">Add a key protector to enable BitLocker.</span></span><br/> |
| <dl> <span data-ttu-id="93507-124"><dt>**FVE \_E \_ NOT \_ DATA \_ VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span><span class="sxs-lookup"><span data-stu-id="93507-124"><dt>**FVE\_E\_NOT\_DATA\_VOLUME**</dt> <dt>2150694937 (0x80310019)</dt></span></span> </dl> | <span data-ttu-id="93507-125">無法針對目前正在執行的作業系統磁片區執行此方法。</span><span class="sxs-lookup"><span data-stu-id="93507-125">The method cannot be run for the currently running operating system volume.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="93507-126">備註</span><span class="sxs-lookup"><span data-stu-id="93507-126">Remarks</span></span>

<span data-ttu-id="93507-127">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="93507-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="93507-128">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="93507-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="93507-129">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="93507-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="93507-130">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="93507-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93507-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="93507-131">Requirements</span></span>



| <span data-ttu-id="93507-132">需求</span><span class="sxs-lookup"><span data-stu-id="93507-132">Requirement</span></span> | <span data-ttu-id="93507-133">值</span><span class="sxs-lookup"><span data-stu-id="93507-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93507-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93507-134">Minimum supported client</span></span><br/> | <span data-ttu-id="93507-135">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93507-135">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="93507-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93507-136">Minimum supported server</span></span><br/> | <span data-ttu-id="93507-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93507-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93507-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="93507-138">Namespace</span></span><br/>                | <span data-ttu-id="93507-139">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="93507-139">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="93507-140">MOF</span><span class="sxs-lookup"><span data-stu-id="93507-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93507-141"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="93507-141"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93507-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93507-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93507-143">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="93507-143">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

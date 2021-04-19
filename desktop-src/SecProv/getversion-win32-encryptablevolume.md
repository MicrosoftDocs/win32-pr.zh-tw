---
description: 傳回磁片區的 FVE 中繼資料版本。
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Win32_EncryptableVolume 類別的 GetVersion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972190"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="29d6c-103">Win32 EncryptableVolume 類別的 GetVersion 方法 \_</span><span class="sxs-lookup"><span data-stu-id="29d6c-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="29d6c-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetVersion** 方法會傳回磁片區的 FVE 中繼資料版本。</span><span class="sxs-lookup"><span data-stu-id="29d6c-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="29d6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="29d6c-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="29d6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="29d6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29d6c-107">*版本* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="29d6c-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="29d6c-108">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="29d6c-108">Type: **uint32**</span></span>

<span data-ttu-id="29d6c-109">不帶正負號的整數，表示磁片區的中繼資料版本。</span><span class="sxs-lookup"><span data-stu-id="29d6c-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="29d6c-110">值</span><span class="sxs-lookup"><span data-stu-id="29d6c-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="29d6c-111">意義</span><span class="sxs-lookup"><span data-stu-id="29d6c-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="29d6c-112"><dt>**未知**</dt>的 <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="29d6c-113">作業系統未知。</span><span class="sxs-lookup"><span data-stu-id="29d6c-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="29d6c-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="29d6c-115">Windows Vista 格式，這表示在執行 Windows Vista 的電腦上，磁片區受到 BitLocker 保護。</span><span class="sxs-lookup"><span data-stu-id="29d6c-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="29d6c-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="29d6c-117">Windows 7 格式，表示在執行 Windows 7 的電腦上使用 BitLocker 保護磁片區，或使用 [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) 方法升級元資料格式。</span><span class="sxs-lookup"><span data-stu-id="29d6c-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29d6c-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="29d6c-118">Return value</span></span>

<span data-ttu-id="29d6c-119">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="29d6c-119">Type: **uint32**</span></span>

<span data-ttu-id="29d6c-120">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="29d6c-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="29d6c-121">如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回零。</span><span class="sxs-lookup"><span data-stu-id="29d6c-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="29d6c-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="29d6c-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="29d6c-123">Description</span><span class="sxs-lookup"><span data-stu-id="29d6c-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="29d6c-124"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="29d6c-125">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="29d6c-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="29d6c-126"><dt>**E \_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="29d6c-127">*Version* 參數的值無效。</span><span class="sxs-lookup"><span data-stu-id="29d6c-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="29d6c-128"><dt>**錯誤 \_不正確 \_ DATA**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="29d6c-129">驅動程式傳回了不支援的資料格式。</span><span class="sxs-lookup"><span data-stu-id="29d6c-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="29d6c-130">備註</span><span class="sxs-lookup"><span data-stu-id="29d6c-130">Remarks</span></span>

<span data-ttu-id="29d6c-131">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="29d6c-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="29d6c-132">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="29d6c-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="29d6c-133">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="29d6c-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="29d6c-134">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="29d6c-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29d6c-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="29d6c-135">Requirements</span></span>



| <span data-ttu-id="29d6c-136">需求</span><span class="sxs-lookup"><span data-stu-id="29d6c-136">Requirement</span></span> | <span data-ttu-id="29d6c-137">值</span><span class="sxs-lookup"><span data-stu-id="29d6c-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29d6c-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="29d6c-138">Minimum supported client</span></span><br/> | <span data-ttu-id="29d6c-139">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29d6c-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="29d6c-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="29d6c-140">Minimum supported server</span></span><br/> | <span data-ttu-id="29d6c-141">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="29d6c-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="29d6c-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="29d6c-142">Namespace</span></span><br/>                | <span data-ttu-id="29d6c-143">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="29d6c-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="29d6c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="29d6c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29d6c-145"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="29d6c-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29d6c-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="29d6c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d6c-147">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="29d6c-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

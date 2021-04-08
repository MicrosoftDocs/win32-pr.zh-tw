---
description: 將磁片區從 Windows Vista 格式升級為 Windows 7 格式。
ms.assetid: d6654e92-8176-471b-b8e5-815dd9512240
title: Win32_EncryptableVolume 類別的 UpgradeVolume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UpgradeVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 6769e8a4a480becc5a5584826f60cdb85f8b90e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943326"
---
# <a name="upgradevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1584a-103">Win32 EncryptableVolume 類別的 UpgradeVolume 方法 \_</span><span class="sxs-lookup"><span data-stu-id="1584a-103">UpgradeVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1584a-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UpgradeVolume** 方法會將磁片區從 Windows Vista 格式升級為 windows 7 格式。</span><span class="sxs-lookup"><span data-stu-id="1584a-104">The **UpgradeVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class upgrades a volume from the Windows Vista format to the Windows 7 format.</span></span> <span data-ttu-id="1584a-105">這是不可反轉操作。</span><span class="sxs-lookup"><span data-stu-id="1584a-105">This is a nonreversible operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="1584a-106">語法</span><span class="sxs-lookup"><span data-stu-id="1584a-106">Syntax</span></span>


```mof
uint32 UpgradeVolume();
```



## <a name="parameters"></a><span data-ttu-id="1584a-107">參數</span><span class="sxs-lookup"><span data-stu-id="1584a-107">Parameters</span></span>

<span data-ttu-id="1584a-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="1584a-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1584a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="1584a-109">Return value</span></span>

<span data-ttu-id="1584a-110">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="1584a-110">Type: **uint32**</span></span>

<span data-ttu-id="1584a-111">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="1584a-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="1584a-112">如果磁片區已解除鎖定，而且沒有其他錯誤，則此方法會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1584a-112">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="1584a-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1584a-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="1584a-114">Description</span><span class="sxs-lookup"><span data-stu-id="1584a-114">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1584a-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1584a-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="1584a-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1584a-116">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1584a-117"><dt>**E \_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="1584a-117"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl>            | <span data-ttu-id="1584a-118">一或多個引數無效。</span><span class="sxs-lookup"><span data-stu-id="1584a-118">One or more of the arguments are not valid.</span></span><br/>                                       |
| <dl> <span data-ttu-id="1584a-119"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="1584a-119"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="1584a-120">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="1584a-120">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="1584a-121"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="1584a-121"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="1584a-122">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1584a-122">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="1584a-123">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="1584a-123">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="1584a-124">備註</span><span class="sxs-lookup"><span data-stu-id="1584a-124">Remarks</span></span>

<span data-ttu-id="1584a-125">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="1584a-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1584a-126">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1584a-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1584a-127">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="1584a-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1584a-128">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="1584a-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1584a-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="1584a-129">Requirements</span></span>



| <span data-ttu-id="1584a-130">需求</span><span class="sxs-lookup"><span data-stu-id="1584a-130">Requirement</span></span> | <span data-ttu-id="1584a-131">值</span><span class="sxs-lookup"><span data-stu-id="1584a-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1584a-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1584a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="1584a-133">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1584a-133">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1584a-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1584a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="1584a-135">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1584a-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1584a-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="1584a-136">Namespace</span></span><br/>                | <span data-ttu-id="1584a-137">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1584a-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1584a-138">MOF</span><span class="sxs-lookup"><span data-stu-id="1584a-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1584a-139"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="1584a-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1584a-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1584a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1584a-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="1584a-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

---
description: 將修復資料備份至 Active Directory。
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Win32_EncryptableVolume 類別的 BackupRecoveryInformationToActiveDirectory 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971645"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="819ae-103">Win32 EncryptableVolume 類別的 BackupRecoveryInformationToActiveDirectory 方法 \_</span><span class="sxs-lookup"><span data-stu-id="819ae-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="819ae-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **BackupRecoveryInformationToActiveDirectory** 方法會將修復資料備份至 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="819ae-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="819ae-105">此方法要求磁片區上必須有數值密碼保護裝置。</span><span class="sxs-lookup"><span data-stu-id="819ae-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="819ae-106">您也必須將群組原則設定為可讓您將修復資訊備份到 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="819ae-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="819ae-107">語法</span><span class="sxs-lookup"><span data-stu-id="819ae-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="819ae-108">參數</span><span class="sxs-lookup"><span data-stu-id="819ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="819ae-109">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="819ae-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="819ae-110">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="819ae-110">Type: **string**</span></span>

<span data-ttu-id="819ae-111">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="819ae-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="819ae-112">此金鑰保護裝置必須是數位密碼保護裝置。</span><span class="sxs-lookup"><span data-stu-id="819ae-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="819ae-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="819ae-113">Return value</span></span>

<span data-ttu-id="819ae-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="819ae-114">Type: **uint32**</span></span>

<span data-ttu-id="819ae-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="819ae-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="819ae-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="819ae-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="819ae-117">Description</span><span class="sxs-lookup"><span data-stu-id="819ae-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="819ae-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="819ae-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="819ae-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="819ae-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="819ae-120"><dt>**S \_FALSE**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="819ae-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="819ae-121">群組原則不允許將修復資訊儲存到 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="819ae-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="819ae-122"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="819ae-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="819ae-123">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="819ae-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="819ae-124">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="819ae-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="819ae-125"><dt>**FVE \_E \_ 不正確 \_ 保護裝置 \_ 類型**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="819ae-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="819ae-126">指定的金鑰保護裝置不是數位金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="819ae-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="819ae-127">您必須輸入數位密碼保護裝置。</span><span class="sxs-lookup"><span data-stu-id="819ae-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="819ae-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="819ae-128">Requirements</span></span>



| <span data-ttu-id="819ae-129">需求</span><span class="sxs-lookup"><span data-stu-id="819ae-129">Requirement</span></span> | <span data-ttu-id="819ae-130">值</span><span class="sxs-lookup"><span data-stu-id="819ae-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="819ae-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="819ae-131">Minimum supported client</span></span><br/> | <span data-ttu-id="819ae-132">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819ae-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="819ae-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="819ae-133">Minimum supported server</span></span><br/> | <span data-ttu-id="819ae-134">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="819ae-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="819ae-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="819ae-135">Namespace</span></span><br/>                | <span data-ttu-id="819ae-136">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="819ae-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="819ae-137">MOF</span><span class="sxs-lookup"><span data-stu-id="819ae-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="819ae-138"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="819ae-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="819ae-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="819ae-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819ae-140">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="819ae-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





---
description: 抓取 BitLocker 已暫止的次數。
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: 'Win32_EncryptableVolume 類別的 GetSuspendCount 方法 (Activdbg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983813"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="17e71-103">Win32 EncryptableVolume 類別的 GetSuspendCount 方法 \_</span><span class="sxs-lookup"><span data-stu-id="17e71-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="17e71-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetSuspendCount** 方法會先抓取重新開機次數，然後才會自動繼續執行保護。</span><span class="sxs-lookup"><span data-stu-id="17e71-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="17e71-105">語法</span><span class="sxs-lookup"><span data-stu-id="17e71-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="17e71-106">參數</span><span class="sxs-lookup"><span data-stu-id="17e71-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17e71-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="17e71-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="17e71-108">從0到15的整數值。</span><span class="sxs-lookup"><span data-stu-id="17e71-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17e71-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="17e71-109">Return value</span></span>

<span data-ttu-id="17e71-110">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="17e71-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="17e71-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="17e71-111">Return code</span></span>                                                                                          | <span data-ttu-id="17e71-112">Description</span><span class="sxs-lookup"><span data-stu-id="17e71-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17e71-113"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="17e71-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="17e71-114">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="17e71-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="17e71-115"><dt>**\_不 \_ 支援的錯誤**</dt></span><span class="sxs-lookup"><span data-stu-id="17e71-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="17e71-116">如果磁片區未暫停或不是 OS 磁片區，則傳回。</span><span class="sxs-lookup"><span data-stu-id="17e71-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="17e71-117">備註</span><span class="sxs-lookup"><span data-stu-id="17e71-117">Remarks</span></span>

<span data-ttu-id="17e71-118">此方法僅適用于 OS 磁片區，而且只有在該磁片區實際暫停時才會套用。</span><span class="sxs-lookup"><span data-stu-id="17e71-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="17e71-119">如果磁片區未暫停或不是 OS 磁片區，則會傳回 **\_ 不 \_ 支援的錯誤** 。</span><span class="sxs-lookup"><span data-stu-id="17e71-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="17e71-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="17e71-120">Requirements</span></span>



| <span data-ttu-id="17e71-121">需求</span><span class="sxs-lookup"><span data-stu-id="17e71-121">Requirement</span></span> | <span data-ttu-id="17e71-122">值</span><span class="sxs-lookup"><span data-stu-id="17e71-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17e71-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17e71-123">Minimum supported client</span></span><br/> | <span data-ttu-id="17e71-124">Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17e71-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="17e71-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17e71-125">Minimum supported server</span></span><br/> | <span data-ttu-id="17e71-126">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17e71-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="17e71-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="17e71-127">Namespace</span></span><br/>                | <span data-ttu-id="17e71-128">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="17e71-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="17e71-129">標頭</span><span class="sxs-lookup"><span data-stu-id="17e71-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="17e71-130"><dt>Activdbg。h</dt></span><span class="sxs-lookup"><span data-stu-id="17e71-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="17e71-131">MOF</span><span class="sxs-lookup"><span data-stu-id="17e71-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17e71-132"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="17e71-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17e71-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17e71-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17e71-134">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="17e71-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





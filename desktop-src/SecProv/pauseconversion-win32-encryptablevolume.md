---
description: 暫停磁片區的加密或解密。
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Win32_EncryptableVolume 類別的 PauseConversion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975374"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="dedd4-103">Win32 EncryptableVolume 類別的 PauseConversion 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dedd4-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="dedd4-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **PauseConversion** 方法會暫停磁片區的加密或解密。</span><span class="sxs-lookup"><span data-stu-id="dedd4-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="dedd4-105">如果光碟支援硬體加密，此函式可以暫停抹除操作，但無法暫停以硬體為基礎的加密。</span><span class="sxs-lookup"><span data-stu-id="dedd4-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dedd4-106">語法</span><span class="sxs-lookup"><span data-stu-id="dedd4-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="dedd4-107">參數</span><span class="sxs-lookup"><span data-stu-id="dedd4-107">Parameters</span></span>

<span data-ttu-id="dedd4-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dedd4-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dedd4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="dedd4-109">Return value</span></span>

<span data-ttu-id="dedd4-110">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="dedd4-110">Type: **uint32**</span></span>

<span data-ttu-id="dedd4-111">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="dedd4-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="dedd4-112">如果此方法用於完整加密或完整解密的磁片區，或磁片區上已暫停加密/解密，則會傳回0，假設沒有其他錯誤發生。</span><span class="sxs-lookup"><span data-stu-id="dedd4-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="dedd4-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="dedd4-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="dedd4-114">Description</span><span class="sxs-lookup"><span data-stu-id="dedd4-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="dedd4-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dedd4-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="dedd4-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="dedd4-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="dedd4-117"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="dedd4-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="dedd4-118">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="dedd4-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="dedd4-119">備註</span><span class="sxs-lookup"><span data-stu-id="dedd4-119">Remarks</span></span>

<span data-ttu-id="dedd4-120">如果在進行加密/解密的磁片區上使用此方法，成功執行此方法會導致 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 指出加密或解密已暫停。</span><span class="sxs-lookup"><span data-stu-id="dedd4-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="dedd4-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="dedd4-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dedd4-122">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dedd4-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dedd4-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="dedd4-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dedd4-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="dedd4-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dedd4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dedd4-125">Requirements</span></span>



| <span data-ttu-id="dedd4-126">需求</span><span class="sxs-lookup"><span data-stu-id="dedd4-126">Requirement</span></span> | <span data-ttu-id="dedd4-127">值</span><span class="sxs-lookup"><span data-stu-id="dedd4-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dedd4-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dedd4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dedd4-129">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dedd4-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dedd4-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dedd4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dedd4-131">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dedd4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dedd4-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="dedd4-132">Namespace</span></span><br/>                | <span data-ttu-id="dedd4-133">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="dedd4-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="dedd4-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dedd4-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dedd4-135"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="dedd4-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dedd4-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dedd4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dedd4-137">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="dedd4-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

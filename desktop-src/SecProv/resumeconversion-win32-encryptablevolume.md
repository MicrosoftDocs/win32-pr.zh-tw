---
description: 繼續加密或解密磁片區。
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Win32_EncryptableVolume 類別的 ResumeConversion 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690095"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="74dfd-103">Win32 EncryptableVolume 類別的 ResumeConversion 方法 \_</span><span class="sxs-lookup"><span data-stu-id="74dfd-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="74dfd-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **ResumeConversion** 方法會繼續加密或解密磁片區。</span><span class="sxs-lookup"><span data-stu-id="74dfd-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="74dfd-105">如果光碟支援硬體加密，此函式只能繼續抹除作業。</span><span class="sxs-lookup"><span data-stu-id="74dfd-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="74dfd-106">如需詳細資訊，請參閱 [**PauseConversion**](pauseconversion-win32-encryptablevolume.md)。</span><span class="sxs-lookup"><span data-stu-id="74dfd-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="74dfd-107">語法</span><span class="sxs-lookup"><span data-stu-id="74dfd-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="74dfd-108">參數</span><span class="sxs-lookup"><span data-stu-id="74dfd-108">Parameters</span></span>

<span data-ttu-id="74dfd-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="74dfd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="74dfd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="74dfd-110">Return value</span></span>

<span data-ttu-id="74dfd-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="74dfd-111">Type: **uint32**</span></span>

<span data-ttu-id="74dfd-112">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="74dfd-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="74dfd-113">如果在完整加密或完整解密的磁片區上使用此方法，或磁片區上已進行加密/解密，則會傳回0，假設沒有其他錯誤發生。</span><span class="sxs-lookup"><span data-stu-id="74dfd-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="74dfd-114">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="74dfd-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="74dfd-115">Description</span><span class="sxs-lookup"><span data-stu-id="74dfd-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="74dfd-116"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="74dfd-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="74dfd-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="74dfd-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="74dfd-118"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="74dfd-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="74dfd-119">磁片區已鎖定。</span><span class="sxs-lookup"><span data-stu-id="74dfd-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="74dfd-120">備註</span><span class="sxs-lookup"><span data-stu-id="74dfd-120">Remarks</span></span>

<span data-ttu-id="74dfd-121">如果在具有暫停加密/解密的磁片區上使用此方法，則成功執行此方法會導致 [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) 指出正在進行加密或解密。</span><span class="sxs-lookup"><span data-stu-id="74dfd-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="74dfd-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="74dfd-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="74dfd-123">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="74dfd-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="74dfd-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="74dfd-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="74dfd-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="74dfd-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74dfd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="74dfd-126">Requirements</span></span>



| <span data-ttu-id="74dfd-127">需求</span><span class="sxs-lookup"><span data-stu-id="74dfd-127">Requirement</span></span> | <span data-ttu-id="74dfd-128">值</span><span class="sxs-lookup"><span data-stu-id="74dfd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74dfd-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74dfd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74dfd-130">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74dfd-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="74dfd-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74dfd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74dfd-132">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74dfd-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74dfd-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="74dfd-133">Namespace</span></span><br/>                | <span data-ttu-id="74dfd-134">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="74dfd-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="74dfd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="74dfd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74dfd-136"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="74dfd-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74dfd-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74dfd-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74dfd-138">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="74dfd-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

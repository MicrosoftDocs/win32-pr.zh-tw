---
description: 判斷磁片區是否位於支援或可支援硬體加密的磁片磁碟機上。
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Win32_EncryptableVolume 類別的 GetHardwareEncryptionStatus 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973438"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="bd222-103">Win32 EncryptableVolume 類別的 GetHardwareEncryptionStatus 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bd222-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="bd222-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetHardwareEncryptionStatus** 方法會判斷磁片區是否位於支援或可支援硬體加密的磁片磁碟機上。</span><span class="sxs-lookup"><span data-stu-id="bd222-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd222-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd222-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="bd222-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd222-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd222-107">*HardwareEncryptionStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bd222-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd222-108">指定磁片磁碟機是否可以支援硬體加密。</span><span class="sxs-lookup"><span data-stu-id="bd222-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="bd222-109">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bd222-109">This can be one of the following values.</span></span>



| <span data-ttu-id="bd222-110">值</span><span class="sxs-lookup"><span data-stu-id="bd222-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="bd222-111">意義</span><span class="sxs-lookup"><span data-stu-id="bd222-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="bd222-112"><dt>**不支援**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="bd222-113">不支援硬體加密。</span><span class="sxs-lookup"><span data-stu-id="bd222-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="bd222-114"><dt>**無保護措施**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="bd222-115">不支援磁片磁碟機加密。</span><span class="sxs-lookup"><span data-stu-id="bd222-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="bd222-116"><dt>**使用軟體**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="bd222-117">加密方法是以軟體為基礎。</span><span class="sxs-lookup"><span data-stu-id="bd222-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="bd222-118"><dt>**使用硬體**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="bd222-119">磁片磁碟機支援硬體加密。</span><span class="sxs-lookup"><span data-stu-id="bd222-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd222-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd222-120">Return value</span></span>

<span data-ttu-id="bd222-121">如果磁片區與 BitLocker 硬體加密相容，則此函式會傳回零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="bd222-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="bd222-122">否則，函數會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="bd222-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="bd222-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="bd222-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="bd222-124">Description</span><span class="sxs-lookup"><span data-stu-id="bd222-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bd222-125"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bd222-126">磁片區與 BitLocker 硬體加密相容。</span><span class="sxs-lookup"><span data-stu-id="bd222-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd222-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd222-127">Requirements</span></span>



| <span data-ttu-id="bd222-128">需求</span><span class="sxs-lookup"><span data-stu-id="bd222-128">Requirement</span></span> | <span data-ttu-id="bd222-129">值</span><span class="sxs-lookup"><span data-stu-id="bd222-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd222-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd222-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bd222-131">Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd222-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd222-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd222-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bd222-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd222-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd222-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd222-134">Namespace</span></span><br/>                | <span data-ttu-id="bd222-135">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="bd222-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="bd222-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bd222-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd222-137"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd222-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd222-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd222-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd222-139">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="bd222-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





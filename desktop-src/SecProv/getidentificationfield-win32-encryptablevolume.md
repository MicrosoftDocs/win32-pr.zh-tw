---
description: 傳回磁片區的中繼資料中可用的識別碼字串。
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Win32_EncryptableVolume 類別的 GetIdentificationField 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112637"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f70e2-103">Win32 EncryptableVolume 類別的 GetIdentificationField 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f70e2-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f70e2-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetIdentificationField** 方法會傳回磁片區中繼資料中可用的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="f70e2-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="f70e2-105">語法</span><span class="sxs-lookup"><span data-stu-id="f70e2-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="f70e2-106">參數</span><span class="sxs-lookup"><span data-stu-id="f70e2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f70e2-107">*IdentificationField* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f70e2-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f70e2-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f70e2-108">Type: **string**</span></span>

<span data-ttu-id="f70e2-109">字串，指定指派給磁片區的識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="f70e2-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f70e2-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f70e2-110">Return value</span></span>

<span data-ttu-id="f70e2-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f70e2-111">Type: **uint32**</span></span>

<span data-ttu-id="f70e2-112">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f70e2-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f70e2-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f70e2-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f70e2-114">Description</span><span class="sxs-lookup"><span data-stu-id="f70e2-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f70e2-115"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f70e2-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f70e2-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f70e2-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="f70e2-117"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f70e2-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f70e2-118">此磁片磁碟機已由 BitLocker 磁碟機加密鎖定。</span><span class="sxs-lookup"><span data-stu-id="f70e2-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="f70e2-119">您必須將此磁片區從主控台解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="f70e2-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="f70e2-120"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f70e2-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="f70e2-121">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="f70e2-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f70e2-122">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="f70e2-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="f70e2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f70e2-123">Requirements</span></span>



| <span data-ttu-id="f70e2-124">需求</span><span class="sxs-lookup"><span data-stu-id="f70e2-124">Requirement</span></span> | <span data-ttu-id="f70e2-125">值</span><span class="sxs-lookup"><span data-stu-id="f70e2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f70e2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f70e2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f70e2-127">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f70e2-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f70e2-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f70e2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f70e2-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f70e2-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f70e2-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="f70e2-130">Namespace</span></span><br/>                | <span data-ttu-id="f70e2-131">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f70e2-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f70e2-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f70e2-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f70e2-133"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="f70e2-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f70e2-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f70e2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f70e2-135">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f70e2-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





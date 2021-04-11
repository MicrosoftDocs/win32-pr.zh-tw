---
description: 在磁片區的中繼資料中設定指定的識別碼字串。
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Win32_EncryptableVolume 類別的 SetIdentificationField 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852075"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b9f57-103">Win32 EncryptableVolume 類別的 SetIdentificationField 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b9f57-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b9f57-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **SetIdentificationField** 方法會在磁片區的中繼資料中設定指定的識別碼字串。</span><span class="sxs-lookup"><span data-stu-id="b9f57-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9f57-105">語法</span><span class="sxs-lookup"><span data-stu-id="b9f57-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="b9f57-106">參數</span><span class="sxs-lookup"><span data-stu-id="b9f57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9f57-107">*IdentificationField* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="b9f57-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b9f57-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="b9f57-108">Type: **string**</span></span>

<span data-ttu-id="b9f57-109">字串，指定指派給磁片區的識別碼欄位。</span><span class="sxs-lookup"><span data-stu-id="b9f57-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="b9f57-110">如果選擇性字串不存在，則會使用登錄集值。</span><span class="sxs-lookup"><span data-stu-id="b9f57-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="b9f57-111">如果字串存在且不是空的，則會使用指定的值。</span><span class="sxs-lookup"><span data-stu-id="b9f57-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="b9f57-112">*IdentificationField* 參數不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b9f57-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9f57-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="b9f57-113">Return value</span></span>

<span data-ttu-id="b9f57-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="b9f57-114">Type: **uint32**</span></span>

<span data-ttu-id="b9f57-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b9f57-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b9f57-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b9f57-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="b9f57-117">Description</span><span class="sxs-lookup"><span data-stu-id="b9f57-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9f57-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b9f57-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="b9f57-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="b9f57-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="b9f57-120"><dt>**FVE \_E \_ 鎖定的 \_ 磁片**</dt>區 <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="b9f57-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="b9f57-121">此磁片磁碟機已由 BitLocker 磁碟機加密鎖定。</span><span class="sxs-lookup"><span data-stu-id="b9f57-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="b9f57-122">您必須將此磁片區從主控台解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="b9f57-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="b9f57-123"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="b9f57-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="b9f57-124">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b9f57-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="b9f57-125">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="b9f57-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="b9f57-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="b9f57-126">Requirements</span></span>



| <span data-ttu-id="b9f57-127">需求</span><span class="sxs-lookup"><span data-stu-id="b9f57-127">Requirement</span></span> | <span data-ttu-id="b9f57-128">值</span><span class="sxs-lookup"><span data-stu-id="b9f57-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9f57-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b9f57-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9f57-130">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9f57-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b9f57-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b9f57-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9f57-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b9f57-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b9f57-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="b9f57-133">Namespace</span></span><br/>                | <span data-ttu-id="b9f57-134">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b9f57-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b9f57-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b9f57-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9f57-136"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9f57-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9f57-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b9f57-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9f57-138">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="b9f57-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 





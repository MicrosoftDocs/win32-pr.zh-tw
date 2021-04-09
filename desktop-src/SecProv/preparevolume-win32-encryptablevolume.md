---
description: 使用探索磁片區的指定檔案系統類型建立 BitLocker 磁片區。
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Win32_EncryptableVolume 類別的 PrepareVolume 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112633"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4efcf-103">Win32 EncryptableVolume 類別的 PrepareVolume 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4efcf-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4efcf-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **PrepareVolume** 方法會使用探索磁片區的指定檔案系統類型來建立 BitLocker 磁片區。</span><span class="sxs-lookup"><span data-stu-id="4efcf-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="4efcf-105">必須先呼叫這個方法，才能使用任何 \**ProtectKeyWith \** _ 方法來保護磁片區。</span><span class="sxs-lookup"><span data-stu-id="4efcf-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="4efcf-106">語法</span><span class="sxs-lookup"><span data-stu-id="4efcf-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="4efcf-107">參數</span><span class="sxs-lookup"><span data-stu-id="4efcf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4efcf-108">_DiscoveryVolumeType \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4efcf-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efcf-109">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="4efcf-109">Type: **string**</span></span>

<span data-ttu-id="4efcf-110">指定探索磁片區類型的字串。</span><span class="sxs-lookup"><span data-stu-id="4efcf-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="4efcf-111">值</span><span class="sxs-lookup"><span data-stu-id="4efcf-111">Value</span></span>               | <span data-ttu-id="4efcf-112">意義</span><span class="sxs-lookup"><span data-stu-id="4efcf-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="4efcf-113">**&lt;沒有&gt;**</span><span class="sxs-lookup"><span data-stu-id="4efcf-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="4efcf-114">無探索磁片區。</span><span class="sxs-lookup"><span data-stu-id="4efcf-114">No discovery volume.</span></span> <span data-ttu-id="4efcf-115">此值會建立原生 BitLocker 磁片區。</span><span class="sxs-lookup"><span data-stu-id="4efcf-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="4efcf-116">**&lt;預設&gt;**</span><span class="sxs-lookup"><span data-stu-id="4efcf-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="4efcf-117">此值為預設行為。</span><span class="sxs-lookup"><span data-stu-id="4efcf-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="4efcf-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="4efcf-118">**FAT32**</span></span>           | <span data-ttu-id="4efcf-119">此值會建立 FAT32 探索磁片區。</span><span class="sxs-lookup"><span data-stu-id="4efcf-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="4efcf-120">*ForceEncryptionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4efcf-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4efcf-121">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4efcf-121">Type: **uint32**</span></span>

<span data-ttu-id="4efcf-122">指定加密類型的整數。</span><span class="sxs-lookup"><span data-stu-id="4efcf-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="4efcf-123">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4efcf-123">This can be one of the following values.</span></span>

| <span data-ttu-id="4efcf-124">值</span><span class="sxs-lookup"><span data-stu-id="4efcf-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="4efcf-125">意義</span><span class="sxs-lookup"><span data-stu-id="4efcf-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="4efcf-126"><dt>**未指定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4efcf-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="4efcf-127">未指定加密類型。</span><span class="sxs-lookup"><span data-stu-id="4efcf-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="4efcf-128"><dt>**軟體**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4efcf-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="4efcf-129">軟體加密。</span><span class="sxs-lookup"><span data-stu-id="4efcf-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="4efcf-130"><dt>**硬體**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4efcf-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="4efcf-131">硬體加密。</span><span class="sxs-lookup"><span data-stu-id="4efcf-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4efcf-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="4efcf-132">Return value</span></span>

<span data-ttu-id="4efcf-133">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="4efcf-133">Type: **uint32**</span></span>

<span data-ttu-id="4efcf-134">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4efcf-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="4efcf-135">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="4efcf-135">Return code/value</span></span>      | <span data-ttu-id="4efcf-136">Description</span><span class="sxs-lookup"><span data-stu-id="4efcf-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="4efcf-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="4efcf-137">**S_OK**</span></span> <br/> <span data-ttu-id="4efcf-138">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="4efcf-138">0 (0x0)</span></span> | <span data-ttu-id="4efcf-139">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="4efcf-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="4efcf-140">備註</span><span class="sxs-lookup"><span data-stu-id="4efcf-140">Remarks</span></span>

<span data-ttu-id="4efcf-141">如果您在啟用 BitLocker 磁片區時未呼叫這個方法，就如同在 *DiscoveryVolumeType* 參數中使用預設值呼叫此方法一樣。</span><span class="sxs-lookup"><span data-stu-id="4efcf-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4efcf-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="4efcf-142">Requirements</span></span>

| <span data-ttu-id="4efcf-143">需求</span><span class="sxs-lookup"><span data-stu-id="4efcf-143">Requirement</span></span> | <span data-ttu-id="4efcf-144">值</span><span class="sxs-lookup"><span data-stu-id="4efcf-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4efcf-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4efcf-145">Minimum supported client</span></span><br/> | <span data-ttu-id="4efcf-146">Windows 7 企業版，僅限 Windows 7 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4efcf-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4efcf-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4efcf-147">Minimum supported server</span></span><br/> | <span data-ttu-id="4efcf-148">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4efcf-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4efcf-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="4efcf-149">Namespace</span></span><br/>                | <span data-ttu-id="4efcf-150">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="4efcf-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4efcf-151">MOF</span><span class="sxs-lookup"><span data-stu-id="4efcf-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4efcf-152"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="4efcf-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="4efcf-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4efcf-153">See also</span></span>

[<span data-ttu-id="4efcf-154">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="4efcf-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)

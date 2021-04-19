---
description: 從檔案傳回外部金鑰。
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Win32_EncryptableVolume 類別的 GetExternalKeyFromFile 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988354"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f23e9-103">Win32 EncryptableVolume 類別的 GetExternalKeyFromFile 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f23e9-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f23e9-104">如果指定檔案的位置， [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetExternalKeyFromFile** 方法會從 [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md)所建立的檔案傳回外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="f23e9-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="f23e9-105">語法</span><span class="sxs-lookup"><span data-stu-id="f23e9-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="f23e9-106">參數</span><span class="sxs-lookup"><span data-stu-id="f23e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f23e9-107">*PathWithFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f23e9-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f23e9-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f23e9-108">Type: **string**</span></span>

<span data-ttu-id="f23e9-109">字串，指定包含外部索引鍵之檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="f23e9-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="f23e9-110">*ExternalKey* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f23e9-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f23e9-111">類型： **uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f23e9-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f23e9-112">位元組陣列，這是包含在可用來解除鎖定磁片區之檔案中的256位外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="f23e9-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f23e9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f23e9-113">Return value</span></span>

<span data-ttu-id="f23e9-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f23e9-114">Type: **uint32**</span></span>

<span data-ttu-id="f23e9-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f23e9-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f23e9-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f23e9-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="f23e9-117">Description</span><span class="sxs-lookup"><span data-stu-id="f23e9-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="f23e9-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f23e9-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="f23e9-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f23e9-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="f23e9-120"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f23e9-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="f23e9-121">檔案不包含外部金鑰。</span><span class="sxs-lookup"><span data-stu-id="f23e9-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="f23e9-122"><dt>**錯誤 \_\_找不 \_ 到**</dt>檔案 <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="f23e9-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="f23e9-123">在指定的位置找不到檔案。</span><span class="sxs-lookup"><span data-stu-id="f23e9-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f23e9-124">備註</span><span class="sxs-lookup"><span data-stu-id="f23e9-124">Remarks</span></span>

<span data-ttu-id="f23e9-125">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f23e9-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f23e9-126">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f23e9-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f23e9-127">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f23e9-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f23e9-128">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="f23e9-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f23e9-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="f23e9-129">Requirements</span></span>



| <span data-ttu-id="f23e9-130">需求</span><span class="sxs-lookup"><span data-stu-id="f23e9-130">Requirement</span></span> | <span data-ttu-id="f23e9-131">值</span><span class="sxs-lookup"><span data-stu-id="f23e9-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f23e9-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f23e9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f23e9-133">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f23e9-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f23e9-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f23e9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f23e9-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f23e9-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f23e9-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="f23e9-136">Namespace</span></span><br/>                | <span data-ttu-id="f23e9-137">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f23e9-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f23e9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="f23e9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f23e9-139"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="f23e9-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f23e9-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f23e9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f23e9-141">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f23e9-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

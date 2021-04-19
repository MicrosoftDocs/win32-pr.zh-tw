---
description: 使用提供的 Active Directory 安全識別碼 (SID) 字串來取得衍生金鑰，並解除鎖定加密的磁片區。
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Win32_EncryptableVolume 類別的 UnlockWithAdSid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975893"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ec5ea-103">Win32 EncryptableVolume 類別的 UnlockWithAdSid 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ec5ea-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ec5ea-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **UnlockWithAdSid** 方法會使用提供的 Active Directory 安全識別碼 (SID) 字串來取得衍生金鑰，並解除鎖定加密的磁片區。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="ec5ea-105">如果光碟支援硬體加密，此函式會將頻外狀態設為「已解除鎖定」。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ec5ea-106">語法</span><span class="sxs-lookup"><span data-stu-id="ec5ea-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="ec5ea-107">參數</span><span class="sxs-lookup"><span data-stu-id="ec5ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec5ea-108">*SidString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec5ea-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec5ea-109">包含 Active Directory SID 的字串。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec5ea-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec5ea-110">Return value</span></span>

<span data-ttu-id="ec5ea-111">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ec5ea-112">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ec5ea-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ec5ea-113">Description</span><span class="sxs-lookup"><span data-stu-id="ec5ea-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ec5ea-114"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ec5ea-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ec5ea-115">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ec5ea-116">備註</span><span class="sxs-lookup"><span data-stu-id="ec5ea-116">Remarks</span></span>

<span data-ttu-id="ec5ea-117">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ec5ea-118">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ec5ea-119">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ec5ea-120">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="ec5ea-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec5ea-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec5ea-121">Requirements</span></span>



| <span data-ttu-id="ec5ea-122">需求</span><span class="sxs-lookup"><span data-stu-id="ec5ea-122">Requirement</span></span> | <span data-ttu-id="ec5ea-123">值</span><span class="sxs-lookup"><span data-stu-id="ec5ea-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec5ea-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec5ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec5ea-125">Windows 8 企業版，僅 Windows 8 Pro \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5ea-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ec5ea-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec5ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec5ea-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec5ea-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec5ea-128">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec5ea-128">Namespace</span></span><br/>                | <span data-ttu-id="ec5ea-129">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ec5ea-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ec5ea-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ec5ea-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec5ea-131"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec5ea-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec5ea-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec5ea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec5ea-133">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="ec5ea-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

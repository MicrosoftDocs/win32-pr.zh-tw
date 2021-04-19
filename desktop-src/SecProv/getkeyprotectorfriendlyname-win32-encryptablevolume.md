---
description: 抓取用來識別指定金鑰保護裝置的顯示名稱。
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Win32_EncryptableVolume 類別的 GetKeyProtectorFriendlyName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997872"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f2741-103">Win32 EncryptableVolume 類別的 GetKeyProtectorFriendlyName 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f2741-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f2741-104">[**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md)類別的 **GetKeyProtectorFriendlyName** 方法會抓取用來識別指定金鑰保護裝置的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f2741-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2741-105">語法</span><span class="sxs-lookup"><span data-stu-id="f2741-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="f2741-106">參數</span><span class="sxs-lookup"><span data-stu-id="f2741-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2741-107">*VolumeKeyProtectorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f2741-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2741-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2741-108">Type: **string**</span></span>

<span data-ttu-id="f2741-109">用來管理加密磁片區金鑰保護裝置的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2741-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="f2741-110">*FriendlyName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f2741-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2741-111">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="f2741-111">Type: **string**</span></span>

<span data-ttu-id="f2741-112">字串，其中包含使用者指定的名稱，用來識別指定的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="f2741-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2741-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f2741-113">Return value</span></span>

<span data-ttu-id="f2741-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="f2741-114">Type: **uint32**</span></span>

<span data-ttu-id="f2741-115">這個方法會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f2741-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f2741-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f2741-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f2741-117">Description</span><span class="sxs-lookup"><span data-stu-id="f2741-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f2741-118"><dt>**S \_確定**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f2741-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f2741-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f2741-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f2741-120"><dt>**E \_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f2741-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="f2741-121">*VolumeKeyProtectorID* 參數未參考有效的金鑰保護裝置。</span><span class="sxs-lookup"><span data-stu-id="f2741-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="f2741-122"><dt>**FVE \_E \_ 未 \_ 啟用**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f2741-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="f2741-123">磁碟區上未啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="f2741-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f2741-124">新增金鑰保護裝置以啟用 BitLocker。</span><span class="sxs-lookup"><span data-stu-id="f2741-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2741-125">備註</span><span class="sxs-lookup"><span data-stu-id="f2741-125">Remarks</span></span>

<span data-ttu-id="f2741-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="f2741-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f2741-127">MOF 檔案不會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f2741-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f2741-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="f2741-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f2741-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](../wmisdk/managed-object-format--mof-.md)。</span><span class="sxs-lookup"><span data-stu-id="f2741-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2741-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2741-130">Requirements</span></span>



| <span data-ttu-id="f2741-131">需求</span><span class="sxs-lookup"><span data-stu-id="f2741-131">Requirement</span></span> | <span data-ttu-id="f2741-132">值</span><span class="sxs-lookup"><span data-stu-id="f2741-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2741-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f2741-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f2741-134">僅限 windows Vista Enterprise、Windows Vista 旗艦版傳統型 \[ 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2741-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f2741-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f2741-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f2741-136">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f2741-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2741-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="f2741-137">Namespace</span></span><br/>                | <span data-ttu-id="f2741-138">根 \\ CIMV2 \\ 安全性 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f2741-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f2741-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f2741-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2741-140"><dt>Win32 \_ encryptablevolume mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2741-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2741-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f2741-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2741-142">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="f2741-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 

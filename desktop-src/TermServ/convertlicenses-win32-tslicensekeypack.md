---
title: Win32_TSLicenseKeyPack 類別的 ConvertLicenses 方法
description: 轉換目前金鑰套件中的授權。
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- ConvertLicenses 方法遠端桌面服務
- ConvertLicenses 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ConvertLicenses 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384081"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="11694-106">Win32 TSLicenseKeyPack 類別的 ConvertLicenses 方法 \_</span><span class="sxs-lookup"><span data-stu-id="11694-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="11694-107">轉換目前金鑰套件中的授權。</span><span class="sxs-lookup"><span data-stu-id="11694-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="11694-108">如果授權是每個使用者的授權，則會轉換成每個裝置的授權。</span><span class="sxs-lookup"><span data-stu-id="11694-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="11694-109">如果授權是個別裝置授權，則會轉換為每個使用者的授權。</span><span class="sxs-lookup"><span data-stu-id="11694-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="11694-110">語法</span><span class="sxs-lookup"><span data-stu-id="11694-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="11694-111">參數</span><span class="sxs-lookup"><span data-stu-id="11694-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11694-112">*計數* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11694-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11694-113">要轉換的授權數目。</span><span class="sxs-lookup"><span data-stu-id="11694-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="11694-114">*KeypackID* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11694-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11694-115">結果金鑰套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="11694-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11694-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="11694-116">Return value</span></span>

<span data-ttu-id="11694-117">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="11694-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="11694-118">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="11694-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="11694-119">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="11694-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11694-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="11694-120">Requirements</span></span>



| <span data-ttu-id="11694-121">需求</span><span class="sxs-lookup"><span data-stu-id="11694-121">Requirement</span></span> | <span data-ttu-id="11694-122">值</span><span class="sxs-lookup"><span data-stu-id="11694-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="11694-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11694-123">Minimum supported client</span></span><br/> | <span data-ttu-id="11694-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="11694-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="11694-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11694-125">Minimum supported server</span></span><br/> | <span data-ttu-id="11694-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11694-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="11694-127">命名空間</span><span class="sxs-lookup"><span data-stu-id="11694-127">Namespace</span></span><br/>                | <span data-ttu-id="11694-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="11694-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="11694-129">MOF</span><span class="sxs-lookup"><span data-stu-id="11694-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11694-130"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="11694-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11694-131">DLL</span><span class="sxs-lookup"><span data-stu-id="11694-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11694-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11694-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11694-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11694-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11694-134">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="11694-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






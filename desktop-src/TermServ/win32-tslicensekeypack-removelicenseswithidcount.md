---
title: Win32_TSLicenseKeyPack 類別的 RemoveLicensesWithIdCount 方法
description: 從指定的金鑰套件中移除指定的遠端桌面服務授權數目。
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- RemoveLicensesWithIdCount 方法遠端桌面服務
- RemoveLicensesWithIdCount 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，RemoveLicensesWithIdCount 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024686"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="af12b-106">Win32 TSLicenseKeyPack 類別的 RemoveLicensesWithIdCount 方法 \_</span><span class="sxs-lookup"><span data-stu-id="af12b-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="af12b-107">從指定的金鑰套件中移除指定的遠端桌面服務授權數目。</span><span class="sxs-lookup"><span data-stu-id="af12b-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="af12b-108">語法</span><span class="sxs-lookup"><span data-stu-id="af12b-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="af12b-109">參數</span><span class="sxs-lookup"><span data-stu-id="af12b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af12b-110">*KeyPackId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af12b-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af12b-111">包含要移除之授權的金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="af12b-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="af12b-112">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="af12b-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af12b-113">要卸載的授權數目。</span><span class="sxs-lookup"><span data-stu-id="af12b-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af12b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="af12b-114">Return value</span></span>

<span data-ttu-id="af12b-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="af12b-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="af12b-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="af12b-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="af12b-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="af12b-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="af12b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="af12b-118">Requirements</span></span>



| <span data-ttu-id="af12b-119">需求</span><span class="sxs-lookup"><span data-stu-id="af12b-119">Requirement</span></span> | <span data-ttu-id="af12b-120">值</span><span class="sxs-lookup"><span data-stu-id="af12b-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="af12b-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af12b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="af12b-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="af12b-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="af12b-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af12b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="af12b-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="af12b-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="af12b-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="af12b-125">Namespace</span></span><br/>                | <span data-ttu-id="af12b-126">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="af12b-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="af12b-127">MOF</span><span class="sxs-lookup"><span data-stu-id="af12b-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af12b-128"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="af12b-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="af12b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="af12b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af12b-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="af12b-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af12b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af12b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af12b-132">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="af12b-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






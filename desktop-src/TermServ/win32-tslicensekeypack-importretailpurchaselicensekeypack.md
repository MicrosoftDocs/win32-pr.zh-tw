---
title: Win32_TSLicenseKeyPack 類別的 ImportRetailPurchaseLicenseKeyPack 方法
description: 從另一部遠端桌面授權伺服器匯入，這是透過零售通路購買的遠端桌面服務授權金鑰套件。
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- ImportRetailPurchaseLicenseKeyPack 方法遠端桌面服務
- ImportRetailPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ImportRetailPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685974"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e6ed6-106">Win32 TSLicenseKeyPack 類別的 ImportRetailPurchaseLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e6ed6-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e6ed6-107">從另一部遠端桌面授權伺服器匯入，這是透過零售通路購買的遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ed6-108">語法</span><span class="sxs-lookup"><span data-stu-id="e6ed6-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e6ed6-109">參數</span><span class="sxs-lookup"><span data-stu-id="e6ed6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6ed6-110">*sLicenseCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6ed6-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ed6-111">包含25個字元的授權碼。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-111">Contains the 25-character license code.</span></span> <span data-ttu-id="e6ed6-112">只應提供25個字元的英數位元字串做為輸入。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="e6ed6-113">不應新增連字號。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="e6ed6-114">*sSourceLSName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6ed6-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ed6-115">來源遠端桌面授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="e6ed6-116">這可以是完整的辨別名稱或伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="e6ed6-117">*sSourceLSProductId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6ed6-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ed6-118">遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="e6ed6-119">是35字元的英數位元字串，不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="e6ed6-120">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e6ed6-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6ed6-121">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6ed6-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6ed6-122">Return value</span></span>

<span data-ttu-id="e6ed6-123">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e6ed6-124">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e6ed6-125">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e6ed6-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ed6-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6ed6-126">Requirements</span></span>



| <span data-ttu-id="e6ed6-127">需求</span><span class="sxs-lookup"><span data-stu-id="e6ed6-127">Requirement</span></span> | <span data-ttu-id="e6ed6-128">值</span><span class="sxs-lookup"><span data-stu-id="e6ed6-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ed6-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6ed6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e6ed6-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="e6ed6-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e6ed6-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6ed6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e6ed6-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6ed6-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e6ed6-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="e6ed6-133">Namespace</span></span><br/>                | <span data-ttu-id="e6ed6-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e6ed6-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e6ed6-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e6ed6-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6ed6-136"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6ed6-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6ed6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e6ed6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6ed6-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6ed6-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ed6-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6ed6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ed6-140">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="e6ed6-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






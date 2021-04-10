---
title: Win32_TSLicenseKeyPack 類別的 ReinstallOpenPurchaseLicenseKeyPack 方法
description: 重新安裝 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- ReinstallOpenPurchaseLicenseKeyPack 方法遠端桌面服務
- ReinstallOpenPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallOpenPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686350"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="d1bf8-106">Win32 TSLicenseKeyPack 類別的 ReinstallOpenPurchaseLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d1bf8-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="d1bf8-107">重新安裝 Open License 遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1bf8-108">語法</span><span class="sxs-lookup"><span data-stu-id="d1bf8-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="d1bf8-109">參數</span><span class="sxs-lookup"><span data-stu-id="d1bf8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1bf8-110">*sLicenseNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-111">授權金鑰套件所提供的8個字元數位字串。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="d1bf8-112">*SLicenseNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-113">*sAuthorizationNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-114">以授權金鑰提供的15個字元的英數位元字串。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="d1bf8-115">*SAuthorizationNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-116">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-117">產品版本。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-117">Product version.</span></span>

<dt>

<span data-ttu-id="d1bf8-118">0</span><span class="sxs-lookup"><span data-stu-id="d1bf8-118">0</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-119">不支援。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-120">1</span><span class="sxs-lookup"><span data-stu-id="d1bf8-120">1</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-121">不支援。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-122">2</span><span class="sxs-lookup"><span data-stu-id="d1bf8-122">2</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1bf8-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d1bf8-124">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-125">產品類型。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-125">Product type.</span></span>

<dt>

<span data-ttu-id="d1bf8-126">0</span><span class="sxs-lookup"><span data-stu-id="d1bf8-126">0</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-127">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="d1bf8-128">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-129">1</span><span class="sxs-lookup"><span data-stu-id="d1bf8-129">1</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-130">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="d1bf8-131">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-132">2</span><span class="sxs-lookup"><span data-stu-id="d1bf8-132">2</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-133">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d1bf8-134">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-135">要安裝的授權數目。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="d1bf8-136">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d1bf8-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1bf8-137">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1bf8-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1bf8-138">Return value</span></span>

<span data-ttu-id="d1bf8-139">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d1bf8-140">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d1bf8-141">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="d1bf8-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1bf8-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1bf8-142">Requirements</span></span>



| <span data-ttu-id="d1bf8-143">需求</span><span class="sxs-lookup"><span data-stu-id="d1bf8-143">Requirement</span></span> | <span data-ttu-id="d1bf8-144">值</span><span class="sxs-lookup"><span data-stu-id="d1bf8-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1bf8-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1bf8-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d1bf8-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="d1bf8-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="d1bf8-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1bf8-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d1bf8-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1bf8-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="d1bf8-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1bf8-149">Namespace</span></span><br/>                | <span data-ttu-id="d1bf8-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d1bf8-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="d1bf8-151">MOF</span><span class="sxs-lookup"><span data-stu-id="d1bf8-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1bf8-152"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1bf8-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1bf8-153">DLL</span><span class="sxs-lookup"><span data-stu-id="d1bf8-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1bf8-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1bf8-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1bf8-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1bf8-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1bf8-156">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="d1bf8-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






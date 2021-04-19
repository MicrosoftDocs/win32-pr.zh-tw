---
title: Win32_TSLicenseKeyPack 類別的 ImportOpenPurchaseLicenseKeyPack 方法
description: 從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- ImportOpenPurchaseLicenseKeyPack 方法遠端桌面服務
- ImportOpenPurchaseLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ImportOpenPurchaseLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976975"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="8f00b-106">Win32 TSLicenseKeyPack 類別的 ImportOpenPurchaseLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8f00b-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="8f00b-107">從另一部遠端桌面授權伺服器匯入 Open License 遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="8f00b-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f00b-108">語法</span><span class="sxs-lookup"><span data-stu-id="8f00b-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="8f00b-109">參數</span><span class="sxs-lookup"><span data-stu-id="8f00b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f00b-110">*sLicenseNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-111">授權金鑰套件所提供的8個字元數位字串。</span><span class="sxs-lookup"><span data-stu-id="8f00b-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="8f00b-112">*SLicenseNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="8f00b-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-113">*sAuthorizationNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-114">以授權金鑰提供的15個字元的英數位元字串。</span><span class="sxs-lookup"><span data-stu-id="8f00b-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="8f00b-115">*SAuthorizationNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="8f00b-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-116">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-117">產品版本。</span><span class="sxs-lookup"><span data-stu-id="8f00b-117">Product version.</span></span>

<dt>

<span data-ttu-id="8f00b-118">0</span><span class="sxs-lookup"><span data-stu-id="8f00b-118">0</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-119">不支援。</span><span class="sxs-lookup"><span data-stu-id="8f00b-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-120">1</span><span class="sxs-lookup"><span data-stu-id="8f00b-120">1</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-121">不支援。</span><span class="sxs-lookup"><span data-stu-id="8f00b-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-122">2</span><span class="sxs-lookup"><span data-stu-id="8f00b-122">2</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f00b-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8f00b-124">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-125">產品類型。</span><span class="sxs-lookup"><span data-stu-id="8f00b-125">Product type.</span></span>

<dt>

<span data-ttu-id="8f00b-126">0</span><span class="sxs-lookup"><span data-stu-id="8f00b-126">0</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-127">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="8f00b-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="8f00b-128">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="8f00b-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-129">1</span><span class="sxs-lookup"><span data-stu-id="8f00b-129">1</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-130">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="8f00b-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="8f00b-131">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="8f00b-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-132">2</span><span class="sxs-lookup"><span data-stu-id="8f00b-132">2</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-133">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="8f00b-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8f00b-134">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-135">要匯入的授權數目</span><span class="sxs-lookup"><span data-stu-id="8f00b-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-136">*sSourceLSName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-137">來源遠端桌面授權伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8f00b-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="8f00b-138">這可以是完整的辨別名稱或伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="8f00b-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-139">*sSourceLSProductId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-140">遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f00b-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="8f00b-141">是35字元的英數位元字串，不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="8f00b-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="8f00b-142">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f00b-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f00b-143">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8f00b-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f00b-144">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f00b-144">Return value</span></span>

<span data-ttu-id="8f00b-145">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="8f00b-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8f00b-146">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="8f00b-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8f00b-147">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="8f00b-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f00b-148">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f00b-148">Requirements</span></span>



| <span data-ttu-id="8f00b-149">需求</span><span class="sxs-lookup"><span data-stu-id="8f00b-149">Requirement</span></span> | <span data-ttu-id="8f00b-150">值</span><span class="sxs-lookup"><span data-stu-id="8f00b-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f00b-151">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f00b-151">Minimum supported client</span></span><br/> | <span data-ttu-id="8f00b-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="8f00b-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8f00b-153">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f00b-153">Minimum supported server</span></span><br/> | <span data-ttu-id="8f00b-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f00b-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8f00b-155">命名空間</span><span class="sxs-lookup"><span data-stu-id="8f00b-155">Namespace</span></span><br/>                | <span data-ttu-id="8f00b-156">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8f00b-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8f00b-157">MOF</span><span class="sxs-lookup"><span data-stu-id="8f00b-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8f00b-158"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="8f00b-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8f00b-159">DLL</span><span class="sxs-lookup"><span data-stu-id="8f00b-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f00b-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f00b-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f00b-161">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f00b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f00b-162">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="8f00b-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






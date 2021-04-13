---
title: Win32_TSLicenseKeyPack 類別的 ReinstallAgreementLicenseKeyPack 方法
description: 重新安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。
ms.assetid: BC3C966B-E6CE-45E2-BC1D-2439B75D4C3C
ms.tgt_platform: multiple
keywords:
- ReinstallAgreementLicenseKeyPack 方法遠端桌面服務
- ReinstallAgreementLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，ReinstallAgreementLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821ff6dc538a670e03757253b616ff16489dc108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508635"
---
# <a name="reinstallagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="61687-106">Win32 TSLicenseKeyPack 類別的 ReinstallAgreementLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61687-106">ReinstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="61687-107">重新安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。</span><span class="sxs-lookup"><span data-stu-id="61687-107">Reinstalls a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="61687-108">語法</span><span class="sxs-lookup"><span data-stu-id="61687-108">Syntax</span></span>


```mof
uint32 ReinstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="61687-109">參數</span><span class="sxs-lookup"><span data-stu-id="61687-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61687-110">*AgreementType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61687-110">*AgreementType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-111">合約類型。</span><span class="sxs-lookup"><span data-stu-id="61687-111">Agreement type.</span></span>

<dt>

<span data-ttu-id="61687-112">0</span><span class="sxs-lookup"><span data-stu-id="61687-112">0</span></span>
</dt> <dd>

<span data-ttu-id="61687-113">授權金鑰套件來自選取的大量授權合約 (，適用于具有250或更多電腦) 的客戶。</span><span class="sxs-lookup"><span data-stu-id="61687-113">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="61687-114">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-114">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="61687-115">1</span><span class="sxs-lookup"><span data-stu-id="61687-115">1</span></span>
</dt> <dd>

<span data-ttu-id="61687-116">授權金鑰套件是針對具有250或更多電腦的客戶提供的 Enterprise volume 授權合約。</span><span class="sxs-lookup"><span data-stu-id="61687-116">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="61687-117">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-117">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="61687-118">2</span><span class="sxs-lookup"><span data-stu-id="61687-118">2</span></span>
</dt> <dd>

<span data-ttu-id="61687-119">授權金鑰套件來自較高教育機構的校園大量授權合約。</span><span class="sxs-lookup"><span data-stu-id="61687-119">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="61687-120">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-120">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="61687-121">3</span><span class="sxs-lookup"><span data-stu-id="61687-121">3</span></span>
</dt> <dd>

<span data-ttu-id="61687-122">授權金鑰套件來自主要和次要機構的學校大量授權合約。</span><span class="sxs-lookup"><span data-stu-id="61687-122">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="61687-123">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-123">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="61687-124">4</span><span class="sxs-lookup"><span data-stu-id="61687-124">4</span></span>
</dt> <dd>

<span data-ttu-id="61687-125">授權金鑰套件來自服務提供者的服務提供者授權合約，可讓您每月授權 Microsoft 軟體。</span><span class="sxs-lookup"><span data-stu-id="61687-125">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="61687-126">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-126">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span>

</dd> <dt>

<span data-ttu-id="61687-127">5</span><span class="sxs-lookup"><span data-stu-id="61687-127">5</span></span>
</dt> <dd>

<span data-ttu-id="61687-128">授權金鑰套件來自另一個授權合約，例如開放價值、多年 Open License，以及 Open 訂用帳戶授權。</span><span class="sxs-lookup"><span data-stu-id="61687-128">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="61687-129">*SAgreementNumber* 參數是與您的程式資訊一起提供的合約編號。</span><span class="sxs-lookup"><span data-stu-id="61687-129">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61687-130">*sAgreementNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61687-130">*sAgreementNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-131">合約編號或註冊編號。</span><span class="sxs-lookup"><span data-stu-id="61687-131">Agreement number or enrollment number.</span></span> <span data-ttu-id="61687-132">*SAgreementNumber* 參數是不含連字號的七位數數位字串。</span><span class="sxs-lookup"><span data-stu-id="61687-132">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="61687-133">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61687-133">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-134">產品版本。</span><span class="sxs-lookup"><span data-stu-id="61687-134">Product version.</span></span>

<dt>

<span data-ttu-id="61687-135">0</span><span class="sxs-lookup"><span data-stu-id="61687-135">0</span></span>
</dt> <dd>

<span data-ttu-id="61687-136">不支援。</span><span class="sxs-lookup"><span data-stu-id="61687-136">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="61687-137">1</span><span class="sxs-lookup"><span data-stu-id="61687-137">1</span></span>
</dt> <dd>

<span data-ttu-id="61687-138">不支援。</span><span class="sxs-lookup"><span data-stu-id="61687-138">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="61687-139">2</span><span class="sxs-lookup"><span data-stu-id="61687-139">2</span></span>
</dt> <dd>

<span data-ttu-id="61687-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61687-140">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61687-141">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61687-141">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-142">產品類型。</span><span class="sxs-lookup"><span data-stu-id="61687-142">Product type.</span></span>

<dt>

<span data-ttu-id="61687-143">0</span><span class="sxs-lookup"><span data-stu-id="61687-143">0</span></span>
</dt> <dd>

<span data-ttu-id="61687-144">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="61687-144">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="61687-145">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="61687-145">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="61687-146">1</span><span class="sxs-lookup"><span data-stu-id="61687-146">1</span></span>
</dt> <dd>

<span data-ttu-id="61687-147">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="61687-147">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="61687-148">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="61687-148">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="61687-149">2</span><span class="sxs-lookup"><span data-stu-id="61687-149">2</span></span>
</dt> <dd>

<span data-ttu-id="61687-150">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="61687-150">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="61687-151">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61687-151">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-152">要安裝的授權數目。</span><span class="sxs-lookup"><span data-stu-id="61687-152">Number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="61687-153">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61687-153">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61687-154">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="61687-154">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61687-155">傳回值</span><span class="sxs-lookup"><span data-stu-id="61687-155">Return value</span></span>

<span data-ttu-id="61687-156">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="61687-156">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="61687-157">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="61687-157">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="61687-158">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="61687-158">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61687-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="61687-159">Requirements</span></span>



| <span data-ttu-id="61687-160">需求</span><span class="sxs-lookup"><span data-stu-id="61687-160">Requirement</span></span> | <span data-ttu-id="61687-161">值</span><span class="sxs-lookup"><span data-stu-id="61687-161">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="61687-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61687-162">Minimum supported client</span></span><br/> | <span data-ttu-id="61687-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="61687-163">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="61687-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61687-164">Minimum supported server</span></span><br/> | <span data-ttu-id="61687-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61687-165">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="61687-166">命名空間</span><span class="sxs-lookup"><span data-stu-id="61687-166">Namespace</span></span><br/>                | <span data-ttu-id="61687-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="61687-167">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="61687-168">MOF</span><span class="sxs-lookup"><span data-stu-id="61687-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61687-169"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="61687-169"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="61687-170">DLL</span><span class="sxs-lookup"><span data-stu-id="61687-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61687-171"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61687-171"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61687-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61687-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61687-173">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="61687-173">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






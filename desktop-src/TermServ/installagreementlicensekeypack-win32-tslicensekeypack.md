---
title: Win32_TSLicenseKeyPack 類別的 InstallAgreementLicenseKeyPack 方法
description: 安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- InstallAgreementLicenseKeyPack 方法遠端桌面服務
- InstallAgreementLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallAgreementLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968791"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="37d72-106">Win32 TSLicenseKeyPack 類別的 InstallAgreementLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="37d72-106">InstallAgreementLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="37d72-107">安裝透過授權合約購買的遠端桌面服務授權金鑰套件，並透過網際網路自動連接以驗證金鑰套件授權。</span><span class="sxs-lookup"><span data-stu-id="37d72-107">Installs a Remote Desktop Services license key pack that was purchased through a license agreement, and automatically connects over the Internet to validate the key pack license.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d72-108">語法</span><span class="sxs-lookup"><span data-stu-id="37d72-108">Syntax</span></span>


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="37d72-109">參數</span><span class="sxs-lookup"><span data-stu-id="37d72-109">Parameters</span></span>

<span data-ttu-id="37d72-110">*AgreementType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37d72-110">*AgreementType* \[in\]</span></span>

<span data-ttu-id="37d72-111">合約類型。</span><span class="sxs-lookup"><span data-stu-id="37d72-111">Agreement type.</span></span>

| <span data-ttu-id="37d72-112">值</span><span class="sxs-lookup"><span data-stu-id="37d72-112">Value</span></span> | <span data-ttu-id="37d72-113">描述</span><span class="sxs-lookup"><span data-stu-id="37d72-113">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="37d72-114">0</span><span class="sxs-lookup"><span data-stu-id="37d72-114">0</span></span> | <span data-ttu-id="37d72-115">授權金鑰套件來自選取的大量授權合約 (，適用于具有250或更多電腦) 的客戶。</span><span class="sxs-lookup"><span data-stu-id="37d72-115">The license key pack is from a Select volume license agreement (for customers with 250 or more computers).</span></span> <span data-ttu-id="37d72-116">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-116">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="37d72-117">1</span><span class="sxs-lookup"><span data-stu-id="37d72-117">1</span></span> | <span data-ttu-id="37d72-118">授權金鑰套件是針對具有250或更多電腦的客戶提供的 Enterprise volume 授權合約。</span><span class="sxs-lookup"><span data-stu-id="37d72-118">The license key pack is from an Enterprise volume license agreement for customers with 250 or more computers.</span></span> <span data-ttu-id="37d72-119">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-119">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="37d72-120">2</span><span class="sxs-lookup"><span data-stu-id="37d72-120">2</span></span> | <span data-ttu-id="37d72-121">授權金鑰套件來自較高教育機構的校園大量授權合約。</span><span class="sxs-lookup"><span data-stu-id="37d72-121">The license key pack is from a Campus volume license agreement for a higher education institution.</span></span> <span data-ttu-id="37d72-122">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-122">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="37d72-123">3</span><span class="sxs-lookup"><span data-stu-id="37d72-123">3</span></span> | <span data-ttu-id="37d72-124">授權金鑰套件來自主要和次要機構的學校大量授權合約。</span><span class="sxs-lookup"><span data-stu-id="37d72-124">The license key pack is from a School volume license agreement for primary and secondary institutions.</span></span> <span data-ttu-id="37d72-125">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-125">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="37d72-126">4</span><span class="sxs-lookup"><span data-stu-id="37d72-126">4</span></span> | <span data-ttu-id="37d72-127">授權金鑰套件來自服務提供者的服務提供者授權合約，可讓您每月授權 Microsoft 軟體。</span><span class="sxs-lookup"><span data-stu-id="37d72-127">The license key pack is from a Service Provider license agreement for service providers to license Microsoft software on a monthly basis.</span></span> <span data-ttu-id="37d72-128">*SAgreementNumber* 參數是在簽署的合約表單上) 找到的 (七個數字的註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-128">The *sAgreementNumber* parameter is the enrollment number (seven numeric digits) found on the signed agreement form.</span></span> |
| <span data-ttu-id="37d72-129">5</span><span class="sxs-lookup"><span data-stu-id="37d72-129">5</span></span> | <span data-ttu-id="37d72-130">授權金鑰套件來自另一個授權合約，例如開放價值、多年 Open License，以及 Open 訂用帳戶授權。</span><span class="sxs-lookup"><span data-stu-id="37d72-130">The license key pack is from another license agreement, such as Open Value, Multi-Year Open License, and Open Subscription License.</span></span> <span data-ttu-id="37d72-131">*SAgreementNumber* 參數是與您的程式資訊一起提供的合約編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-131">The *sAgreementNumber* parameter is the agreement number provided with your program information.</span></span> |

<span data-ttu-id="37d72-132">*sAgreementNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37d72-132">*sAgreementNumber* \[in\]</span></span>

<span data-ttu-id="37d72-133">合約編號或註冊編號。</span><span class="sxs-lookup"><span data-stu-id="37d72-133">Agreement number or enrollment number.</span></span> <span data-ttu-id="37d72-134">*SAgreementNumber* 參數是不含連字號的七位數數位字串。</span><span class="sxs-lookup"><span data-stu-id="37d72-134">The *sAgreementNumber* parameter is a seven digit numeric string without hyphens.</span></span>

<span data-ttu-id="37d72-135">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37d72-135">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="37d72-136">產品版本。</span><span class="sxs-lookup"><span data-stu-id="37d72-136">Product version.</span></span>

| <span data-ttu-id="37d72-137">值</span><span class="sxs-lookup"><span data-stu-id="37d72-137">Value</span></span> | <span data-ttu-id="37d72-138">描述</span><span class="sxs-lookup"><span data-stu-id="37d72-138">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="37d72-139">0</span><span class="sxs-lookup"><span data-stu-id="37d72-139">0</span></span> | <span data-ttu-id="37d72-140">不支援</span><span class="sxs-lookup"><span data-stu-id="37d72-140">Not supported</span></span> |
| <span data-ttu-id="37d72-141">1</span><span class="sxs-lookup"><span data-stu-id="37d72-141">1</span></span> | <span data-ttu-id="37d72-142">不支援</span><span class="sxs-lookup"><span data-stu-id="37d72-142">Not supported</span></span> |
| <span data-ttu-id="37d72-143">2</span><span class="sxs-lookup"><span data-stu-id="37d72-143">2</span></span> | <span data-ttu-id="37d72-144">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37d72-144">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="37d72-145">4</span><span class="sxs-lookup"><span data-stu-id="37d72-145">4</span></span> | <span data-ttu-id="37d72-146">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="37d72-146">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="37d72-147">5</span><span class="sxs-lookup"><span data-stu-id="37d72-147">5</span></span> | <span data-ttu-id="37d72-148">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="37d72-148">Windows Server 2016</span></span> |
| <span data-ttu-id="37d72-149">6</span><span class="sxs-lookup"><span data-stu-id="37d72-149">6</span></span> | <span data-ttu-id="37d72-150">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="37d72-150">Windows Server 2019</span></span> |

<span data-ttu-id="37d72-151">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37d72-151">*ProductType* \[in\]</span></span>

<span data-ttu-id="37d72-152">產品類型。</span><span class="sxs-lookup"><span data-stu-id="37d72-152">Product type.</span></span>

| <span data-ttu-id="37d72-153">值</span><span class="sxs-lookup"><span data-stu-id="37d72-153">Value</span></span> | <span data-ttu-id="37d72-154">描述</span><span class="sxs-lookup"><span data-stu-id="37d72-154">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="37d72-155">0</span><span class="sxs-lookup"><span data-stu-id="37d72-155">0</span></span> | <span data-ttu-id="37d72-156">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="37d72-156">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="37d72-157">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="37d72-157">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="37d72-158">1</span><span class="sxs-lookup"><span data-stu-id="37d72-158">1</span></span> | <span data-ttu-id="37d72-159">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="37d72-159">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="37d72-160">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="37d72-160">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="37d72-161">2</span><span class="sxs-lookup"><span data-stu-id="37d72-161">2</span></span> | <span data-ttu-id="37d72-162">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="37d72-162">This product type is not valid.</span></span> |

<span data-ttu-id="37d72-163">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="37d72-163">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="37d72-164">要安裝的授權數目。</span><span class="sxs-lookup"><span data-stu-id="37d72-164">Number of licenses to install.</span></span>

<span data-ttu-id="37d72-165">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="37d72-165">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="37d72-166">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="37d72-166">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="37d72-167">傳回值</span><span class="sxs-lookup"><span data-stu-id="37d72-167">Return value</span></span>

<span data-ttu-id="37d72-168">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="37d72-168">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="37d72-169">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="37d72-169">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="37d72-170">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="37d72-170">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="37d72-171">備註</span><span class="sxs-lookup"><span data-stu-id="37d72-171">Remarks</span></span>

<span data-ttu-id="37d72-172">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="37d72-172">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="37d72-173">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="37d72-173">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="37d72-174">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="37d72-174">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="37d72-175">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="37d72-175">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="37d72-176">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="37d72-176">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="37d72-177">規格需求</span><span class="sxs-lookup"><span data-stu-id="37d72-177">Requirements</span></span>

| <span data-ttu-id="37d72-178">需求</span><span class="sxs-lookup"><span data-stu-id="37d72-178">Requirement</span></span> | <span data-ttu-id="37d72-179">值</span><span class="sxs-lookup"><span data-stu-id="37d72-179">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="37d72-180">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="37d72-180">Minimum supported client</span></span><br/> | <span data-ttu-id="37d72-181">都不支援</span><span class="sxs-lookup"><span data-stu-id="37d72-181">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="37d72-182">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="37d72-182">Minimum supported server</span></span><br/> | <span data-ttu-id="37d72-183">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="37d72-183">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="37d72-184">命名空間</span><span class="sxs-lookup"><span data-stu-id="37d72-184">Namespace</span></span><br/>                | <span data-ttu-id="37d72-185">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="37d72-185">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="37d72-186">MOF</span><span class="sxs-lookup"><span data-stu-id="37d72-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37d72-187"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="37d72-187"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37d72-188">DLL</span><span class="sxs-lookup"><span data-stu-id="37d72-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d72-189"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d72-189"><dt>TlsWmiProv.dll</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="37d72-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="37d72-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d72-191">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="37d72-191">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 


---
title: Win32_TSLicenseKeyPack 類別的 InstallOpenLicenseKeyPack 方法
description: 安裝 Open License 遠端桌面服務授權金鑰套件。
ms.assetid: be50e25c-cda3-408b-934b-51ce343f3271
ms.tgt_platform: multiple
keywords:
- InstallOpenLicenseKeyPack 方法遠端桌面服務
- InstallOpenLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，InstallOpenLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallOpenLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7335f25d3118c14f8cd0d27f72fd6a8d4cf1e0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464793"
---
# <a name="installopenlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="71088-106">Win32 TSLicenseKeyPack 類別的 InstallOpenLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="71088-106">InstallOpenLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="71088-107">安裝 Open License 遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="71088-107">Installs an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="71088-108">語法</span><span class="sxs-lookup"><span data-stu-id="71088-108">Syntax</span></span>


```mof
uint32 InstallOpenLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a><span data-ttu-id="71088-109">參數</span><span class="sxs-lookup"><span data-stu-id="71088-109">Parameters</span></span>

<span data-ttu-id="71088-110">*sLicenseNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71088-110">*sLicenseNumber* \[in\]</span></span>

<span data-ttu-id="71088-111">授權金鑰套件所提供的8個字元數位字串。</span><span class="sxs-lookup"><span data-stu-id="71088-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="71088-112">*SLicenseNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="71088-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="71088-113">*sAuthorizationNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71088-113">*sAuthorizationNumber* \[in\]</span></span>

<span data-ttu-id="71088-114">以授權金鑰提供的15個字元的英數位元字串。</span><span class="sxs-lookup"><span data-stu-id="71088-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="71088-115">*SAuthorizationNumber* 參數不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="71088-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

<span data-ttu-id="71088-116">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71088-116">*ProductVersion* \[in\]</span></span>

<span data-ttu-id="71088-117">產品版本。</span><span class="sxs-lookup"><span data-stu-id="71088-117">Product version.</span></span>

| <span data-ttu-id="71088-118">值</span><span class="sxs-lookup"><span data-stu-id="71088-118">Value</span></span> | <span data-ttu-id="71088-119">描述</span><span class="sxs-lookup"><span data-stu-id="71088-119">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="71088-120">0</span><span class="sxs-lookup"><span data-stu-id="71088-120">0</span></span> | <span data-ttu-id="71088-121">不支援</span><span class="sxs-lookup"><span data-stu-id="71088-121">Not supported</span></span> |
| <span data-ttu-id="71088-122">1</span><span class="sxs-lookup"><span data-stu-id="71088-122">1</span></span> | <span data-ttu-id="71088-123">不支援</span><span class="sxs-lookup"><span data-stu-id="71088-123">Not supported</span></span> |
| <span data-ttu-id="71088-124">2</span><span class="sxs-lookup"><span data-stu-id="71088-124">2</span></span> | <span data-ttu-id="71088-125">Windows Server 2008/Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="71088-125">Windows Server 2008/Windows Server 2008 R2</span></span> |
| <span data-ttu-id="71088-126">4</span><span class="sxs-lookup"><span data-stu-id="71088-126">4</span></span> | <span data-ttu-id="71088-127">Windows Server 2012/Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="71088-127">Windows Server 2012/Windows Server 2012 R2</span></span> |
| <span data-ttu-id="71088-128">5</span><span class="sxs-lookup"><span data-stu-id="71088-128">5</span></span> | <span data-ttu-id="71088-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="71088-129">Windows Server 2016</span></span> |
| <span data-ttu-id="71088-130">6</span><span class="sxs-lookup"><span data-stu-id="71088-130">6</span></span> | <span data-ttu-id="71088-131">Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="71088-131">Windows Server 2019</span></span> |

<span data-ttu-id="71088-132">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71088-132">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71088-133">產品類型。</span><span class="sxs-lookup"><span data-stu-id="71088-133">Product type.</span></span>

| <span data-ttu-id="71088-134">值</span><span class="sxs-lookup"><span data-stu-id="71088-134">Value</span></span> | <span data-ttu-id="71088-135">描述</span><span class="sxs-lookup"><span data-stu-id="71088-135">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="71088-136">0</span><span class="sxs-lookup"><span data-stu-id="71088-136">0</span></span> | <span data-ttu-id="71088-137">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="71088-137">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="71088-138">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="71088-138">Therefore, each device that connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="71088-139">1</span><span class="sxs-lookup"><span data-stu-id="71088-139">1</span></span> | <span data-ttu-id="71088-140">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="71088-140">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="71088-141">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="71088-141">Therefore, each user who connects to the RD Session Host server must have a license.</span></span> |
| <span data-ttu-id="71088-142">2</span><span class="sxs-lookup"><span data-stu-id="71088-142">2</span></span> | <span data-ttu-id="71088-143">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="71088-143">This product type is not valid.</span></span> |

<span data-ttu-id="71088-144">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="71088-144">*LicenseCount* \[in\]</span></span>

<span data-ttu-id="71088-145">要安裝的授權數目。</span><span class="sxs-lookup"><span data-stu-id="71088-145">The number of licenses to install.</span></span>

<span data-ttu-id="71088-146">*KeyPackId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="71088-146">*KeyPackId* \[out\]</span></span>

<span data-ttu-id="71088-147">接收金鑰組識別碼。</span><span class="sxs-lookup"><span data-stu-id="71088-147">Receives the key pack identifier.</span></span>

## <a name="return-value"></a><span data-ttu-id="71088-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="71088-148">Return value</span></span>

<span data-ttu-id="71088-149">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="71088-149">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="71088-150">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="71088-150">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="71088-151">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="71088-151">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="71088-152">備註</span><span class="sxs-lookup"><span data-stu-id="71088-152">Remarks</span></span>

<span data-ttu-id="71088-153">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="71088-153">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="71088-154">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="71088-154">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="71088-155">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="71088-155">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="71088-156">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="71088-156">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="71088-157">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="71088-157">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="71088-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="71088-158">Requirements</span></span>



| <span data-ttu-id="71088-159">需求</span><span class="sxs-lookup"><span data-stu-id="71088-159">Requirement</span></span> | <span data-ttu-id="71088-160">值</span><span class="sxs-lookup"><span data-stu-id="71088-160">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="71088-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="71088-161">Minimum supported client</span></span><br/> | <span data-ttu-id="71088-162">都不支援</span><span class="sxs-lookup"><span data-stu-id="71088-162">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="71088-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="71088-163">Minimum supported server</span></span><br/> | <span data-ttu-id="71088-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="71088-164">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="71088-165">命名空間</span><span class="sxs-lookup"><span data-stu-id="71088-165">Namespace</span></span><br/>                | <span data-ttu-id="71088-166">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="71088-166">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="71088-167">MOF</span><span class="sxs-lookup"><span data-stu-id="71088-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="71088-168"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="71088-168"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="71088-169">DLL</span><span class="sxs-lookup"><span data-stu-id="71088-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71088-170"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71088-170"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71088-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71088-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71088-172">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="71088-172">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 


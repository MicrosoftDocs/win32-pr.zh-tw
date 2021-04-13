---
title: Win32_TSLicenseKeyPack 類別的 UninstallLicenseKeyPack 方法
description: 卸載遠端桌面服務授權金鑰套件。
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- UninstallLicenseKeyPack 方法遠端桌面服務
- UninstallLicenseKeyPack 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，UninstallLicenseKeyPack 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383954"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="f6d05-106">Win32 TSLicenseKeyPack 類別的 UninstallLicenseKeyPack 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f6d05-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="f6d05-107">卸載遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="f6d05-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d05-108">語法</span><span class="sxs-lookup"><span data-stu-id="f6d05-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="f6d05-109">參數</span><span class="sxs-lookup"><span data-stu-id="f6d05-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6d05-110">*ProductVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d05-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-111">遠端桌面服務授權金鑰套件的產品版本識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6d05-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="f6d05-112">0</span><span class="sxs-lookup"><span data-stu-id="f6d05-112">0</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-113">不支援。</span><span class="sxs-lookup"><span data-stu-id="f6d05-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6d05-114">1</span><span class="sxs-lookup"><span data-stu-id="f6d05-114">1</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-115">不支援。</span><span class="sxs-lookup"><span data-stu-id="f6d05-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="f6d05-116">2</span><span class="sxs-lookup"><span data-stu-id="f6d05-116">2</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6d05-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6d05-118">*ProductType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d05-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-119">遠端桌面服務授權金鑰套件的產品類型。</span><span class="sxs-lookup"><span data-stu-id="f6d05-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="f6d05-120">0</span><span class="sxs-lookup"><span data-stu-id="f6d05-120">0</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-121">遠端桌面服務授權金鑰套件產品類型是依裝置。</span><span class="sxs-lookup"><span data-stu-id="f6d05-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="f6d05-122">因此，連接到 RD 工作階段主機伺服器的每個裝置都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="f6d05-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="f6d05-123">1</span><span class="sxs-lookup"><span data-stu-id="f6d05-123">1</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-124">遠端桌面服務的授權金鑰套件產品類型為 [每位使用者]。</span><span class="sxs-lookup"><span data-stu-id="f6d05-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="f6d05-125">因此，連接到 RD 工作階段主機伺服器的每個使用者都必須具有授權。</span><span class="sxs-lookup"><span data-stu-id="f6d05-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="f6d05-126">2</span><span class="sxs-lookup"><span data-stu-id="f6d05-126">2</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-127">此產品類型無效。</span><span class="sxs-lookup"><span data-stu-id="f6d05-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f6d05-128">*LicenseCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f6d05-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6d05-129">要卸載的授權數目。</span><span class="sxs-lookup"><span data-stu-id="f6d05-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6d05-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6d05-130">Return value</span></span>

<span data-ttu-id="f6d05-131">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f6d05-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="f6d05-132">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="f6d05-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="f6d05-133">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="f6d05-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6d05-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6d05-134">Requirements</span></span>



| <span data-ttu-id="f6d05-135">需求</span><span class="sxs-lookup"><span data-stu-id="f6d05-135">Requirement</span></span> | <span data-ttu-id="f6d05-136">值</span><span class="sxs-lookup"><span data-stu-id="f6d05-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6d05-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6d05-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f6d05-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="f6d05-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="f6d05-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6d05-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f6d05-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6d05-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="f6d05-141">命名空間</span><span class="sxs-lookup"><span data-stu-id="f6d05-141">Namespace</span></span><br/>                | <span data-ttu-id="f6d05-142">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f6d05-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="f6d05-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f6d05-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6d05-144"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6d05-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6d05-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f6d05-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6d05-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6d05-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6d05-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6d05-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d05-148">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="f6d05-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






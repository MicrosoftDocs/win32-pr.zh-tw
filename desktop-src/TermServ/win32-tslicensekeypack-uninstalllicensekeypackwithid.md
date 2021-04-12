---
title: Win32_TSLicenseKeyPack 類別的 UninstallLicenseKeyPackWithId 方法
description: 使用指定的金鑰套件識別碼卸載遠端桌面服務授權金鑰套件。
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- UninstallLicenseKeyPackWithId 方法遠端桌面服務
- UninstallLicenseKeyPackWithId 方法遠端桌面服務，Win32_TSLicenseKeyPack 類別
- Win32_TSLicenseKeyPack 類別遠端桌面服務，UninstallLicenseKeyPackWithId 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464477"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="b3209-106">Win32 TSLicenseKeyPack 類別的 UninstallLicenseKeyPackWithId 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b3209-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="b3209-107">使用指定的金鑰套件識別碼卸載遠端桌面服務授權金鑰套件。</span><span class="sxs-lookup"><span data-stu-id="b3209-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3209-108">語法</span><span class="sxs-lookup"><span data-stu-id="b3209-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="b3209-109">參數</span><span class="sxs-lookup"><span data-stu-id="b3209-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3209-110">*KeyPackId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3209-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3209-111">要卸載之金鑰套件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3209-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3209-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3209-112">Return value</span></span>

<span data-ttu-id="b3209-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b3209-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b3209-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="b3209-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b3209-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="b3209-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3209-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3209-116">Requirements</span></span>



| <span data-ttu-id="b3209-117">需求</span><span class="sxs-lookup"><span data-stu-id="b3209-117">Requirement</span></span> | <span data-ttu-id="b3209-118">值</span><span class="sxs-lookup"><span data-stu-id="b3209-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3209-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3209-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3209-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="b3209-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b3209-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3209-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3209-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3209-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b3209-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3209-123">Namespace</span></span><br/>                | <span data-ttu-id="b3209-124">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b3209-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b3209-125">MOF</span><span class="sxs-lookup"><span data-stu-id="b3209-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3209-126"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3209-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3209-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b3209-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3209-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3209-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3209-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3209-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3209-130">**Win32 \_ TSLicenseKeyPack**</span><span class="sxs-lookup"><span data-stu-id="b3209-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 






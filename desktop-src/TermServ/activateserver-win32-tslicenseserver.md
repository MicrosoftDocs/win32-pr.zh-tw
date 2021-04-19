---
title: Win32_TSLicenseServer 類別的 ActivateServer 方法
description: 使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，啟用遠端桌面授權伺服器。
ms.assetid: 628e87f0-600e-404d-a0b4-35f1570b4fc0
ms.tgt_platform: multiple
keywords:
- ActivateServer 方法遠端桌面服務
- ActivateServer 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ActivateServer 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19db0df0ca9b0bf41fe692ba07fe605dc1e8d5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969209"
---
# <a name="activateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="dfec1-106">Win32 TSLicenseServer 類別的 ActivateServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dfec1-106">ActivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="dfec1-107">使用透過電話或網際網路取得的遠端桌面授權伺服器識別碼，啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfec1-107">Activates the Remote Desktop license server by using a Remote Desktop license server identifier that is obtained over the phone or the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfec1-108">語法</span><span class="sxs-lookup"><span data-stu-id="dfec1-108">Syntax</span></span>


```mof
uint32 ActivateServer(
  [in]  string sLicenseServerId,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="dfec1-109">參數</span><span class="sxs-lookup"><span data-stu-id="dfec1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfec1-110">*sLicenseServerId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dfec1-110">*sLicenseServerId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfec1-111">透過電話或網際網路取得的遠端桌面授權伺服器識別碼。</span><span class="sxs-lookup"><span data-stu-id="dfec1-111">Remote Desktop license server ID that was obtained over the phone or the Internet.</span></span> <span data-ttu-id="dfec1-112">*SLicenseServerId* 參數是35字元的英數位元字串，不能包含連字號。</span><span class="sxs-lookup"><span data-stu-id="dfec1-112">The *sLicenseServerId* parameter is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="dfec1-113">*ActivationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dfec1-113">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfec1-114">傳回的啟用狀態可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="dfec1-114">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="dfec1-115">0</span><span class="sxs-lookup"><span data-stu-id="dfec1-115">0</span></span>
</dt> <dd>

<span data-ttu-id="dfec1-116">啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfec1-116">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="dfec1-117">1</span><span class="sxs-lookup"><span data-stu-id="dfec1-117">1</span></span>
</dt> <dd>

<span data-ttu-id="dfec1-118">未啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfec1-118">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="dfec1-119">2</span><span class="sxs-lookup"><span data-stu-id="dfec1-119">2</span></span>
</dt> <dd>

<span data-ttu-id="dfec1-120">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="dfec1-120">An unknown error occurred.</span></span> <span data-ttu-id="dfec1-121">不知道是否啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="dfec1-121">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfec1-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="dfec1-122">Return value</span></span>

<span data-ttu-id="dfec1-123">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="dfec1-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="dfec1-124">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="dfec1-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="dfec1-125">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="dfec1-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dfec1-126">備註</span><span class="sxs-lookup"><span data-stu-id="dfec1-126">Remarks</span></span>

<span data-ttu-id="dfec1-127">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="dfec1-127">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="dfec1-128">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="dfec1-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dfec1-129">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="dfec1-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="dfec1-130">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="dfec1-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dfec1-131">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="dfec1-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="dfec1-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="dfec1-132">Requirements</span></span>



| <span data-ttu-id="dfec1-133">需求</span><span class="sxs-lookup"><span data-stu-id="dfec1-133">Requirement</span></span> | <span data-ttu-id="dfec1-134">值</span><span class="sxs-lookup"><span data-stu-id="dfec1-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfec1-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dfec1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dfec1-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="dfec1-136">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="dfec1-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dfec1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dfec1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dfec1-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="dfec1-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="dfec1-139">Namespace</span></span><br/>                | <span data-ttu-id="dfec1-140">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="dfec1-140">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="dfec1-141">MOF</span><span class="sxs-lookup"><span data-stu-id="dfec1-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dfec1-142"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="dfec1-142"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dfec1-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dfec1-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfec1-144"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dfec1-144"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfec1-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dfec1-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfec1-146">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="dfec1-146">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


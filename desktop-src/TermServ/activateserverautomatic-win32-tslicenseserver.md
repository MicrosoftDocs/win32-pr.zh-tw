---
title: Win32_TSLicenseServer 類別的 ActivateServerAutomatic 方法
description: 透過網際網路自動啟用遠端桌面授權伺服器。
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- ActivateServerAutomatic 方法遠端桌面服務
- ActivateServerAutomatic 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，ActivateServerAutomatic 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934132"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="256e1-106">Win32 TSLicenseServer 類別的 ActivateServerAutomatic 方法 \_</span><span class="sxs-lookup"><span data-stu-id="256e1-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="256e1-107">透過網際網路自動啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="256e1-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="256e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="256e1-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="256e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="256e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="256e1-110">*ActivationStatus* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="256e1-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="256e1-111">傳回的啟用狀態可以是下列其中一項。</span><span class="sxs-lookup"><span data-stu-id="256e1-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="256e1-112">0</span><span class="sxs-lookup"><span data-stu-id="256e1-112">0</span></span>
</dt> <dd>

<span data-ttu-id="256e1-113">啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="256e1-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="256e1-114">1</span><span class="sxs-lookup"><span data-stu-id="256e1-114">1</span></span>
</dt> <dd>

<span data-ttu-id="256e1-115">未啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="256e1-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="256e1-116">2</span><span class="sxs-lookup"><span data-stu-id="256e1-116">2</span></span>
</dt> <dd>

<span data-ttu-id="256e1-117">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="256e1-117">An unknown error occurred.</span></span> <span data-ttu-id="256e1-118">不知道是否啟用遠端桌面授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="256e1-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="256e1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="256e1-119">Return value</span></span>

<span data-ttu-id="256e1-120">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="256e1-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="256e1-121">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="256e1-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="256e1-122">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="256e1-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="256e1-123">備註</span><span class="sxs-lookup"><span data-stu-id="256e1-123">Remarks</span></span>

<span data-ttu-id="256e1-124">除非已設定 **FirstName**、 **LastName**、 **Company** 和 **國家（地區** ）屬性，否則這個方法會失敗。</span><span class="sxs-lookup"><span data-stu-id="256e1-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="256e1-125">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="256e1-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="256e1-126">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="256e1-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="256e1-127">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="256e1-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="256e1-128">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="256e1-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="256e1-129">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="256e1-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="256e1-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="256e1-130">Requirements</span></span>



| <span data-ttu-id="256e1-131">需求</span><span class="sxs-lookup"><span data-stu-id="256e1-131">Requirement</span></span> | <span data-ttu-id="256e1-132">值</span><span class="sxs-lookup"><span data-stu-id="256e1-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="256e1-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="256e1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="256e1-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="256e1-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="256e1-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="256e1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="256e1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="256e1-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="256e1-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="256e1-137">Namespace</span></span><br/>                | <span data-ttu-id="256e1-138">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="256e1-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="256e1-139">MOF</span><span class="sxs-lookup"><span data-stu-id="256e1-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="256e1-140"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="256e1-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="256e1-141">DLL</span><span class="sxs-lookup"><span data-stu-id="256e1-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="256e1-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="256e1-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="256e1-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="256e1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="256e1-144">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="256e1-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 


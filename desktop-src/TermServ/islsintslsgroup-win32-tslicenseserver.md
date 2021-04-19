---
title: Win32_TSLicenseServer 類別的 IsLSinTSLSGroup 方法
description: 抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。
ms.assetid: a6ad7f09-8972-47d4-8b3b-cd129b400ea8
ms.tgt_platform: multiple
keywords:
- IsLSinTSLSGroup 方法遠端桌面服務
- IsLSinTSLSGroup 方法遠端桌面服務，Win32_TSLicenseServer 類別
- Win32_TSLicenseServer 類別遠端桌面服務，IsLSinTSLSGroup 方法
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSinTSLSGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de3577e4632167612b4d71841501a2a2845203a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993748"
---
# <a name="islsintslsgroup-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="b39b8-106">Win32 TSLicenseServer 類別的 IsLSinTSLSGroup 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b39b8-106">IsLSinTSLSGroup method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="b39b8-107">抓取遠端桌面授權伺服器是否為指定網域中網域控制站上的遠端桌面授權伺服器群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b39b8-107">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop license server group on a domain controller in a given domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="b39b8-108">語法</span><span class="sxs-lookup"><span data-stu-id="b39b8-108">Syntax</span></span>


```mof
uint32 IsLSinTSLSGroup(
  [in]  string  Domain,
  [out] boolean IsMember
);
```



## <a name="parameters"></a><span data-ttu-id="b39b8-109">參數</span><span class="sxs-lookup"><span data-stu-id="b39b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b39b8-110">*網域* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b39b8-110">*Domain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b39b8-111">網域名稱。</span><span class="sxs-lookup"><span data-stu-id="b39b8-111">The domain name.</span></span>

</dd> <dt>

<span data-ttu-id="b39b8-112">*IsMember* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b39b8-112">*IsMember* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b39b8-113">布林值，指出授權伺服器是否為網域中的遠端桌面授權伺服器群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b39b8-113">Boolean value that indicates whether the license server is a member of the Remote Desktop license server group in the domain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b39b8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="b39b8-114">Return value</span></span>

<span data-ttu-id="b39b8-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="b39b8-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b39b8-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="b39b8-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b39b8-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="b39b8-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b39b8-118">備註</span><span class="sxs-lookup"><span data-stu-id="b39b8-118">Remarks</span></span>

<span data-ttu-id="b39b8-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="b39b8-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b39b8-120">如果未提供功能變數名稱，則會查詢授權伺服器所在網域中的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="b39b8-120">If no domain name is provided, a domain controller in the same domain as the license server is queried.</span></span>

<span data-ttu-id="b39b8-121">如果伺服器設定為使用網域或樹系探索領域，則授權伺服器應為遠端桌面授權伺服器群組的成員。</span><span class="sxs-lookup"><span data-stu-id="b39b8-121">The license server should be a member of the Remote Desktop license server group if the server is configured to use the domain or forest discovery scope.</span></span> <span data-ttu-id="b39b8-122">如果授權伺服器不是此群組的成員，則每位使用者的授權追蹤和報告將無法運作。</span><span class="sxs-lookup"><span data-stu-id="b39b8-122">If the license server is not a member of this group, per-user license tracking and reporting will not work.</span></span>

<span data-ttu-id="b39b8-123">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="b39b8-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b39b8-124">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b39b8-124">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b39b8-125">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="b39b8-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b39b8-126">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="b39b8-126">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b39b8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b39b8-127">Requirements</span></span>



| <span data-ttu-id="b39b8-128">需求</span><span class="sxs-lookup"><span data-stu-id="b39b8-128">Requirement</span></span> | <span data-ttu-id="b39b8-129">值</span><span class="sxs-lookup"><span data-stu-id="b39b8-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b39b8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b39b8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b39b8-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="b39b8-131">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="b39b8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b39b8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b39b8-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b39b8-133">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="b39b8-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="b39b8-134">Namespace</span></span><br/>                | <span data-ttu-id="b39b8-135">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b39b8-135">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="b39b8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b39b8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b39b8-137"><dt>TlsWmiProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b39b8-137"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b39b8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b39b8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b39b8-139"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b39b8-139"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b39b8-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b39b8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b39b8-141">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="b39b8-141">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="b39b8-142">**AddLStoTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="b39b8-142">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)
</dt> <dt>

[<span data-ttu-id="b39b8-143">**RemoveLSfromTSLSGroup**</span><span class="sxs-lookup"><span data-stu-id="b39b8-143">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)
</dt> </dl>

 


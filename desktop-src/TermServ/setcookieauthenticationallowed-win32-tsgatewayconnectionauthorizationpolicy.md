---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetCookieAuthenticationAllowed 方法
description: 設定 CookieAuthenticationAllowed 屬性。
ms.assetid: 481b89cb-d73b-4dae-941c-a629c2ae5ac4
ms.tgt_platform: multiple
keywords:
- SetCookieAuthenticationAllowed 方法遠端桌面服務
- SetCookieAuthenticationAllowed 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetCookieAuthenticationAllowed 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetCookieAuthenticationAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9293123ab6ce5b1ddcdb172f9258ba73b23fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094103"
---
# <a name="setcookieauthenticationallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="3c5e4-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetCookieAuthenticationAllowed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3c5e4-106">SetCookieAuthenticationAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="3c5e4-107">設定 **CookieAuthenticationAllowed** 屬性。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-107">Sets the **CookieAuthenticationAllowed** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c5e4-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c5e4-108">Syntax</span></span>


```mof
uint32 SetCookieAuthenticationAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="3c5e4-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c5e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c5e4-110">*允許* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c5e4-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c5e4-111">類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="3c5e4-111">Type: **boolean**</span></span>

<span data-ttu-id="3c5e4-112">新的屬性值。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-112">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c5e4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c5e4-113">Return value</span></span>

<span data-ttu-id="3c5e4-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="3c5e4-114">Type: **uint32**</span></span>

<span data-ttu-id="3c5e4-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3c5e4-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3c5e4-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3c5e4-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c5e4-118">Remarks</span></span>

<span data-ttu-id="3c5e4-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3c5e4-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c5e4-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c5e4-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c5e4-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="3c5e4-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c5e4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c5e4-124">Requirements</span></span>



| <span data-ttu-id="3c5e4-125">需求</span><span class="sxs-lookup"><span data-stu-id="3c5e4-125">Requirement</span></span> | <span data-ttu-id="3c5e4-126">值</span><span class="sxs-lookup"><span data-stu-id="3c5e4-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c5e4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c5e4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c5e4-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="3c5e4-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3c5e4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c5e4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c5e4-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3c5e4-130">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="3c5e4-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="3c5e4-131">Namespace</span></span><br/>                | <span data-ttu-id="3c5e4-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="3c5e4-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3c5e4-133">MOF</span><span class="sxs-lookup"><span data-stu-id="3c5e4-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c5e4-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c5e4-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c5e4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c5e4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c5e4-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c5e4-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3c5e4-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c5e4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c5e4-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="3c5e4-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


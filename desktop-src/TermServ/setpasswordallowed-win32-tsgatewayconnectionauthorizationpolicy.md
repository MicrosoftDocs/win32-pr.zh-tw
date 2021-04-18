---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetPasswordAllowed 方法
description: 設定 PasswordAllowed 屬性，此屬性可啟用或停用使用密碼連接到遠端桌面閘道 (RD 閘道) server 的支援。
ms.assetid: 2d2dfc45-ac2c-41dc-b2c1-4c8eab42c442
ms.tgt_platform: multiple
keywords:
- SetPasswordAllowed 方法遠端桌面服務
- SetPasswordAllowed 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetPasswordAllowed 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetPasswordAllowed
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8bda5fde2fd79cc02697fd270fc307ef5f410f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385166"
---
# <a name="setpasswordallowed-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="9060c-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetPasswordAllowed 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9060c-106">SetPasswordAllowed method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="9060c-107">設定 **PasswordAllowed** 屬性，此屬性可啟用或停用使用密碼連接到遠端桌面閘道 (RD 閘道) server 的支援。</span><span class="sxs-lookup"><span data-stu-id="9060c-107">Sets the **PasswordAllowed** property, which enables or disables support for using a password to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9060c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9060c-108">Syntax</span></span>


```mof
uint32 SetPasswordAllowed(
  [in] boolean Allowed
);
```



## <a name="parameters"></a><span data-ttu-id="9060c-109">參數</span><span class="sxs-lookup"><span data-stu-id="9060c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9060c-110">*允許* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9060c-110">*Allowed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9060c-111">新的 **PasswordAllowed** 值。</span><span class="sxs-lookup"><span data-stu-id="9060c-111">New **PasswordAllowed** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9060c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9060c-112">Return value</span></span>

<span data-ttu-id="9060c-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="9060c-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="9060c-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="9060c-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="9060c-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="9060c-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9060c-116">備註</span><span class="sxs-lookup"><span data-stu-id="9060c-116">Remarks</span></span>

<span data-ttu-id="9060c-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="9060c-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="9060c-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="9060c-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9060c-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="9060c-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9060c-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="9060c-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9060c-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="9060c-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9060c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="9060c-122">Requirements</span></span>



| <span data-ttu-id="9060c-123">需求</span><span class="sxs-lookup"><span data-stu-id="9060c-123">Requirement</span></span> | <span data-ttu-id="9060c-124">值</span><span class="sxs-lookup"><span data-stu-id="9060c-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9060c-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9060c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9060c-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="9060c-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="9060c-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9060c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9060c-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9060c-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="9060c-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="9060c-129">Namespace</span></span><br/>                | <span data-ttu-id="9060c-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="9060c-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="9060c-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9060c-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9060c-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="9060c-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="9060c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9060c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9060c-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9060c-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9060c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9060c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9060c-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="9060c-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


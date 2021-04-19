---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetUserGroupNames 方法
description: 將此遠端桌面連線授權原則的 UserGroupNames 屬性設定 (RD \ 160;端點) 。
ms.assetid: 03c9b2c5-8769-46f2-941f-302d798dd3a1
ms.tgt_platform: multiple
keywords:
- SetUserGroupNames 方法遠端桌面服務
- SetUserGroupNames 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetUserGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ca948b63cd106e7284b00c2c5f9e54c6dfa86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966343"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="e9568-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetUserGroupNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e9568-106">SetUserGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="e9568-107">將此遠端桌面連線授權原則的 **UserGroupNames** 屬性設定 (RD CAP) 。</span><span class="sxs-lookup"><span data-stu-id="e9568-107">Sets the **UserGroupNames** property for this Remote Desktop connection authorization policy (RD CAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9568-108">語法</span><span class="sxs-lookup"><span data-stu-id="e9568-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="e9568-109">參數</span><span class="sxs-lookup"><span data-stu-id="e9568-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9568-110">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e9568-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9568-111">分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="e9568-111">List of semicolon-separated user group names.</span></span> <span data-ttu-id="e9568-112">名稱的格式為 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="e9568-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="e9568-113">如果使用者隸屬于這些使用者群組中的任何一項，則會允許使用者存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="e9568-113">If the user belongs to any of these user groups, the user will be permitted access to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9568-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9568-114">Return value</span></span>

<span data-ttu-id="e9568-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="e9568-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e9568-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="e9568-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e9568-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="e9568-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9568-118">備註</span><span class="sxs-lookup"><span data-stu-id="e9568-118">Remarks</span></span>

<span data-ttu-id="e9568-119">如果 *UserGroupNames* 參數中有多個使用者組名，而且其中一個名稱無法處理，則不會處理任何名稱。</span><span class="sxs-lookup"><span data-stu-id="e9568-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="e9568-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="e9568-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="e9568-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e9568-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e9568-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e9568-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e9568-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e9568-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e9568-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e9568-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9568-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9568-125">Requirements</span></span>



| <span data-ttu-id="e9568-126">需求</span><span class="sxs-lookup"><span data-stu-id="e9568-126">Requirement</span></span> | <span data-ttu-id="e9568-127">值</span><span class="sxs-lookup"><span data-stu-id="e9568-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9568-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e9568-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9568-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="e9568-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e9568-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e9568-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9568-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9568-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="e9568-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="e9568-132">Namespace</span></span><br/>                | <span data-ttu-id="e9568-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e9568-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="e9568-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e9568-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9568-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9568-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9568-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e9568-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9568-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9568-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e9568-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9568-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9568-139">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="e9568-139">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


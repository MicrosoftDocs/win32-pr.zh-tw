---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 SetUserGroupNames 方法
description: 設定遠端桌面資源授權原則的 UserGroupNames 屬性 (RD \ 160;RAP) 。
ms.assetid: 91b77cd6-779e-460a-88a3-eda7a6fe99e5
ms.tgt_platform: multiple
keywords:
- SetUserGroupNames 方法遠端桌面服務
- SetUserGroupNames 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，SetUserGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.SetUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708d3eb3a6cc08cd94ba56979fc482a92a530646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104291"
---
# <a name="setusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="7083d-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 SetUserGroupNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7083d-106">SetUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="7083d-107">設定遠端桌面資源授權原則的 **UserGroupNames** 屬性 (RD RAP) 。</span><span class="sxs-lookup"><span data-stu-id="7083d-107">Sets the **UserGroupNames** property for the Remote Desktop resource authorization policy (RD RAP).</span></span>

## <a name="syntax"></a><span data-ttu-id="7083d-108">語法</span><span class="sxs-lookup"><span data-stu-id="7083d-108">Syntax</span></span>


```mof
uint32 SetUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="7083d-109">參數</span><span class="sxs-lookup"><span data-stu-id="7083d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7083d-110">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7083d-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7083d-111">以分號分隔的使用者組名清單。</span><span class="sxs-lookup"><span data-stu-id="7083d-111">Semicolon-separated list of user group names.</span></span> <span data-ttu-id="7083d-112">名稱的格式為 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="7083d-112">The names are of the format *Domain\\UserGroupName*.</span></span> <span data-ttu-id="7083d-113">如果使用者隸屬于這些使用者群組中的任何一項，則會允許存取。</span><span class="sxs-lookup"><span data-stu-id="7083d-113">If the user belongs to any of these user groups, access will be permitted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7083d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="7083d-114">Return value</span></span>

<span data-ttu-id="7083d-115">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="7083d-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7083d-116">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="7083d-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7083d-117">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="7083d-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7083d-118">備註</span><span class="sxs-lookup"><span data-stu-id="7083d-118">Remarks</span></span>

<span data-ttu-id="7083d-119">如果 *UserGroupNames* 參數中有多個使用者組名，而且其中一個名稱無法處理，則不會處理任何名稱。</span><span class="sxs-lookup"><span data-stu-id="7083d-119">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="7083d-120">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="7083d-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="7083d-121">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="7083d-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7083d-122">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="7083d-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="7083d-123">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="7083d-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7083d-124">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="7083d-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="7083d-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7083d-125">Requirements</span></span>



| <span data-ttu-id="7083d-126">需求</span><span class="sxs-lookup"><span data-stu-id="7083d-126">Requirement</span></span> | <span data-ttu-id="7083d-127">值</span><span class="sxs-lookup"><span data-stu-id="7083d-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7083d-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7083d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7083d-129">都不支援</span><span class="sxs-lookup"><span data-stu-id="7083d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7083d-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7083d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7083d-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7083d-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="7083d-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="7083d-132">Namespace</span></span><br/>                | <span data-ttu-id="7083d-133">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="7083d-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="7083d-134">MOF</span><span class="sxs-lookup"><span data-stu-id="7083d-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7083d-135"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="7083d-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="7083d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7083d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7083d-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7083d-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="7083d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7083d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7083d-139">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="7083d-139">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


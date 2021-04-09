---
title: Win32_TSGatewayResourceAuthorizationPolicy 類別的 AddUserGroupNames 方法
description: 將指定的使用者組名分號分隔清單，加入至 UserGroupNames 屬性中的現有使用者群組。
ms.assetid: 9cd18ecd-ad56-49c7-954a-2d67bbd7b1db
ms.tgt_platform: multiple
keywords:
- AddUserGroupNames 方法遠端桌面服務
- AddUserGroupNames 方法遠端桌面服務，Win32_TSGatewayResourceAuthorizationPolicy 類別
- Win32_TSGatewayResourceAuthorizationPolicy 類別遠端桌面服務，AddUserGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayResourceAuthorizationPolicy.AddUserGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c5c3fcb57c60ff2ca4c14d2e42ff0acdc84f0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934067"
---
# <a name="addusergroupnames-method-of-the-win32_tsgatewayresourceauthorizationpolicy-class"></a><span data-ttu-id="a36d8-106">Win32 TSGatewayResourceAuthorizationPolicy 類別的 AddUserGroupNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a36d8-106">AddUserGroupNames method of the Win32\_TSGatewayResourceAuthorizationPolicy class</span></span>

<span data-ttu-id="a36d8-107">將指定的使用者組名分號分隔清單，加入至 **UserGroupNames** 屬性中的現有使用者群組。</span><span class="sxs-lookup"><span data-stu-id="a36d8-107">Adds the specified semicolon-separated list of user group names to the existing user groups in the **UserGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a36d8-108">語法</span><span class="sxs-lookup"><span data-stu-id="a36d8-108">Syntax</span></span>


```mof
uint32 AddUserGroupNames(
  [in] string UserGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="a36d8-109">參數</span><span class="sxs-lookup"><span data-stu-id="a36d8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a36d8-110">*UserGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a36d8-110">*UserGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a36d8-111">要加入至 **UserGroupNames** 屬性的使用者組名清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="a36d8-111">Semicolon-separated list of user group names to add to the **UserGroupNames** property.</span></span> <span data-ttu-id="a36d8-112">使用者組名的格式應該是 *網域 \\ UserGroupName*。</span><span class="sxs-lookup"><span data-stu-id="a36d8-112">User group names should be of the format *Domain\\UserGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a36d8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a36d8-113">Return value</span></span>

<span data-ttu-id="a36d8-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="a36d8-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="a36d8-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="a36d8-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="a36d8-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="a36d8-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a36d8-117">備註</span><span class="sxs-lookup"><span data-stu-id="a36d8-117">Remarks</span></span>

<span data-ttu-id="a36d8-118">如果 *UserGroupNames* 參數中有多個使用者組名，而且其中一個名稱無法處理，則不會處理任何名稱。</span><span class="sxs-lookup"><span data-stu-id="a36d8-118">If multiple user group names are in the *UserGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="a36d8-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="a36d8-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="a36d8-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="a36d8-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a36d8-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="a36d8-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a36d8-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="a36d8-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a36d8-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="a36d8-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a36d8-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a36d8-124">Requirements</span></span>



| <span data-ttu-id="a36d8-125">需求</span><span class="sxs-lookup"><span data-stu-id="a36d8-125">Requirement</span></span> | <span data-ttu-id="a36d8-126">值</span><span class="sxs-lookup"><span data-stu-id="a36d8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36d8-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a36d8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a36d8-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="a36d8-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a36d8-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a36d8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a36d8-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a36d8-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a36d8-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="a36d8-131">Namespace</span></span><br/>                | <span data-ttu-id="a36d8-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="a36d8-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a36d8-133">MOF</span><span class="sxs-lookup"><span data-stu-id="a36d8-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a36d8-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="a36d8-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="a36d8-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a36d8-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a36d8-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a36d8-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="a36d8-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a36d8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a36d8-138">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="a36d8-138">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> </dl>

 


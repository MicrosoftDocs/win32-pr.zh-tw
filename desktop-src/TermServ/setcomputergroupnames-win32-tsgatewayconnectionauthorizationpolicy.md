---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 SetComputerGroupNames 方法
description: 設定 ComputerGroupNames 屬性。
ms.assetid: dd6747df-140f-4eeb-857b-d14f8713586c
ms.tgt_platform: multiple
keywords:
- SetComputerGroupNames 方法遠端桌面服務
- SetComputerGroupNames 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，SetComputerGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.SetComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a99c29ce37aeb8bfad0ae77197c7364b0135fa99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384565"
---
# <a name="setcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="6bb62-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 SetComputerGroupNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6bb62-106">SetComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="6bb62-107">設定 **ComputerGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb62-107">Sets the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb62-108">語法</span><span class="sxs-lookup"><span data-stu-id="6bb62-108">Syntax</span></span>


```mof
uint32 SetComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="6bb62-109">參數</span><span class="sxs-lookup"><span data-stu-id="6bb62-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb62-110">*ComputerGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6bb62-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6bb62-111">分號分隔的電腦群組名清單。</span><span class="sxs-lookup"><span data-stu-id="6bb62-111">List of semicolon-separated computer group names.</span></span> <span data-ttu-id="6bb62-112">這個值可以是空的。</span><span class="sxs-lookup"><span data-stu-id="6bb62-112">This value can be empty.</span></span> <span data-ttu-id="6bb62-113">名稱的格式為 *網域 \\ ComputerGroupName*。</span><span class="sxs-lookup"><span data-stu-id="6bb62-113">The names are of the format *Domain\\ComputerGroupName*.</span></span> <span data-ttu-id="6bb62-114">如果指定了值，用戶端電腦必須屬於其中一個電腦群組，使用者才能存取 RD 閘道 server。</span><span class="sxs-lookup"><span data-stu-id="6bb62-114">If a value is specified, the client computer must belong to one of these computer groups for the user to access the RD Gateway server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb62-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bb62-115">Return value</span></span>

<span data-ttu-id="6bb62-116">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6bb62-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="6bb62-117">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="6bb62-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="6bb62-118">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="6bb62-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb62-119">備註</span><span class="sxs-lookup"><span data-stu-id="6bb62-119">Remarks</span></span>

<span data-ttu-id="6bb62-120">如果 *ComputerGroupNames* 參數中有多個電腦群組名，而且其中一個名稱無法處理，則不會處理任何名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb62-120">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="6bb62-121">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="6bb62-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="6bb62-122">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="6bb62-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6bb62-123">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="6bb62-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6bb62-124">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="6bb62-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6bb62-125">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="6bb62-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb62-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb62-126">Requirements</span></span>



| <span data-ttu-id="6bb62-127">需求</span><span class="sxs-lookup"><span data-stu-id="6bb62-127">Requirement</span></span> | <span data-ttu-id="6bb62-128">值</span><span class="sxs-lookup"><span data-stu-id="6bb62-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb62-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bb62-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6bb62-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="6bb62-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6bb62-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bb62-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6bb62-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6bb62-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6bb62-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="6bb62-133">Namespace</span></span><br/>                | <span data-ttu-id="6bb62-134">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="6bb62-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="6bb62-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6bb62-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6bb62-136"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="6bb62-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="6bb62-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb62-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bb62-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb62-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="6bb62-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6bb62-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb62-140">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="6bb62-140">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


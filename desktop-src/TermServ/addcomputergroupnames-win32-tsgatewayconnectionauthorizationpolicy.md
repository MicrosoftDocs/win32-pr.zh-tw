---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 AddComputerGroupNames 方法
description: 將指定的電腦群組名加入至 ComputerGroupNames 屬性。
ms.assetid: f0c440d6-0cc2-48b4-b656-65f12e652151
ms.tgt_platform: multiple
keywords:
- AddComputerGroupNames 方法遠端桌面服務
- AddComputerGroupNames 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，AddComputerGroupNames 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.AddComputerGroupNames
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72647ef66b9e2eeaed824b3e77c404214786b615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104340"
---
# <a name="addcomputergroupnames-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="70da7-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 AddComputerGroupNames 方法 \_</span><span class="sxs-lookup"><span data-stu-id="70da7-106">AddComputerGroupNames method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="70da7-107">將指定的電腦群組名加入至 **ComputerGroupNames** 屬性。</span><span class="sxs-lookup"><span data-stu-id="70da7-107">Adds the specified computer group names to the **ComputerGroupNames** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="70da7-108">語法</span><span class="sxs-lookup"><span data-stu-id="70da7-108">Syntax</span></span>


```mof
uint32 AddComputerGroupNames(
  [in] string ComputerGroupNames
);
```



## <a name="parameters"></a><span data-ttu-id="70da7-109">參數</span><span class="sxs-lookup"><span data-stu-id="70da7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70da7-110">*ComputerGroupNames* \[在\]</span><span class="sxs-lookup"><span data-stu-id="70da7-110">*ComputerGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70da7-111">要加入至 **ComputerGroupNames** 屬性的電腦群組名清單（以分號分隔）。</span><span class="sxs-lookup"><span data-stu-id="70da7-111">Semicolon-separated list of computer group names to add to the **ComputerGroupNames** property.</span></span> <span data-ttu-id="70da7-112">電腦群組名的格式應為 *網域 \\ ComputerGroupName*。</span><span class="sxs-lookup"><span data-stu-id="70da7-112">Computer group names should be of the format *Domain\\ComputerGroupName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70da7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="70da7-113">Return value</span></span>

<span data-ttu-id="70da7-114">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="70da7-114">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="70da7-115">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="70da7-115">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="70da7-116">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="70da7-116">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="70da7-117">備註</span><span class="sxs-lookup"><span data-stu-id="70da7-117">Remarks</span></span>

<span data-ttu-id="70da7-118">如果 *ComputerGroupNames* 參數中有多個電腦群組名，而且其中一個名稱無法處理，則不會處理任何名稱。</span><span class="sxs-lookup"><span data-stu-id="70da7-118">If multiple computer group names are in the *ComputerGroupNames* parameter and one of the names cannot be processed, none of the names will be processed.</span></span>

<span data-ttu-id="70da7-119">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="70da7-119">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="70da7-120">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="70da7-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="70da7-121">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="70da7-121">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="70da7-122">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="70da7-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="70da7-123">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="70da7-123">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="70da7-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="70da7-124">Requirements</span></span>



| <span data-ttu-id="70da7-125">需求</span><span class="sxs-lookup"><span data-stu-id="70da7-125">Requirement</span></span> | <span data-ttu-id="70da7-126">值</span><span class="sxs-lookup"><span data-stu-id="70da7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="70da7-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="70da7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="70da7-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="70da7-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="70da7-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="70da7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="70da7-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70da7-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="70da7-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="70da7-131">Namespace</span></span><br/>                | <span data-ttu-id="70da7-132">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="70da7-132">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="70da7-133">MOF</span><span class="sxs-lookup"><span data-stu-id="70da7-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="70da7-134"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="70da7-134"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="70da7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="70da7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70da7-136"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70da7-136"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="70da7-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70da7-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70da7-138">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="70da7-138">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


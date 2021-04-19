---
title: Win32_TSGatewayConnectionAuthorizationPolicy 類別的 MoveDown 方法
description: 將目前的遠端桌面連線授權原則移動 (RD \ 160;以 RD \ 160 的順序向下) 一個位置的上限評估端點。
ms.assetid: 57349e59-e200-4789-bbcb-d474eacde39d
ms.tgt_platform: multiple
keywords:
- MoveDown 方法遠端桌面服務
- MoveDown 方法遠端桌面服務，Win32_TSGatewayConnectionAuthorizationPolicy 類別
- Win32_TSGatewayConnectionAuthorizationPolicy 類別遠端桌面服務，MoveDown 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnectionAuthorizationPolicy.MoveDown
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92e5b2e2b56a60d78f827f8989c0317cb003e511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970457"
---
# <a name="movedown-method-of-the-win32_tsgatewayconnectionauthorizationpolicy-class"></a><span data-ttu-id="0bcb9-106">Win32 TSGatewayConnectionAuthorizationPolicy 類別的 MoveDown 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0bcb9-106">MoveDown method of the Win32\_TSGatewayConnectionAuthorizationPolicy class</span></span>

<span data-ttu-id="0bcb9-107">將目前的遠端桌面連線授權原則 (RD CAP) 評估 RD Cap 的順序下一個位置。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-107">Moves the current Remote Desktop connection authorization policy (RD CAP) one position down in the order that RD CAPs are evaluated.</span></span> <span data-ttu-id="0bcb9-108">這個方法會遞增目前 RD CAP 的 **order** 屬性，並遞減遵循目前 RD CAP 之 RD CAP 的 **order** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-108">This method increments the **Order** property of the current RD CAP and decrements the **Order** property of the RD CAP that followed the current RD CAP.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bcb9-109">語法</span><span class="sxs-lookup"><span data-stu-id="0bcb9-109">Syntax</span></span>


```mof
uint32 MoveDown();
```



## <a name="parameters"></a><span data-ttu-id="0bcb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="0bcb9-110">Parameters</span></span>

<span data-ttu-id="0bcb9-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0bcb9-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0bcb9-112">Return value</span></span>

<span data-ttu-id="0bcb9-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0bcb9-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0bcb9-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0bcb9-116">備註</span><span class="sxs-lookup"><span data-stu-id="0bcb9-116">Remarks</span></span>

<span data-ttu-id="0bcb9-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0bcb9-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0bcb9-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0bcb9-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0bcb9-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0bcb9-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0bcb9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0bcb9-122">Requirements</span></span>



| <span data-ttu-id="0bcb9-123">需求</span><span class="sxs-lookup"><span data-stu-id="0bcb9-123">Requirement</span></span> | <span data-ttu-id="0bcb9-124">值</span><span class="sxs-lookup"><span data-stu-id="0bcb9-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bcb9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0bcb9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0bcb9-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="0bcb9-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0bcb9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0bcb9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0bcb9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0bcb9-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0bcb9-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="0bcb9-129">Namespace</span></span><br/>                | <span data-ttu-id="0bcb9-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0bcb9-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0bcb9-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0bcb9-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bcb9-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bcb9-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bcb9-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0bcb9-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bcb9-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bcb9-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0bcb9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0bcb9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bcb9-136">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="0bcb9-136">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="0bcb9-137">**上移**</span><span class="sxs-lookup"><span data-stu-id="0bcb9-137">**MoveUp**</span></span>](moveup-win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> </dl>

 


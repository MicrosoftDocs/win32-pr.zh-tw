---
title: Win32_TSGatewayLoadBalancer 類別的 IsLoadBalancingServer 方法
description: 判斷遠端桌面閘道 (RD 閘道) server 是否可以執行負載平衡。
ms.assetid: ae1a91c1-0b8b-4bd0-83f9-41c973247f27
ms.tgt_platform: multiple
keywords:
- IsLoadBalancingServer 方法遠端桌面服務
- IsLoadBalancingServer 方法遠端桌面服務，Win32_TSGatewayLoadBalancer 類別
- Win32_TSGatewayLoadBalancer 類別遠端桌面服務，IsLoadBalancingServer 方法
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer.IsLoadBalancingServer
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eae909df4074c8129a1b49eb0d5c3b336fed5d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965502"
---
# <a name="isloadbalancingserver-method-of-the-win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="0f1e6-106">Win32 TSGatewayLoadBalancer 類別的 IsLoadBalancingServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0f1e6-106">IsLoadBalancingServer method of the Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="0f1e6-107">判斷遠端桌面閘道 (RD 閘道) server 是否可以執行負載平衡。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-107">Determines whether the Remote Desktop Gateway (RD Gateway) server can perform load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f1e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="0f1e6-108">Syntax</span></span>


```mof
uint32 IsLoadBalancingServer(
  [out] boolean LoadBalancing
);
```



## <a name="parameters"></a><span data-ttu-id="0f1e6-109">參數</span><span class="sxs-lookup"><span data-stu-id="0f1e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f1e6-110">*負載平衡* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0f1e6-110">*LoadBalancing* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f1e6-111">如果伺服器可以執行負載平衡，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-111">**TRUE** if the server can perform load balancing, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f1e6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f1e6-112">Return value</span></span>

<span data-ttu-id="0f1e6-113">如果方法成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="0f1e6-114">如果方法失敗，則會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="0f1e6-115">如需錯誤碼清單，請參閱 [遠端桌面服務 WMI 提供者錯誤碼](terminal-services-wmi-provider-error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f1e6-116">備註</span><span class="sxs-lookup"><span data-stu-id="0f1e6-116">Remarks</span></span>

<span data-ttu-id="0f1e6-117">您必須是 Administrators 群組的成員，才能呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="0f1e6-118">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0f1e6-119">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0f1e6-120">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0f1e6-121">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="0f1e6-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f1e6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f1e6-122">Requirements</span></span>



| <span data-ttu-id="0f1e6-123">需求</span><span class="sxs-lookup"><span data-stu-id="0f1e6-123">Requirement</span></span> | <span data-ttu-id="0f1e6-124">值</span><span class="sxs-lookup"><span data-stu-id="0f1e6-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f1e6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f1e6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0f1e6-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="0f1e6-126">None supported</span></span><br/>                                                                |
| <span data-ttu-id="0f1e6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f1e6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0f1e6-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f1e6-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0f1e6-129">命名空間</span><span class="sxs-lookup"><span data-stu-id="0f1e6-129">Namespace</span></span><br/>                | <span data-ttu-id="0f1e6-130">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="0f1e6-130">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="0f1e6-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0f1e6-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f1e6-132"><dt>TSGateway mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f1e6-132"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f1e6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0f1e6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f1e6-134"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f1e6-134"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0f1e6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f1e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f1e6-136">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="0f1e6-136">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> </dl>

 


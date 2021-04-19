---
title: Win32_TSSessionDirectory 類別的 SetLoadBalancingState 方法
description: 設定值，指出伺服器是否將參與遠端桌面連線代理人 (RD 連線代理人) 負載平衡。
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- SetLoadBalancingState 方法遠端桌面服務
- SetLoadBalancingState 方法遠端桌面服務，Win32_TSSessionDirectory 類別
- Win32_TSSessionDirectory 類別遠端桌面服務，SetLoadBalancingState 方法
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969152"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e5a16-106">Win32 TSSessionDirectory 類別的 SetLoadBalancingState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e5a16-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e5a16-107">設定值，指出伺服器是否將參與遠端桌面連線代理人 (RD 連線代理人) 負載平衡。</span><span class="sxs-lookup"><span data-stu-id="e5a16-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a16-108">語法</span><span class="sxs-lookup"><span data-stu-id="e5a16-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="e5a16-109">參數</span><span class="sxs-lookup"><span data-stu-id="e5a16-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5a16-110">*StateValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5a16-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5a16-111">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="e5a16-111">Type: **uint32**</span></span>

<span data-ttu-id="e5a16-112">指出伺服器是否將參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="e5a16-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="e5a16-113">0</span><span class="sxs-lookup"><span data-stu-id="e5a16-113">0</span></span>
</dt> <dd>

<span data-ttu-id="e5a16-114">伺服器將不會參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="e5a16-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="e5a16-115">1</span><span class="sxs-lookup"><span data-stu-id="e5a16-115">1</span></span>
</dt> <dd>

<span data-ttu-id="e5a16-116">伺服器將參與 RD 連線代理人負載平衡。</span><span class="sxs-lookup"><span data-stu-id="e5a16-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e5a16-117">備註</span><span class="sxs-lookup"><span data-stu-id="e5a16-117">Remarks</span></span>

<span data-ttu-id="e5a16-118">伺服器必須加入 RD 連線代理人中的伺服器陣列。</span><span class="sxs-lookup"><span data-stu-id="e5a16-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="e5a16-119">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="e5a16-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e5a16-120">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="e5a16-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e5a16-121">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="e5a16-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e5a16-122">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="e5a16-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5a16-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5a16-123">Requirements</span></span>



| <span data-ttu-id="e5a16-124">需求</span><span class="sxs-lookup"><span data-stu-id="e5a16-124">Requirement</span></span> | <span data-ttu-id="e5a16-125">值</span><span class="sxs-lookup"><span data-stu-id="e5a16-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a16-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5a16-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e5a16-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="e5a16-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e5a16-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5a16-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e5a16-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e5a16-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e5a16-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5a16-130">Namespace</span></span><br/>                | <span data-ttu-id="e5a16-131">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="e5a16-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e5a16-132">MOF</span><span class="sxs-lookup"><span data-stu-id="e5a16-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5a16-133"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="e5a16-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5a16-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e5a16-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5a16-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a16-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a16-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5a16-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a16-137">**Win32 \_ TSSessionDirectory**</span><span class="sxs-lookup"><span data-stu-id="e5a16-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 


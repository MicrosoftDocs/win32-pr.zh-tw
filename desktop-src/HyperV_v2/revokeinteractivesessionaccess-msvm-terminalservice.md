---
description: 從指定的受信者清單撤銷虛擬機器的互動式會話存取權。
ms.assetid: c6d3df04-c31e-404a-9a04-3e8653bdc14f
title: Msvm_TerminalService 類別的 RevokeInteractiveSessionAccess 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.RevokeInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab92f375f082d3af1f04b3fe52db5cb7964e3d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692975"
---
# <a name="revokeinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="bfbd6-103">Msvm TerminalService 類別的 RevokeInteractiveSessionAccess 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bfbd6-103">RevokeInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="bfbd6-104">從指定的受信者清單撤銷虛擬機器的互動式會話存取權。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-104">Revokes access to the interactive session of the virtual machine from the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfbd6-105">語法</span><span class="sxs-lookup"><span data-stu-id="bfbd6-105">Syntax</span></span>


```mof
uint32 RevokeInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bfbd6-106">參數</span><span class="sxs-lookup"><span data-stu-id="bfbd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfbd6-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfbd6-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfbd6-108">[**CIM \_**](cim-computersystem.md)系統類型實例的參考，代表將撤銷存取權的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-108">A reference to an instance of the [**CIM\_ComputerSystem**](cim-computersystem.md) class that represents the virtual machine to which access will be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd6-109">信任者 \[在\]</span><span class="sxs-lookup"><span data-stu-id="bfbd6-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfbd6-110">字串的陣列，每個字串都會識別要撤銷其存取權限的信任者。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-110">An array of strings, each identifying a trustee whose access rights will be revoked.</span></span> <span data-ttu-id="bfbd6-111">受信任的識別碼應以 Windows SAM 相容格式或 Windows SID 字串格式指定。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="bfbd6-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bfbd6-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bfbd6-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfbd6-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bfbd6-114">Return value</span></span>

<span data-ttu-id="bfbd6-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bfbd6-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bfbd6-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="bfbd6-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="bfbd6-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="bfbd6-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bfbd6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="bfbd6-127">Requirements</span></span>



| <span data-ttu-id="bfbd6-128">需求</span><span class="sxs-lookup"><span data-stu-id="bfbd6-128">Requirement</span></span> | <span data-ttu-id="bfbd6-129">值</span><span class="sxs-lookup"><span data-stu-id="bfbd6-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfbd6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bfbd6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bfbd6-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfbd6-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bfbd6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bfbd6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bfbd6-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bfbd6-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfbd6-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="bfbd6-134">Namespace</span></span><br/>                | <span data-ttu-id="bfbd6-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bfbd6-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bfbd6-136">MOF</span><span class="sxs-lookup"><span data-stu-id="bfbd6-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfbd6-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bfbd6-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfbd6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="bfbd6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfbd6-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bfbd6-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bfbd6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bfbd6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfbd6-141">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="bfbd6-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 


---
description: 將虛擬機器的互動式會話存取權授與指定的受信者清單。
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Msvm_TerminalService 類別的 GrantInteractiveSessionAccess 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8bd49805b5fdc5545a81e4f0b816fe35a6c37b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981523"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="541bd-103">Msvm TerminalService 類別的 GrantInteractiveSessionAccess 方法 \_</span><span class="sxs-lookup"><span data-stu-id="541bd-103">GrantInteractiveSessionAccess method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="541bd-104">將虛擬機器的互動式會話存取權授與指定的受信者清單。</span><span class="sxs-lookup"><span data-stu-id="541bd-104">Grants access to the interactive session of the virtual machine to the specified list of trustees.</span></span>

## <a name="syntax"></a><span data-ttu-id="541bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="541bd-105">Syntax</span></span>


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="541bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="541bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="541bd-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="541bd-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541bd-108">[**Msvm \_**](msvm-computersystem.md)實例類別的實例參考，代表將授與存取權的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="541bd-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to which access will be granted.</span></span>

</dd> <dt>

<span data-ttu-id="541bd-109">信任者 \[在\]</span><span class="sxs-lookup"><span data-stu-id="541bd-109">*Trustees* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="541bd-110">字串的陣列，每個都識別將被授與虛擬機器互動式會話存取權的信任者。</span><span class="sxs-lookup"><span data-stu-id="541bd-110">An array of strings, each identifying a trustee that will be granted access to the interactive session of the virtual machine.</span></span> <span data-ttu-id="541bd-111">受信任的識別碼應以 Windows SAM 相容格式或 Windows SID 字串格式指定。</span><span class="sxs-lookup"><span data-stu-id="541bd-111">The trustee identifiers should be specified in Windows SAM-compatible format or Windows SID string format.</span></span>

</dd> <dt>

<span data-ttu-id="541bd-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="541bd-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="541bd-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="541bd-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="541bd-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="541bd-114">Return value</span></span>

<span data-ttu-id="541bd-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="541bd-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="541bd-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="541bd-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-117">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="541bd-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-118">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="541bd-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-119">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="541bd-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-120">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="541bd-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-121">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="541bd-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-122"> (6) 的 **參數不相容**</span><span class="sxs-lookup"><span data-stu-id="541bd-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="541bd-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="541bd-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="541bd-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="541bd-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="541bd-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="541bd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="541bd-127">Requirements</span></span>



| <span data-ttu-id="541bd-128">需求</span><span class="sxs-lookup"><span data-stu-id="541bd-128">Requirement</span></span> | <span data-ttu-id="541bd-129">值</span><span class="sxs-lookup"><span data-stu-id="541bd-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="541bd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="541bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="541bd-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="541bd-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="541bd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="541bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="541bd-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="541bd-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="541bd-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="541bd-134">Namespace</span></span><br/>                | <span data-ttu-id="541bd-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="541bd-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="541bd-136">MOF</span><span class="sxs-lookup"><span data-stu-id="541bd-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="541bd-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="541bd-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="541bd-138">DLL</span><span class="sxs-lookup"><span data-stu-id="541bd-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="541bd-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="541bd-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="541bd-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="541bd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="541bd-141">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="541bd-141">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 


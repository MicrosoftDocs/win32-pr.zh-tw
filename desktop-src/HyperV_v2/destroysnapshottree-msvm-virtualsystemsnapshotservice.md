---
description: 移除虛擬機器的現有快照集及其所有子系。
ms.assetid: d7a6442a-41a5-4e82-8ec8-dbc8e14d9a89
title: Msvm_VirtualSystemSnapshotService 類別的 DestroySnapshotTree 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.DestroySnapshotTree
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e5658e954766531765c47f8bef80d5509f2ad27c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998137"
---
# <a name="destroysnapshottree-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="f701b-103">Msvm VirtualSystemSnapshotService 類別的 DestroySnapshotTree 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f701b-103">DestroySnapshotTree method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="f701b-104">移除虛擬機器的現有快照集及其所有子系。</span><span class="sxs-lookup"><span data-stu-id="f701b-104">Removes an existing snapshot, and all its children, of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="f701b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f701b-105">Syntax</span></span>


```mof
uint32 DestroySnapshotTree(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f701b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f701b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f701b-107">*SnapshotSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f701b-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f701b-108">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))參考，代表要終結的虛擬機器快照集樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="f701b-108">A [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) reference that represents the virtual machine snapshot tree to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="f701b-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f701b-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f701b-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="f701b-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f701b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f701b-111">Return value</span></span>

<span data-ttu-id="f701b-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f701b-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f701b-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f701b-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f701b-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f701b-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f701b-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f701b-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f701b-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f701b-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f701b-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="f701b-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f701b-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f701b-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f701b-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f701b-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f701b-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f701b-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f701b-126">Requirements</span></span>



| <span data-ttu-id="f701b-127">需求</span><span class="sxs-lookup"><span data-stu-id="f701b-127">Requirement</span></span> | <span data-ttu-id="f701b-128">值</span><span class="sxs-lookup"><span data-stu-id="f701b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f701b-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f701b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f701b-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f701b-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f701b-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f701b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f701b-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f701b-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f701b-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="f701b-133">Namespace</span></span><br/>                | <span data-ttu-id="f701b-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="f701b-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f701b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f701b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f701b-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f701b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f701b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f701b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f701b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f701b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f701b-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f701b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f701b-140">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="f701b-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="f701b-141">**RemoveVirtualSystemSnapshotTree (V1)**</span><span class="sxs-lookup"><span data-stu-id="f701b-141">**RemoveVirtualSystemSnapshotTree (V1)**</span></span>](/previous-versions/windows/desktop/virtual/removevirtualsystemsnapshottree-msvm-virtualsystemmanagementservice)
</dt> </dl>

 


---
description: 清除現有快照集的儲存狀態。
ms.assetid: abb0ed4a-7f89-4d32-93d2-7491d2f2aa83
title: Msvm_VirtualSystemSnapshotService 類別的 ClearSnapshotState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ClearSnapshotState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a218b600e45d91d8c744d6b49afe97666ddb51ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971850"
---
# <a name="clearsnapshotstate-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="6905e-103">Msvm VirtualSystemSnapshotService 類別的 ClearSnapshotState 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6905e-103">ClearSnapshotState method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="6905e-104">清除現有快照集的儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="6905e-104">Clears save state from an existing snapshot.</span></span>

## <a name="syntax"></a><span data-ttu-id="6905e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6905e-105">Syntax</span></span>


```mof
uint32 ClearSnapshotState(
  [in]  CIM_VirtualSystemSettingData REF SnapshotSettingData,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6905e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6905e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6905e-107">*SnapshotSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6905e-107">*SnapshotSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6905e-108">[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))實例的參考，代表要清除其狀態的快照集。</span><span class="sxs-lookup"><span data-stu-id="6905e-108">A reference to the [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instance that represents the snapshot whose state is to be cleared.</span></span>

</dd> <dt>

<span data-ttu-id="6905e-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6905e-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6905e-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="6905e-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6905e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6905e-111">Return value</span></span>

<span data-ttu-id="6905e-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6905e-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6905e-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6905e-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="6905e-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="6905e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="6905e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="6905e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="6905e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="6905e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="6905e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="6905e-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="6905e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="6905e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="6905e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6905e-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="6905e-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6905e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6905e-126">Requirements</span></span>



| <span data-ttu-id="6905e-127">需求</span><span class="sxs-lookup"><span data-stu-id="6905e-127">Requirement</span></span> | <span data-ttu-id="6905e-128">值</span><span class="sxs-lookup"><span data-stu-id="6905e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6905e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6905e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6905e-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6905e-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6905e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6905e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6905e-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6905e-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6905e-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="6905e-133">Namespace</span></span><br/>                | <span data-ttu-id="6905e-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6905e-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6905e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6905e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6905e-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6905e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6905e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6905e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6905e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6905e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6905e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6905e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6905e-140">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="6905e-140">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 


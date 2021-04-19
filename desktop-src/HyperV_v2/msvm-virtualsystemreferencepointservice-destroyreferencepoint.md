---
description: 刪除指定的參考點。
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Msvm_VirtualSystemReferencePointService 類別的 DestroyReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cf7a21e60369a928cc1d617e24db5f5fc70c522
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106997599"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="101c8-103">Msvm VirtualSystemReferencePointService 類別的 DestroyReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="101c8-103">DestroyReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="101c8-104">刪除指定的參考點。</span><span class="sxs-lookup"><span data-stu-id="101c8-104">Deletes the specified reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="101c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="101c8-105">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="101c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="101c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="101c8-107">*AffectedReferencePoint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="101c8-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="101c8-108">[**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)實例的參考，代表要移除的參考點。</span><span class="sxs-lookup"><span data-stu-id="101c8-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="101c8-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="101c8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="101c8-110">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="101c8-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="101c8-111">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="101c8-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="101c8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="101c8-112">Return value</span></span>

<span data-ttu-id="101c8-113">成功時，會傳回 0 (完成，沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="101c8-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="101c8-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="101c8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="101c8-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="101c8-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="101c8-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="101c8-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="101c8-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="101c8-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="101c8-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="101c8-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="101c8-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="101c8-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="101c8-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="101c8-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="101c8-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="101c8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="101c8-127">Requirements</span></span>



| <span data-ttu-id="101c8-128">需求</span><span class="sxs-lookup"><span data-stu-id="101c8-128">Requirement</span></span> | <span data-ttu-id="101c8-129">值</span><span class="sxs-lookup"><span data-stu-id="101c8-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="101c8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="101c8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="101c8-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="101c8-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="101c8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="101c8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="101c8-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="101c8-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="101c8-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="101c8-134">Namespace</span></span><br/>                | <span data-ttu-id="101c8-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="101c8-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="101c8-136">MOF</span><span class="sxs-lookup"><span data-stu-id="101c8-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="101c8-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="101c8-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="101c8-138">DLL</span><span class="sxs-lookup"><span data-stu-id="101c8-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="101c8-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="101c8-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="101c8-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="101c8-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="101c8-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="101c8-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 





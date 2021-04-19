---
description: 終結虛擬系統。
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: CIM_VirtualSystemManagementService 類別的 DestroySystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983577"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="6aeac-103">CIM VirtualSystemManagementService 類別的 DestroySystem 方法 \_</span><span class="sxs-lookup"><span data-stu-id="6aeac-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6aeac-104">終結虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="6aeac-104">Destroys a virtual system.</span></span>

<span data-ttu-id="6aeac-105">受參考的虛擬系統已終結，包括其範圍內的任何元素。</span><span class="sxs-lookup"><span data-stu-id="6aeac-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="6aeac-106">虛擬資源會傳回到其資源集區，這可能表示將這些資源的終結 (實) 的相依。</span><span class="sxs-lookup"><span data-stu-id="6aeac-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="6aeac-107">如果虛擬系統在叫用作業時處於作用中狀態，則會先將它停用，然後再損毀。</span><span class="sxs-lookup"><span data-stu-id="6aeac-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="6aeac-108">如果快照集是從虛擬系統建立的，也會損毀。</span><span class="sxs-lookup"><span data-stu-id="6aeac-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="6aeac-109">語法</span><span class="sxs-lookup"><span data-stu-id="6aeac-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6aeac-110">參數</span><span class="sxs-lookup"><span data-stu-id="6aeac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6aeac-111">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6aeac-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6aeac-112">參考 CIM 的類別實例， [**代表 \_**](cim-computersystem.md) 要終結的虛擬電腦系統。</span><span class="sxs-lookup"><span data-stu-id="6aeac-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="6aeac-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6aeac-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6aeac-114">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="6aeac-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6aeac-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6aeac-115">Return value</span></span>

<span data-ttu-id="6aeac-116">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="6aeac-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6aeac-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6aeac-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-118">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="6aeac-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-119">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="6aeac-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-120">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="6aeac-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-121">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="6aeac-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-122">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="6aeac-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-123">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="6aeac-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="6aeac-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-125">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="6aeac-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6aeac-126">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="6aeac-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6aeac-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="6aeac-127">Requirements</span></span>



| <span data-ttu-id="6aeac-128">需求</span><span class="sxs-lookup"><span data-stu-id="6aeac-128">Requirement</span></span> | <span data-ttu-id="6aeac-129">值</span><span class="sxs-lookup"><span data-stu-id="6aeac-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6aeac-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6aeac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6aeac-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="6aeac-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="6aeac-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6aeac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6aeac-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6aeac-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="6aeac-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="6aeac-134">Namespace</span></span><br/>                | <span data-ttu-id="6aeac-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="6aeac-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6aeac-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6aeac-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6aeac-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6aeac-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6aeac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6aeac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6aeac-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6aeac-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6aeac-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6aeac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6aeac-141">**CIM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6aeac-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 





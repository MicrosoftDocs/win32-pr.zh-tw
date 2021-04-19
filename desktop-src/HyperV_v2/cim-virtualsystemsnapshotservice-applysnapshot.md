---
description: 將虛擬系統快照集套用至其建立來源的虛擬系統。
ms.assetid: acd90ce0-7f82-48d9-9d23-903ba6815779
title: CIM_VirtualSystemSnapshotService 類別的 ApplySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 252f7d7d9a57b439ac00fa663fa0a0e816ebada0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985475"
---
# <a name="applysnapshot-method-of-the-cim_virtualsystemsnapshotservice-class"></a><span data-ttu-id="f992f-103">CIM VirtualSystemSnapshotService 類別的 ApplySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f992f-103">ApplySnapshot method of the CIM\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="f992f-104">將虛擬系統快照集套用至其建立來源的虛擬系統。</span><span class="sxs-lookup"><span data-stu-id="f992f-104">Applies a virtual system snapshot to the virtual system that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="f992f-105">語法</span><span class="sxs-lookup"><span data-stu-id="f992f-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f992f-106">參數</span><span class="sxs-lookup"><span data-stu-id="f992f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f992f-107">*快照* \[ 集在\]</span><span class="sxs-lookup"><span data-stu-id="f992f-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f992f-108">虛擬系統快照集的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。</span><span class="sxs-lookup"><span data-stu-id="f992f-108">A [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) reference to the virtual system snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="f992f-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f992f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f992f-110">如果作業的執行時間很長，則可以選擇性地傳回代表作業的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 。</span><span class="sxs-lookup"><span data-stu-id="f992f-110">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

> [!Note]  
> <span data-ttu-id="f992f-111">此參數在 Windows 8.1 中是讀取/寫入。</span><span class="sxs-lookup"><span data-stu-id="f992f-111">This parameter was read/write in Windows 8.1.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f992f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f992f-112">Return value</span></span>

<span data-ttu-id="f992f-113">成功時傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="f992f-113">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f992f-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f992f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="f992f-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="f992f-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="f992f-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="f992f-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="f992f-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-120">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="f992f-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="f992f-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="f992f-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="f992f-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="f992f-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="f992f-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f992f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="f992f-125">Requirements</span></span>



| <span data-ttu-id="f992f-126">需求</span><span class="sxs-lookup"><span data-stu-id="f992f-126">Requirement</span></span> | <span data-ttu-id="f992f-127">值</span><span class="sxs-lookup"><span data-stu-id="f992f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f992f-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f992f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f992f-129">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f992f-129">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f992f-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f992f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f992f-131">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f992f-131">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f992f-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="f992f-132">Namespace</span></span><br/>                | <span data-ttu-id="f992f-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f992f-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f992f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f992f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f992f-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f992f-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f992f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f992f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f992f-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f992f-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f992f-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f992f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f992f-139">**CIM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="f992f-139">**CIM\_VirtualSystemSnapshotService**</span></span>](cim-virtualsystemsnapshotservice.md)
</dt> </dl>

 

 





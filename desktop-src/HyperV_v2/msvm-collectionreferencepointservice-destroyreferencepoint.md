---
description: 終結現有的參考點集合。 這個方法可能會損毀其他相依于受影響之參考點集合的參考點。
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Msvm_CollectionReferencePointService 類別的 DestroyReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d7fb3fd9168778854518022744f1a0c5ba3c5f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115900"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="80e9f-104">Msvm CollectionReferencePointService 類別的 DestroyReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="80e9f-104">DestroyReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="80e9f-105">終結現有的參考點集合。</span><span class="sxs-lookup"><span data-stu-id="80e9f-105">Destroys an existing reference point collection.</span></span> <span data-ttu-id="80e9f-106">這個方法可能會損毀其他相依于受影響之參考點集合的參考點。</span><span class="sxs-lookup"><span data-stu-id="80e9f-106">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="80e9f-107">語法</span><span class="sxs-lookup"><span data-stu-id="80e9f-107">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="80e9f-108">參數</span><span class="sxs-lookup"><span data-stu-id="80e9f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80e9f-109">*AffectedReferencePointCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80e9f-109">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80e9f-110">參考受影響的虛擬系統參考點集合。</span><span class="sxs-lookup"><span data-stu-id="80e9f-110">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="80e9f-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="80e9f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80e9f-112">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="80e9f-112">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80e9f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="80e9f-113">Return value</span></span>

<span data-ttu-id="80e9f-114">如果成功，則會傳回 0 (沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="80e9f-114">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="80e9f-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="80e9f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-116">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="80e9f-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-117">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="80e9f-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-118">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="80e9f-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-119">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="80e9f-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-120">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="80e9f-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-121">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="80e9f-121">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-122">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="80e9f-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="80e9f-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-124">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="80e9f-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="80e9f-125">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="80e9f-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80e9f-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="80e9f-126">Requirements</span></span>



| <span data-ttu-id="80e9f-127">需求</span><span class="sxs-lookup"><span data-stu-id="80e9f-127">Requirement</span></span> | <span data-ttu-id="80e9f-128">值</span><span class="sxs-lookup"><span data-stu-id="80e9f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e9f-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80e9f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="80e9f-130">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80e9f-130">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="80e9f-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80e9f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="80e9f-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="80e9f-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="80e9f-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="80e9f-133">Namespace</span></span><br/>                | <span data-ttu-id="80e9f-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="80e9f-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="80e9f-135">MOF</span><span class="sxs-lookup"><span data-stu-id="80e9f-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80e9f-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="80e9f-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="80e9f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="80e9f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e9f-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="80e9f-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="80e9f-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80e9f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e9f-140">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="80e9f-140">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 





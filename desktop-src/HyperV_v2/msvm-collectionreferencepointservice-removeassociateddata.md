---
description: Msvm_CollectionReferencePointService 類別的 RemoveAssociatedData 方法-移除與參考點關聯的資料記錄檔。
ms.assetid: 42242b76-9123-41a7-b8b1-82d2e827ea53
title: Msvm_CollectionReferencePointService 類別的 RemoveAssociatedData 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66a5cf068545f31f9919a9da60a1b09b32f78e4d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119226"
---
# <a name="removeassociateddata-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="5b224-103">Msvm CollectionReferencePointService 類別的 RemoveAssociatedData 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5b224-103">RemoveAssociatedData method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="5b224-104">移除與參考點關聯的資料記錄檔。</span><span class="sxs-lookup"><span data-stu-id="5b224-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b224-105">語法</span><span class="sxs-lookup"><span data-stu-id="5b224-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5b224-106">參數</span><span class="sxs-lookup"><span data-stu-id="5b224-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b224-107">*AffectedReferencePointCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b224-107">*AffectedReferencePointCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b224-108">參考受影響的虛擬系統參考點集合。</span><span class="sxs-lookup"><span data-stu-id="5b224-108">Reference to the affected virtual system reference point collection.</span></span>

</dd> <dt>

<span data-ttu-id="5b224-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5b224-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b224-110">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="5b224-110">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b224-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b224-111">Return value</span></span>

<span data-ttu-id="5b224-112">如果成功，則會傳回 0 (沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b224-112">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="5b224-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="5b224-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-114">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="5b224-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-115">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="5b224-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-116">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="5b224-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-117">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="5b224-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-118">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="5b224-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-119">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="5b224-119">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-120">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="5b224-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="5b224-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-122">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="5b224-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5b224-123">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="5b224-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5b224-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b224-124">Requirements</span></span>



| <span data-ttu-id="5b224-125">需求</span><span class="sxs-lookup"><span data-stu-id="5b224-125">Requirement</span></span> | <span data-ttu-id="5b224-126">值</span><span class="sxs-lookup"><span data-stu-id="5b224-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b224-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b224-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5b224-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b224-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="5b224-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b224-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5b224-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5b224-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5b224-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b224-131">Namespace</span></span><br/>                | <span data-ttu-id="5b224-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="5b224-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5b224-133">MOF</span><span class="sxs-lookup"><span data-stu-id="5b224-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b224-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="5b224-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b224-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5b224-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b224-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5b224-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5b224-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b224-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b224-138">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="5b224-138">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 





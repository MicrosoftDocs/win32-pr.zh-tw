---
description: 將快照集集合套用至虛擬電腦系統的集合。
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Msvm_CollectionSnapshotService 類別的 ApplySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974026"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a><span data-ttu-id="685b5-103">Msvm CollectionSnapshotService 類別的 ApplySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="685b5-103">ApplySnapshot method of the Msvm\_CollectionSnapshotService class</span></span>

<span data-ttu-id="685b5-104">將快照集集合套用至虛擬電腦系統的集合。</span><span class="sxs-lookup"><span data-stu-id="685b5-104">Applies a snapshot collection to the collection of virtual computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="685b5-105">語法</span><span class="sxs-lookup"><span data-stu-id="685b5-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="685b5-106">參數</span><span class="sxs-lookup"><span data-stu-id="685b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="685b5-107">*SnapshotCollection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="685b5-107">*SnapshotCollection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="685b5-108">[**CIM \_ 集合**](cim-collection.md)的參考，代表要套用的快照集集合。</span><span class="sxs-lookup"><span data-stu-id="685b5-108">A reference to a [**CIM\_Collection**](cim-collection.md) that represents the snapshot collection to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="685b5-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="685b5-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="685b5-110">如果以非同步方式執行作業，則會傳回選擇性的參考。</span><span class="sxs-lookup"><span data-stu-id="685b5-110">An optional reference that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="685b5-111">如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。</span><span class="sxs-lookup"><span data-stu-id="685b5-111">If present, the returned reference to an instance of [**CIM\_ConcreteJob**](cim-concretejob.md) can be used to monitor progress and to obtain the result of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="685b5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="685b5-112">Return value</span></span>

<span data-ttu-id="685b5-113">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="685b5-113">On success, returns a 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="685b5-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="685b5-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="685b5-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="685b5-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="685b5-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="685b5-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="685b5-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-120">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="685b5-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="685b5-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="685b5-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-123">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="685b5-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="685b5-124">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="685b5-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="685b5-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="685b5-125">Requirements</span></span>



| <span data-ttu-id="685b5-126">需求</span><span class="sxs-lookup"><span data-stu-id="685b5-126">Requirement</span></span> | <span data-ttu-id="685b5-127">值</span><span class="sxs-lookup"><span data-stu-id="685b5-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="685b5-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="685b5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="685b5-129">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="685b5-129">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="685b5-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="685b5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="685b5-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="685b5-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="685b5-132">命名空間</span><span class="sxs-lookup"><span data-stu-id="685b5-132">Namespace</span></span><br/>                | <span data-ttu-id="685b5-133">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="685b5-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="685b5-134">MOF</span><span class="sxs-lookup"><span data-stu-id="685b5-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="685b5-135"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="685b5-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="685b5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="685b5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="685b5-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="685b5-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="685b5-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="685b5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="685b5-139">**Msvm \_ CollectionSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="685b5-139">**Msvm\_CollectionSnapshotService**</span></span>](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 





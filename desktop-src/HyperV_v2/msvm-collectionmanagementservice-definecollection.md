---
description: 建立新的 CIM \_ CollectionOfMSEs 物件。
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Msvm_CollectionManagementService 類別的 DefineCollection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996924"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="35e22-103">Msvm CollectionManagementService 類別的 DefineCollection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="35e22-103">DefineCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="35e22-104">建立新的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="35e22-104">Creates a new [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e22-105">語法</span><span class="sxs-lookup"><span data-stu-id="35e22-105">Syntax</span></span>


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="35e22-106">參數</span><span class="sxs-lookup"><span data-stu-id="35e22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35e22-107">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35e22-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e22-108">新集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="35e22-108">The name of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="35e22-109"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="35e22-109">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e22-110">新集合的識別碼。</span><span class="sxs-lookup"><span data-stu-id="35e22-110">The ID of the new collection.</span></span>

</dd> <dt>

<span data-ttu-id="35e22-111">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35e22-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35e22-112">新集合的型別。</span><span class="sxs-lookup"><span data-stu-id="35e22-112">The type of the new collection.</span></span>

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

<span data-ttu-id="35e22-113">**虛擬系統的集合** (0) </span><span class="sxs-lookup"><span data-stu-id="35e22-113">**Collection of Virtual Systems** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

<span data-ttu-id="35e22-114">**集合** (1) </span><span class="sxs-lookup"><span data-stu-id="35e22-114">**Collection of Collections** (1)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="35e22-115">*DefinedCollection* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="35e22-115">*DefinedCollection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35e22-116">定義集合之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="35e22-116">Reference to the objects that define the collection.</span></span>

</dd> <dt>

<span data-ttu-id="35e22-117">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="35e22-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35e22-118">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="35e22-118">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35e22-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="35e22-119">Return value</span></span>

<span data-ttu-id="35e22-120">如果成功，會傳回0或 4096 (已啟動的作業) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="35e22-120">If successful, returns a 0 or 4096 (Job Started); otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="35e22-121">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="35e22-121">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="35e22-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-123">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="35e22-123">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-124">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="35e22-124">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-125">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="35e22-125">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-126">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="35e22-126">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-127">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="35e22-127">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-128">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="35e22-128">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-129">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="35e22-129">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-130">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="35e22-130">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-131">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="35e22-131">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-132">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="35e22-132">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-133">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="35e22-133">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="35e22-134">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="35e22-134">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="35e22-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="35e22-135">Requirements</span></span>



| <span data-ttu-id="35e22-136">需求</span><span class="sxs-lookup"><span data-stu-id="35e22-136">Requirement</span></span> | <span data-ttu-id="35e22-137">值</span><span class="sxs-lookup"><span data-stu-id="35e22-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35e22-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35e22-138">Minimum supported client</span></span><br/> | <span data-ttu-id="35e22-139">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35e22-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="35e22-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35e22-140">Minimum supported server</span></span><br/> | <span data-ttu-id="35e22-141">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="35e22-141">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="35e22-142">命名空間</span><span class="sxs-lookup"><span data-stu-id="35e22-142">Namespace</span></span><br/>                | <span data-ttu-id="35e22-143">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="35e22-143">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="35e22-144">MOF</span><span class="sxs-lookup"><span data-stu-id="35e22-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35e22-145"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="35e22-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="35e22-146">DLL</span><span class="sxs-lookup"><span data-stu-id="35e22-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35e22-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="35e22-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="35e22-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35e22-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35e22-149">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="35e22-149">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 





---
description: 使用指定的識別碼，將指定的 managed 元素移除為 CIM CollectionOfMSEs 的成員 \_ 。 即使具有該識別碼的物件不存在，也會成功。
ms.assetid: 641535f0-ce71-4f57-a4e1-4775b3bb2374
title: Msvm_CollectionManagementService 類別的 RemoveMemberById 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMemberById
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 31c30d8698b16ac9bf128aa13ab80a64f09a40c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195443"
---
# <a name="removememberbyid-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="61903-104">Msvm CollectionManagementService 類別的 RemoveMemberById 方法 \_</span><span class="sxs-lookup"><span data-stu-id="61903-104">RemoveMemberById method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="61903-105">使用指定的識別碼，將指定的 managed 元素移除為 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 的成員。</span><span class="sxs-lookup"><span data-stu-id="61903-105">Removes the specified managed element as a member of the [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) with the given identifier.</span></span> <span data-ttu-id="61903-106">即使具有該識別碼的物件不存在，也會成功。</span><span class="sxs-lookup"><span data-stu-id="61903-106">This will succeed even if the object with that identifier is not present.</span></span>

## <a name="syntax"></a><span data-ttu-id="61903-107">語法</span><span class="sxs-lookup"><span data-stu-id="61903-107">Syntax</span></span>


```mof
uint32 RemoveMemberById(
  [in]  CIM_ManagedElement REF Member,
  [in]  string                 CollectionId,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="61903-108">參數</span><span class="sxs-lookup"><span data-stu-id="61903-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61903-109">*成員* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61903-109">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61903-110">要移除的成員。</span><span class="sxs-lookup"><span data-stu-id="61903-110">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="61903-111">*CollectionId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="61903-111">*CollectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61903-112">要從中移除成員之集合的集合識別碼。</span><span class="sxs-lookup"><span data-stu-id="61903-112">The collection ID of the collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="61903-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61903-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61903-114">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="61903-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61903-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="61903-115">Return value</span></span>

<span data-ttu-id="61903-116">如果成功，則傳回 0; 如果作業已啟動，則傳回 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="61903-116">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="61903-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="61903-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="61903-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="61903-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="61903-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="61903-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="61903-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="61903-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="61903-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="61903-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="61903-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="61903-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="61903-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="61903-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="61903-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="61903-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="61903-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="61903-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="61903-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="61903-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="61903-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="61903-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="61903-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="61903-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="61903-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="61903-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="61903-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="61903-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="61903-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="61903-131">Requirements</span></span>



| <span data-ttu-id="61903-132">需求</span><span class="sxs-lookup"><span data-stu-id="61903-132">Requirement</span></span> | <span data-ttu-id="61903-133">值</span><span class="sxs-lookup"><span data-stu-id="61903-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61903-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61903-134">Minimum supported client</span></span><br/> | <span data-ttu-id="61903-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61903-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="61903-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61903-136">Minimum supported server</span></span><br/> | <span data-ttu-id="61903-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="61903-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="61903-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="61903-138">Namespace</span></span><br/>                | <span data-ttu-id="61903-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="61903-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="61903-140">MOF</span><span class="sxs-lookup"><span data-stu-id="61903-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61903-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="61903-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="61903-142">DLL</span><span class="sxs-lookup"><span data-stu-id="61903-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61903-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="61903-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="61903-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61903-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61903-145">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="61903-145">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 





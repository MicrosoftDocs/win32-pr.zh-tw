---
description: 將指定的 managed 元素移除為指定之 CIM \_ CollectionOfMSEs 物件的成員。
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: Msvm_CollectionManagementService 類別的 RemoveMember 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851852"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="44c34-103">Msvm CollectionManagementService 類別的 RemoveMember 方法 \_</span><span class="sxs-lookup"><span data-stu-id="44c34-103">RemoveMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="44c34-104">將指定的 managed 元素移除為指定之 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的成員。</span><span class="sxs-lookup"><span data-stu-id="44c34-104">Removes the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c34-105">語法</span><span class="sxs-lookup"><span data-stu-id="44c34-105">Syntax</span></span>


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="44c34-106">參數</span><span class="sxs-lookup"><span data-stu-id="44c34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44c34-107">*成員* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44c34-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44c34-108">要移除的成員。</span><span class="sxs-lookup"><span data-stu-id="44c34-108">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="44c34-109">*集合* \[在\]</span><span class="sxs-lookup"><span data-stu-id="44c34-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44c34-110">要從中移除成員的集合。</span><span class="sxs-lookup"><span data-stu-id="44c34-110">The collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="44c34-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="44c34-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="44c34-112">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="44c34-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44c34-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="44c34-113">Return value</span></span>

<span data-ttu-id="44c34-114">如果成功，則傳回 0; 如果作業已啟動，則傳回 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="44c34-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="44c34-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="44c34-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="44c34-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="44c34-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="44c34-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="44c34-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="44c34-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="44c34-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="44c34-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="44c34-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="44c34-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="44c34-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="44c34-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="44c34-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="44c34-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="44c34-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="44c34-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="44c34-129">Requirements</span></span>



| <span data-ttu-id="44c34-130">需求</span><span class="sxs-lookup"><span data-stu-id="44c34-130">Requirement</span></span> | <span data-ttu-id="44c34-131">值</span><span class="sxs-lookup"><span data-stu-id="44c34-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c34-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44c34-132">Minimum supported client</span></span><br/> | <span data-ttu-id="44c34-133">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="44c34-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="44c34-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44c34-134">Minimum supported server</span></span><br/> | <span data-ttu-id="44c34-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="44c34-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="44c34-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="44c34-136">Namespace</span></span><br/>                | <span data-ttu-id="44c34-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="44c34-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="44c34-138">MOF</span><span class="sxs-lookup"><span data-stu-id="44c34-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44c34-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="44c34-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="44c34-140">DLL</span><span class="sxs-lookup"><span data-stu-id="44c34-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c34-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="44c34-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="44c34-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44c34-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c34-143">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="44c34-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 





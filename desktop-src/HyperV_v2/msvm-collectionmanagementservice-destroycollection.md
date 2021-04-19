---
description: 刪除指定的 CIM \_ CollectionOfMSEs 物件。
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Msvm_CollectionManagementService 類別的 DestroyCollection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992515"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="62b70-103">Msvm CollectionManagementService 類別的 DestroyCollection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="62b70-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="62b70-104">刪除指定的 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="62b70-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b70-105">語法</span><span class="sxs-lookup"><span data-stu-id="62b70-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="62b70-106">參數</span><span class="sxs-lookup"><span data-stu-id="62b70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b70-107">*集合* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62b70-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b70-108">要終結的集合。</span><span class="sxs-lookup"><span data-stu-id="62b70-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="62b70-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="62b70-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62b70-110">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="62b70-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b70-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62b70-111">Return value</span></span>

<span data-ttu-id="62b70-112">如果成功，則傳回 0; 如果作業已啟動，則傳回 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="62b70-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="62b70-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="62b70-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="62b70-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="62b70-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="62b70-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="62b70-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="62b70-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="62b70-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="62b70-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="62b70-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="62b70-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="62b70-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="62b70-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="62b70-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="62b70-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="62b70-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="62b70-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="62b70-127">Requirements</span></span>



| <span data-ttu-id="62b70-128">需求</span><span class="sxs-lookup"><span data-stu-id="62b70-128">Requirement</span></span> | <span data-ttu-id="62b70-129">值</span><span class="sxs-lookup"><span data-stu-id="62b70-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b70-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62b70-130">Minimum supported client</span></span><br/> | <span data-ttu-id="62b70-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="62b70-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="62b70-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62b70-132">Minimum supported server</span></span><br/> | <span data-ttu-id="62b70-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="62b70-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="62b70-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="62b70-134">Namespace</span></span><br/>                | <span data-ttu-id="62b70-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="62b70-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="62b70-136">MOF</span><span class="sxs-lookup"><span data-stu-id="62b70-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62b70-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="62b70-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="62b70-138">DLL</span><span class="sxs-lookup"><span data-stu-id="62b70-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b70-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="62b70-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="62b70-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62b70-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b70-141">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="62b70-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 





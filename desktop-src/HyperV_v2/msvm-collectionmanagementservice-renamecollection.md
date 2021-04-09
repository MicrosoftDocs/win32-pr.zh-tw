---
description: 更新所指定 CIM CollectionOfMSEs 物件的元素名稱 \_ 。
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Msvm_CollectionManagementService 類別的 RenameCollection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851851"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="9635e-103">Msvm CollectionManagementService 類別的 RenameCollection 方法 \_</span><span class="sxs-lookup"><span data-stu-id="9635e-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="9635e-104">更新所指定 [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) 物件的元素名稱。</span><span class="sxs-lookup"><span data-stu-id="9635e-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9635e-105">語法</span><span class="sxs-lookup"><span data-stu-id="9635e-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9635e-106">參數</span><span class="sxs-lookup"><span data-stu-id="9635e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9635e-107">*集合* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9635e-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9635e-108">要重新命名的集合。</span><span class="sxs-lookup"><span data-stu-id="9635e-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="9635e-109">*NewName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9635e-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9635e-110">要使用的新名稱。</span><span class="sxs-lookup"><span data-stu-id="9635e-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="9635e-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9635e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9635e-112">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="9635e-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9635e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="9635e-113">Return value</span></span>

<span data-ttu-id="9635e-114">如果成功，則傳回 0; 如果作業已啟動，則傳回 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="9635e-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="9635e-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="9635e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="9635e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="9635e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="9635e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="9635e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="9635e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="9635e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="9635e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="9635e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="9635e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="9635e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="9635e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="9635e-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9635e-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="9635e-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="9635e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="9635e-129">Requirements</span></span>



| <span data-ttu-id="9635e-130">需求</span><span class="sxs-lookup"><span data-stu-id="9635e-130">Requirement</span></span> | <span data-ttu-id="9635e-131">值</span><span class="sxs-lookup"><span data-stu-id="9635e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9635e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9635e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9635e-133">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9635e-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9635e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9635e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9635e-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9635e-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9635e-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="9635e-136">Namespace</span></span><br/>                | <span data-ttu-id="9635e-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="9635e-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9635e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="9635e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9635e-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="9635e-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9635e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="9635e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9635e-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9635e-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9635e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9635e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9635e-143">**Msvm \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="9635e-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 





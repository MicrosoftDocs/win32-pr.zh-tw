---
description: 驗證檔案系統是否可以支援啟用持續性保留的虛擬硬碟。
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Msvm_ImageManagementService 類別的 ValidatePersistentReservationSupport 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943534"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="73777-103">Msvm ImageManagementService 類別的 ValidatePersistentReservationSupport 方法 \_</span><span class="sxs-lookup"><span data-stu-id="73777-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="73777-104">驗證檔案系統是否可以支援啟用持續性保留的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="73777-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="73777-105">語法</span><span class="sxs-lookup"><span data-stu-id="73777-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="73777-106">參數</span><span class="sxs-lookup"><span data-stu-id="73777-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73777-107">*路徑* \[在\]</span><span class="sxs-lookup"><span data-stu-id="73777-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73777-108">完整路徑，指定磁片影像檔案的位置，或可放置磁片影像檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="73777-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="73777-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73777-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73777-110">如果工作已順利完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="73777-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73777-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="73777-111">Return value</span></span>

<span data-ttu-id="73777-112">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="73777-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="73777-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="73777-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="73777-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="73777-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="73777-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="73777-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="73777-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="73777-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="73777-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="73777-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="73777-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="73777-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="73777-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="73777-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="73777-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="73777-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="73777-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="73777-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="73777-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="73777-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="73777-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="73777-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="73777-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="73777-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="73777-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="73777-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="73777-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="73777-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="73777-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="73777-127">Requirements</span></span>



| <span data-ttu-id="73777-128">需求</span><span class="sxs-lookup"><span data-stu-id="73777-128">Requirement</span></span> | <span data-ttu-id="73777-129">值</span><span class="sxs-lookup"><span data-stu-id="73777-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73777-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73777-130">Minimum supported client</span></span><br/> | <span data-ttu-id="73777-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="73777-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="73777-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73777-132">Minimum supported server</span></span><br/> | <span data-ttu-id="73777-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="73777-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="73777-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="73777-134">Namespace</span></span><br/>                | <span data-ttu-id="73777-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="73777-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="73777-136">MOF</span><span class="sxs-lookup"><span data-stu-id="73777-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73777-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="73777-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73777-138">DLL</span><span class="sxs-lookup"><span data-stu-id="73777-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73777-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73777-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="73777-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73777-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73777-141">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="73777-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 





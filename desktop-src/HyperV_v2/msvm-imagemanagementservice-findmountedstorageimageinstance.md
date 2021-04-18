---
description: 尋找 \_ 指定磁片映射路徑的 Msvm MountedStorageImage 物件。
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Msvm_ImageManagementService 類別的 FindMountedStorageImageInstance 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511884"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="69226-103">Msvm ImageManagementService 類別的 FindMountedStorageImageInstance 方法 \_</span><span class="sxs-lookup"><span data-stu-id="69226-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="69226-104">尋找指定磁片映射路徑的 [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="69226-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="69226-105">語法</span><span class="sxs-lookup"><span data-stu-id="69226-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="69226-106">參數</span><span class="sxs-lookup"><span data-stu-id="69226-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69226-107">*SelectionCriterion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69226-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69226-108">指定磁片影像檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="69226-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="69226-109">*CriterionType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69226-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69226-110">尋找磁片映射時要尋找的準則類型。</span><span class="sxs-lookup"><span data-stu-id="69226-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="69226-111">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="69226-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="69226-112">**路徑** (2) </span><span class="sxs-lookup"><span data-stu-id="69226-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="69226-113">*影像* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="69226-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69226-114">如果映射未裝載) ， [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md) (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="69226-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69226-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="69226-115">Return value</span></span>

<span data-ttu-id="69226-116">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="69226-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="69226-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="69226-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69226-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="69226-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="69226-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="69226-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="69226-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="69226-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="69226-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="69226-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="69226-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="69226-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="69226-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="69226-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="69226-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="69226-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="69226-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="69226-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="69226-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="69226-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="69226-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="69226-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="69226-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="69226-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="69226-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="69226-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="69226-130"> (32789) **找不到物件**</span><span class="sxs-lookup"><span data-stu-id="69226-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69226-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="69226-131">Requirements</span></span>



| <span data-ttu-id="69226-132">需求</span><span class="sxs-lookup"><span data-stu-id="69226-132">Requirement</span></span> | <span data-ttu-id="69226-133">值</span><span class="sxs-lookup"><span data-stu-id="69226-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69226-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69226-134">Minimum supported client</span></span><br/> | <span data-ttu-id="69226-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="69226-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="69226-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69226-136">Minimum supported server</span></span><br/> | <span data-ttu-id="69226-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="69226-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="69226-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="69226-138">Namespace</span></span><br/>                | <span data-ttu-id="69226-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="69226-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69226-140">MOF</span><span class="sxs-lookup"><span data-stu-id="69226-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69226-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="69226-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69226-142">DLL</span><span class="sxs-lookup"><span data-stu-id="69226-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69226-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69226-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69226-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69226-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69226-145">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="69226-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 





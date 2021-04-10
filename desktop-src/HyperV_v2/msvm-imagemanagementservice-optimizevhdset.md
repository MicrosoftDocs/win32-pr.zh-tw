---
description: 將 VHD 設定檔案優化，以使用較少的磁碟空間。
ms.assetid: 2d2f4531-5d2d-4334-bcc2-d3d3c15b1f46
title: Msvm_ImageManagementService 類別的 OptimizeVHDSet 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.OptimizeVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c360dcd8acf0a4721b8921cd2ca914c34002d078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848199"
---
# <a name="optimizevhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="b23cc-103">Msvm ImageManagementService 類別的 OptimizeVHDSet 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b23cc-103">OptimizeVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="b23cc-104">將 VHD 設定檔案優化，以使用較少的磁碟空間。</span><span class="sxs-lookup"><span data-stu-id="b23cc-104">Optimizes a VHD Set file to use less disk space.</span></span>

## <a name="syntax"></a><span data-ttu-id="b23cc-105">語法</span><span class="sxs-lookup"><span data-stu-id="b23cc-105">Syntax</span></span>


```mof
uint32 OptimizeVHDSet(
  [in]  string              VHDSetPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b23cc-106">參數</span><span class="sxs-lookup"><span data-stu-id="b23cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b23cc-107">*VHDSetPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b23cc-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cc-108">指定 VHD 設定檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b23cc-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="b23cc-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b23cc-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b23cc-110">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="b23cc-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b23cc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b23cc-111">Return value</span></span>

<span data-ttu-id="b23cc-112">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="b23cc-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="b23cc-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b23cc-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b23cc-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="b23cc-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="b23cc-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="b23cc-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="b23cc-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="b23cc-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="b23cc-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="b23cc-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="b23cc-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="b23cc-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="b23cc-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="b23cc-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b23cc-126">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="b23cc-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b23cc-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b23cc-127">Requirements</span></span>



| <span data-ttu-id="b23cc-128">需求</span><span class="sxs-lookup"><span data-stu-id="b23cc-128">Requirement</span></span> | <span data-ttu-id="b23cc-129">值</span><span class="sxs-lookup"><span data-stu-id="b23cc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b23cc-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b23cc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b23cc-131">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b23cc-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b23cc-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b23cc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b23cc-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b23cc-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b23cc-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="b23cc-134">Namespace</span></span><br/>                | <span data-ttu-id="b23cc-135">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b23cc-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b23cc-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b23cc-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b23cc-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b23cc-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b23cc-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b23cc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b23cc-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b23cc-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b23cc-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b23cc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b23cc-141">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="b23cc-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 





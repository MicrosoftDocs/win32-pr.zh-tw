---
description: 藉由建立新的 VHD 設定檔案與現有的虛擬硬碟來轉換虛擬硬碟檔案。
ms.assetid: 04ae723e-e3c5-4640-a0e5-0e1b75bb2e6d
title: Msvm_ImageManagementService 類別的 ConvertVirtualHardDiskToVHDSet 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDiskToVHDSet
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6113a14f321ff7319f8be15767621db3a7e833de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945212"
---
# <a name="convertvirtualharddisktovhdset-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="45acf-103">Msvm ImageManagementService 類別的 ConvertVirtualHardDiskToVHDSet 方法 \_</span><span class="sxs-lookup"><span data-stu-id="45acf-103">ConvertVirtualHardDiskToVHDSet method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="45acf-104">藉由建立新的 VHD 設定檔案與現有的虛擬硬碟來轉換虛擬硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="45acf-104">Converts a virtual hard disk file by creating a new VHD Set file alongside the existing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="45acf-105">語法</span><span class="sxs-lookup"><span data-stu-id="45acf-105">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDiskToVHDSet(
  [in]  string              VirtualHardDiskPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="45acf-106">參數</span><span class="sxs-lookup"><span data-stu-id="45acf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45acf-107">*VirtualHardDiskPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45acf-107">*VirtualHardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45acf-108">包含虛擬硬碟檔案路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="45acf-108">String containing the path to the virtual hard disk file.</span></span> <span data-ttu-id="45acf-109">新的 VHD 設定檔案將會有相同的檔案名，但會有。VHD 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="45acf-109">The new VHD Set file will have the same filename but with the .VHDS extension.</span></span>

</dd> <dt>

<span data-ttu-id="45acf-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45acf-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45acf-111">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="45acf-111">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45acf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="45acf-112">Return value</span></span>

<span data-ttu-id="45acf-113">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="45acf-113">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="45acf-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="45acf-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-115">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="45acf-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="45acf-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="45acf-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="45acf-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="45acf-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="45acf-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="45acf-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-122">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="45acf-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="45acf-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="45acf-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="45acf-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="45acf-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="45acf-127">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="45acf-127">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="45acf-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="45acf-128">Requirements</span></span>



| <span data-ttu-id="45acf-129">需求</span><span class="sxs-lookup"><span data-stu-id="45acf-129">Requirement</span></span> | <span data-ttu-id="45acf-130">值</span><span class="sxs-lookup"><span data-stu-id="45acf-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45acf-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45acf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="45acf-132">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45acf-132">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="45acf-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45acf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="45acf-134">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="45acf-134">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="45acf-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="45acf-135">Namespace</span></span><br/>                | <span data-ttu-id="45acf-136">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="45acf-136">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="45acf-137">MOF</span><span class="sxs-lookup"><span data-stu-id="45acf-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45acf-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="45acf-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45acf-139">DLL</span><span class="sxs-lookup"><span data-stu-id="45acf-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45acf-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45acf-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45acf-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45acf-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45acf-142">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="45acf-142">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 





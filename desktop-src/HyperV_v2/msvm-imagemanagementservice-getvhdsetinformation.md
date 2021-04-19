---
description: 抓取 VHD 設定檔案的相關資訊。
ms.assetid: efdfd4c6-b762-4369-add3-e152652c6802
title: Msvm_ImageManagementService 類別的 GetVHDSetInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVHDSetInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 16cdcf4a354e6d6b47b6a67c071daf8883905f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972444"
---
# <a name="getvhdsetinformation-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ffaf5-103">Msvm ImageManagementService 類別的 GetVHDSetInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ffaf5-103">GetVHDSetInformation method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ffaf5-104">抓取 VHD 設定檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-104">Retrieves information about a VHD Set file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffaf5-105">語法</span><span class="sxs-lookup"><span data-stu-id="ffaf5-105">Syntax</span></span>


```mof
uint32 GetVHDSetInformation(
  [in]  string              VHDSetPath,
  [in]  uint32              AdditionalInformation[],
  [out] string              Information,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ffaf5-106">參數</span><span class="sxs-lookup"><span data-stu-id="ffaf5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffaf5-107">*VHDSetPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffaf5-107">*VHDSetPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffaf5-108">指定 VHD 設定檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-108">A fully-qualified path that specifies the location of the VHD Set file.</span></span>

</dd> <dt>

<span data-ttu-id="ffaf5-109">*AdditionalInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ffaf5-109">*AdditionalInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffaf5-110">陣列，指定應針對 VHD 設定檔案收集哪些額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-110">An array specifying what additional information should be gathered about the VHD Set file.</span></span> <span data-ttu-id="ffaf5-111">陣列中的每個專案都是一種額外的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-111">Each entry in the array is a type of additional information.</span></span> <span data-ttu-id="ffaf5-112">如果此參數為 Null，則不會抓取任何其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-112">If this parameter is NULL, no additional information will be retrieved.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ffaf5-113">**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-113">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ffaf5-114">**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-114">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Paths"></span><span id="paths"></span><span id="PATHS"></span>

<span data-ttu-id="ffaf5-115">**路徑** (2) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-115">**Paths** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ffaf5-116">*資訊* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffaf5-116">*Information* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffaf5-117">如果成功，此物件就會包含所要求 VHD 設定檔案的資訊。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-117">If successful, this object contains the information for the requested VHD Set file.</span></span> <span data-ttu-id="ffaf5-118">這是 [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-118">This is an embedded instance of [**Msvm\_VHDSetInformation**](msvm-vhdsetinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="ffaf5-119">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ffaf5-119">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffaf5-120">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="ffaf5-120">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffaf5-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="ffaf5-121">Return value</span></span>

<span data-ttu-id="ffaf5-122">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="ffaf5-122">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ffaf5-123">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-123">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-124">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-125">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-125">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-126">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-126">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-127">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-127">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-128">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-128">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-129">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-129">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-130">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-130">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-131">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-131">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-132">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-132">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-133">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-133">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-134">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-134">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-135">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-135">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ffaf5-136">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="ffaf5-136">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ffaf5-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffaf5-137">Requirements</span></span>



| <span data-ttu-id="ffaf5-138">需求</span><span class="sxs-lookup"><span data-stu-id="ffaf5-138">Requirement</span></span> | <span data-ttu-id="ffaf5-139">值</span><span class="sxs-lookup"><span data-stu-id="ffaf5-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffaf5-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffaf5-140">Minimum supported client</span></span><br/> | <span data-ttu-id="ffaf5-141">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ffaf5-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="ffaf5-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffaf5-142">Minimum supported server</span></span><br/> | <span data-ttu-id="ffaf5-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ffaf5-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ffaf5-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="ffaf5-144">Namespace</span></span><br/>                | <span data-ttu-id="ffaf5-145">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ffaf5-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ffaf5-146">MOF</span><span class="sxs-lookup"><span data-stu-id="ffaf5-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffaf5-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ffaf5-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffaf5-148">DLL</span><span class="sxs-lookup"><span data-stu-id="ffaf5-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffaf5-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffaf5-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffaf5-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffaf5-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffaf5-151">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="ffaf5-151">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 





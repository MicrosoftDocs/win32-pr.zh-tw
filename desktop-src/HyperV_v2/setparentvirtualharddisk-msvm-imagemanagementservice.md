---
description: 更新指定分葉和子虛擬硬碟檔案的父系。
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Msvm_ImageManagementService 類別的 SetParentVirtualHardDisk 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982410"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="45770-103">Msvm ImageManagementService 類別的 SetParentVirtualHardDisk 方法 \_</span><span class="sxs-lookup"><span data-stu-id="45770-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="45770-104">更新指定分葉和子虛擬硬碟檔案的父系。</span><span class="sxs-lookup"><span data-stu-id="45770-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="45770-105">請參閱此方法使用限制的備註。</span><span class="sxs-lookup"><span data-stu-id="45770-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="45770-106">語法</span><span class="sxs-lookup"><span data-stu-id="45770-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="45770-107">參數</span><span class="sxs-lookup"><span data-stu-id="45770-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45770-108">*ChildPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45770-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45770-109">指定子虛擬硬碟檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45770-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="45770-110">*ParentPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45770-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45770-111">指定父虛擬硬碟檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45770-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="45770-112">*LeafPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45770-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45770-113">指定分葉虛擬硬碟檔案位置的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="45770-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="45770-114">如果虛擬硬碟處於離線狀態，則此參數可以是 **Null** ，但如果虛擬硬碟正在使用中，則必須指定。</span><span class="sxs-lookup"><span data-stu-id="45770-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="45770-115">*IgnoreIDMismatch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="45770-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45770-116">指出當虛擬磁片識別碼不相符時，是否應強制設定父系。</span><span class="sxs-lookup"><span data-stu-id="45770-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="45770-117">必須小心使用這個參數，因為如果新的父虛擬硬碟與原始父系不同，則可能會發生資料損毀。</span><span class="sxs-lookup"><span data-stu-id="45770-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="45770-118">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="45770-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45770-119">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="45770-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45770-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="45770-120">Return value</span></span>

<span data-ttu-id="45770-121">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="45770-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="45770-122">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="45770-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45770-123">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="45770-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="45770-124">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="45770-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="45770-125">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="45770-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="45770-126">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="45770-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="45770-127">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="45770-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="45770-128">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="45770-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="45770-129">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="45770-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="45770-130">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="45770-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="45770-131">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="45770-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="45770-132">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="45770-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="45770-133">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="45770-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="45770-134">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="45770-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="45770-135">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="45770-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="45770-136">備註</span><span class="sxs-lookup"><span data-stu-id="45770-136">Remarks</span></span>

<span data-ttu-id="45770-137">只有下列類型的虛擬硬碟可搭配此方法使用：</span><span class="sxs-lookup"><span data-stu-id="45770-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="45770-138">差異 VHD</span><span class="sxs-lookup"><span data-stu-id="45770-138">Differencing VHD</span></span>
-   <span data-ttu-id="45770-139">差異 VHDX</span><span class="sxs-lookup"><span data-stu-id="45770-139">Differencing VHDX</span></span>

<span data-ttu-id="45770-140">存取 [**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="45770-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="45770-141">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="45770-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="45770-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="45770-142">Requirements</span></span>



| <span data-ttu-id="45770-143">需求</span><span class="sxs-lookup"><span data-stu-id="45770-143">Requirement</span></span> | <span data-ttu-id="45770-144">值</span><span class="sxs-lookup"><span data-stu-id="45770-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45770-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="45770-145">Minimum supported client</span></span><br/> | <span data-ttu-id="45770-146">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45770-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45770-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="45770-147">Minimum supported server</span></span><br/> | <span data-ttu-id="45770-148">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="45770-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45770-149">命名空間</span><span class="sxs-lookup"><span data-stu-id="45770-149">Namespace</span></span><br/>                | <span data-ttu-id="45770-150">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="45770-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45770-151">MOF</span><span class="sxs-lookup"><span data-stu-id="45770-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45770-152"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="45770-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45770-153">DLL</span><span class="sxs-lookup"><span data-stu-id="45770-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45770-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45770-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="45770-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45770-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45770-156">**Msvm \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="45770-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 


---
description: 修改磁片合併設定資料。
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Msvm_VirtualSystemManagementService 類別的 ModifyDiskMergeSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983741"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="16fcd-103">Msvm VirtualSystemManagementService 類別的 ModifyDiskMergeSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="16fcd-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="16fcd-104">修改磁片合併設定資料。</span><span class="sxs-lookup"><span data-stu-id="16fcd-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="16fcd-105">語法</span><span class="sxs-lookup"><span data-stu-id="16fcd-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="16fcd-106">參數</span><span class="sxs-lookup"><span data-stu-id="16fcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16fcd-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16fcd-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16fcd-108">[**Msvm \_ DiskMergeSettingData**](msvm-diskmergesettingdata.md)類別的內嵌實例，其中包含已修改的磁片合併函數設定資料。</span><span class="sxs-lookup"><span data-stu-id="16fcd-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="16fcd-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="16fcd-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16fcd-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="16fcd-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16fcd-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="16fcd-111">Return value</span></span>

<span data-ttu-id="16fcd-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="16fcd-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="16fcd-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="16fcd-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="16fcd-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="16fcd-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="16fcd-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="16fcd-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="16fcd-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="16fcd-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="16fcd-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="16fcd-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="16fcd-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="16fcd-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="16fcd-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="16fcd-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="16fcd-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="16fcd-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="16fcd-126">Requirements</span></span>



| <span data-ttu-id="16fcd-127">需求</span><span class="sxs-lookup"><span data-stu-id="16fcd-127">Requirement</span></span> | <span data-ttu-id="16fcd-128">值</span><span class="sxs-lookup"><span data-stu-id="16fcd-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16fcd-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16fcd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="16fcd-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16fcd-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="16fcd-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16fcd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="16fcd-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="16fcd-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16fcd-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="16fcd-133">Namespace</span></span><br/>                | <span data-ttu-id="16fcd-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="16fcd-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="16fcd-135">MOF</span><span class="sxs-lookup"><span data-stu-id="16fcd-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16fcd-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="16fcd-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="16fcd-137">DLL</span><span class="sxs-lookup"><span data-stu-id="16fcd-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16fcd-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="16fcd-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="16fcd-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16fcd-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16fcd-140">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="16fcd-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 


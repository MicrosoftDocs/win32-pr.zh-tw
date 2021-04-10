---
description: 將虛擬機器快照集套用至其建立來源的虛擬機器。
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Msvm_VirtualSystemSnapshotService 類別的 ApplySnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 735e827935689a0f0ede7fbac1d582ea40772ee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849343"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="0f0bb-103">Msvm VirtualSystemSnapshotService 類別的 ApplySnapshot 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0f0bb-103">ApplySnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="0f0bb-104">將虛擬機器快照集套用至其建立來源的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0f0bb-104">Applies a virtual machine snapshot to the virtual machine that it was created from.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f0bb-105">Syntax</span></span>


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0f0bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f0bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f0bb-107">*快照* \[ 集在\]</span><span class="sxs-lookup"><span data-stu-id="0f0bb-107">*Snapshot* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0bb-108">衍生自 [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) 之類別的參考，代表要套用的虛擬機器快照集。</span><span class="sxs-lookup"><span data-stu-id="0f0bb-108">A reference to a class derived from [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) that represents the virtual machine snapshot to be applied.</span></span>

</dd> <dt>

<span data-ttu-id="0f0bb-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0f0bb-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f0bb-110">這項作業一律會以非同步方式執行。</span><span class="sxs-lookup"><span data-stu-id="0f0bb-110">This operation is always performed asynchronously.</span></span> <span data-ttu-id="0f0bb-111">這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="0f0bb-111">This method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f0bb-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f0bb-112">Return value</span></span>

<span data-ttu-id="0f0bb-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0f0bb-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0f0bb-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-115">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-116">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-117">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-118">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-119">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-120">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-120">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-121">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-122">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-123">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-124">**Invalid Parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-125">**不正確狀態** (32775) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-125">**Invalid State** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-126">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-126">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0f0bb-127">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="0f0bb-127">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0f0bb-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f0bb-128">Requirements</span></span>



| <span data-ttu-id="0f0bb-129">需求</span><span class="sxs-lookup"><span data-stu-id="0f0bb-129">Requirement</span></span> | <span data-ttu-id="0f0bb-130">值</span><span class="sxs-lookup"><span data-stu-id="0f0bb-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0bb-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f0bb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0bb-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f0bb-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0f0bb-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f0bb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0bb-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f0bb-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f0bb-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="0f0bb-135">Namespace</span></span><br/>                | <span data-ttu-id="0f0bb-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="0f0bb-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0f0bb-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0f0bb-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f0bb-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="0f0bb-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f0bb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0f0bb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f0bb-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f0bb-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f0bb-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f0bb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f0bb-142">**Msvm \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="0f0bb-142">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="0f0bb-143">**ApplyVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="0f0bb-143">**ApplyVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="0f0bb-144">**ApplyVirtualSystemSnapshotEx (V1)**</span><span class="sxs-lookup"><span data-stu-id="0f0bb-144">**ApplyVirtualSystemSnapshotEx (V1)**</span></span>](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 


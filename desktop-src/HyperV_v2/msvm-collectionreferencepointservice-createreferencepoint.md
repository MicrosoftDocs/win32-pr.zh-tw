---
description: 建立虛擬系統集合的參考點。
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Msvm_CollectionReferencePointService 類別的 CreateReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321103"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="2eb7b-103">Msvm CollectionReferencePointService 類別的 CreateReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2eb7b-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="2eb7b-104">建立虛擬系統集合的參考點。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eb7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="2eb7b-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2eb7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="2eb7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eb7b-107">*集合* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb7b-108">參考受影響的虛擬系統集合。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="2eb7b-109">*ReferencePointSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb7b-110">參數設定。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="2eb7b-111">*ReferencePointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb7b-112">指出參考點的型別。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eb7b-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="2eb7b-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>以 **記錄為基礎** 的 (1) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2eb7b-115">Hyper-v 複本記錄追蹤。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="2eb7b-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**依** (2) 的 .rct</span><span class="sxs-lookup"><span data-stu-id="2eb7b-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2eb7b-117">以虛擬磁片的復原變更追蹤為基礎。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="2eb7b-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="2eb7b-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="2eb7b-120">*ResultingReferencePointCollection* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb7b-121">虛擬系統集合的結果參考點。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="2eb7b-122">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eb7b-123">如果作業的執行時間很長，則可以選擇性地傳回作業。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eb7b-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="2eb7b-124">Return value</span></span>

<span data-ttu-id="2eb7b-125">如果成功，則會傳回 0 (沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="2eb7b-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="2eb7b-126">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-127">**不支援** (1) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-128">**失敗** (2) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-129">**Timeout** (3) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-130">**不正確參數** (4) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-131">**不正確狀態** (5) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-132">**不正確類型** (6) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-133">**DMTF 保留** ( .。。) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-134">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-135">**方法保留** (4097. 32767) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2eb7b-136">**廠商特定** (32768. 65535) </span><span class="sxs-lookup"><span data-stu-id="2eb7b-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2eb7b-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eb7b-137">Requirements</span></span>



| <span data-ttu-id="2eb7b-138">需求</span><span class="sxs-lookup"><span data-stu-id="2eb7b-138">Requirement</span></span> | <span data-ttu-id="2eb7b-139">值</span><span class="sxs-lookup"><span data-stu-id="2eb7b-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2eb7b-140">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eb7b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb7b-141">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb7b-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2eb7b-142">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eb7b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb7b-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2eb7b-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2eb7b-144">命名空間</span><span class="sxs-lookup"><span data-stu-id="2eb7b-144">Namespace</span></span><br/>                | <span data-ttu-id="2eb7b-145">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="2eb7b-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2eb7b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="2eb7b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eb7b-147"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="2eb7b-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eb7b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="2eb7b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eb7b-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2eb7b-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2eb7b-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2eb7b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eb7b-151">**Msvm \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="2eb7b-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 





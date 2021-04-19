---
description: 匯出虛擬系統的參考點。
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Msvm_VirtualSystemReferencePointService 類別的 ExportReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106974763"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="08d08-103">Msvm VirtualSystemReferencePointService 類別的 ExportReferencePoint 方法 \_</span><span class="sxs-lookup"><span data-stu-id="08d08-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="08d08-104">匯出虛擬系統的參考點。</span><span class="sxs-lookup"><span data-stu-id="08d08-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="08d08-105">語法</span><span class="sxs-lookup"><span data-stu-id="08d08-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="08d08-106">參數</span><span class="sxs-lookup"><span data-stu-id="08d08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08d08-107">*ReferencePoint* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08d08-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d08-108">[**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)實例的參考，代表要匯出的參考點。</span><span class="sxs-lookup"><span data-stu-id="08d08-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="08d08-109">*ExportDirectory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08d08-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d08-110">要匯出參考點之目錄的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="08d08-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="08d08-111">*ExportSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="08d08-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08d08-112">[**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)的實例，表示匯出作業的設定。</span><span class="sxs-lookup"><span data-stu-id="08d08-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="08d08-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="08d08-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08d08-114">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="08d08-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="08d08-115">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="08d08-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08d08-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="08d08-116">Return value</span></span>

<span data-ttu-id="08d08-117">成功時，會傳回 0 (完成，沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="08d08-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="08d08-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="08d08-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="08d08-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="08d08-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="08d08-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="08d08-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="08d08-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="08d08-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="08d08-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="08d08-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="08d08-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="08d08-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="08d08-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="08d08-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="08d08-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="08d08-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="08d08-131">Requirements</span></span>



| <span data-ttu-id="08d08-132">需求</span><span class="sxs-lookup"><span data-stu-id="08d08-132">Requirement</span></span> | <span data-ttu-id="08d08-133">值</span><span class="sxs-lookup"><span data-stu-id="08d08-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08d08-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="08d08-134">Minimum supported client</span></span><br/> | <span data-ttu-id="08d08-135">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="08d08-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="08d08-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="08d08-136">Minimum supported server</span></span><br/> | <span data-ttu-id="08d08-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="08d08-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="08d08-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="08d08-138">Namespace</span></span><br/>                | <span data-ttu-id="08d08-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="08d08-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="08d08-140">MOF</span><span class="sxs-lookup"><span data-stu-id="08d08-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08d08-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="08d08-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="08d08-142">DLL</span><span class="sxs-lookup"><span data-stu-id="08d08-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08d08-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="08d08-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="08d08-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08d08-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08d08-145">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="08d08-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 





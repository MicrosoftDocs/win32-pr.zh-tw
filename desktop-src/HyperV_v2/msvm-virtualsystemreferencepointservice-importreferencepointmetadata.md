---
description: 匯入虛擬系統的參考點中繼資料。
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Msvm_VirtualSystemReferencePointService 類別的 ImportReferencePointMetadata 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103945698"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="be489-103">Msvm VirtualSystemReferencePointService 類別的 ImportReferencePointMetadata 方法 \_</span><span class="sxs-lookup"><span data-stu-id="be489-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="be489-104">匯入虛擬系統的參考點中繼資料。</span><span class="sxs-lookup"><span data-stu-id="be489-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="be489-105">語法</span><span class="sxs-lookup"><span data-stu-id="be489-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="be489-106">參數</span><span class="sxs-lookup"><span data-stu-id="be489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be489-107">*AffectedSystem* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be489-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be489-108">描述受影響系統 [**的 \_ Msvm**](msvm-computersystem.md) 系統系統的參考。</span><span class="sxs-lookup"><span data-stu-id="be489-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="be489-109">*ConfigFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be489-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be489-110">將匯入參考點中繼資料之設定檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="be489-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="be489-111">*RuntimeStateFilePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="be489-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be489-112">要從中匯入參考點中繼資料之執行時間狀態檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="be489-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="be489-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="be489-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be489-114">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="be489-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="be489-115">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="be489-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be489-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="be489-116">Return value</span></span>

<span data-ttu-id="be489-117">傳回 0 (沒有錯誤) 或下列其中一個錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="be489-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="be489-118">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="be489-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="be489-119">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="be489-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="be489-120">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="be489-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="be489-121">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="be489-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="be489-122">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="be489-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="be489-123">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="be489-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="be489-124">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="be489-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="be489-125">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="be489-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="be489-126">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="be489-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="be489-127">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="be489-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="be489-128">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="be489-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="be489-129">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="be489-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="be489-130">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="be489-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="be489-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="be489-131">Requirements</span></span>



| <span data-ttu-id="be489-132">需求</span><span class="sxs-lookup"><span data-stu-id="be489-132">Requirement</span></span> | <span data-ttu-id="be489-133">值</span><span class="sxs-lookup"><span data-stu-id="be489-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be489-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be489-134">Minimum supported client</span></span><br/> | <span data-ttu-id="be489-135">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="be489-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="be489-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be489-136">Minimum supported server</span></span><br/> | <span data-ttu-id="be489-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="be489-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="be489-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="be489-138">Namespace</span></span><br/>                | <span data-ttu-id="be489-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="be489-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="be489-140">MOF</span><span class="sxs-lookup"><span data-stu-id="be489-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be489-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="be489-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be489-142">DLL</span><span class="sxs-lookup"><span data-stu-id="be489-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be489-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be489-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be489-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be489-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be489-145">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="be489-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 





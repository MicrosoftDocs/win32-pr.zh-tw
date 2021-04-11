---
description: 匯入虛擬機器的初始複寫。
ms.assetid: 151211fe-e58e-4fd4-87cd-cdb2ad55c0b1
title: Msvm_ReplicationService 類別的 ImportInitialReplica 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ImportInitialReplica
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b60ab10c6387127c294a472c9e1e86be7fd84146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114585"
---
# <a name="importinitialreplica-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="bcfd9-103">Msvm ReplicationService 類別的 ImportInitialReplica 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bcfd9-103">ImportInitialReplica method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="bcfd9-104">匯入虛擬機器的初始複寫。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-104">Imports the initial replication for a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfd9-105">語法</span><span class="sxs-lookup"><span data-stu-id="bcfd9-105">Syntax</span></span>


```mof
uint32 ImportInitialReplica(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 InitialReplicationImportLocation,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bcfd9-106">參數</span><span class="sxs-lookup"><span data-stu-id="bcfd9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcfd9-107">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="bcfd9-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd9-108">[**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem)實例類型的參考，代表應匯入初始複寫的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) instance that represents the virtual machine for which the initial replication should be imported.</span></span>

</dd> <dt>

<span data-ttu-id="bcfd9-109">*InitialReplicationImportLocation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bcfd9-109">*InitialReplicationImportLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd9-110">要匯入初始複寫的目錄完整路徑。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-110">The fully qualified path of the directory from which the initial replication is to be imported.</span></span> <span data-ttu-id="bcfd9-111">這不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-111">This cannot be **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="bcfd9-112">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bcfd9-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfd9-113">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcfd9-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="bcfd9-114">Return value</span></span>

<span data-ttu-id="bcfd9-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bcfd9-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bcfd9-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bcfd9-129">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="bcfd9-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="bcfd9-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcfd9-130">Requirements</span></span>



| <span data-ttu-id="bcfd9-131">需求</span><span class="sxs-lookup"><span data-stu-id="bcfd9-131">Requirement</span></span> | <span data-ttu-id="bcfd9-132">值</span><span class="sxs-lookup"><span data-stu-id="bcfd9-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfd9-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcfd9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfd9-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcfd9-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bcfd9-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcfd9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfd9-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcfd9-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcfd9-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="bcfd9-137">Namespace</span></span><br/>                | <span data-ttu-id="bcfd9-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bcfd9-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bcfd9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bcfd9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcfd9-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bcfd9-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcfd9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bcfd9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcfd9-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcfd9-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bcfd9-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bcfd9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcfd9-144">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="bcfd9-144">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 


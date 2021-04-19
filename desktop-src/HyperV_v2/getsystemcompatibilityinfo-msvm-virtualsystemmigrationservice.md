---
description: 產生不透明的資料 blob，其中包含指定系統的相容性資訊。
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Msvm_VirtualSystemMigrationService 類別的 GetSystemCompatibilityInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999850"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="d3004-103">Msvm VirtualSystemMigrationService 類別的 GetSystemCompatibilityInfo 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d3004-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="d3004-104">產生不透明的資料 blob，其中包含指定系統的相容性資訊。</span><span class="sxs-lookup"><span data-stu-id="d3004-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="d3004-105">這個方法會與 [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) 方法搭配使用，以判斷是否能夠快速或即時將虛擬機器遷移至另一部主機電腦系統，而不需要實際嘗試進行遷移。</span><span class="sxs-lookup"><span data-stu-id="d3004-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3004-106">語法</span><span class="sxs-lookup"><span data-stu-id="d3004-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="d3004-107">參數</span><span class="sxs-lookup"><span data-stu-id="d3004-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3004-108">未進行 \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3004-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3004-109">[**Msvm \_**](msvm-computersystem.md)電腦類型的參考，代表要取得其相容性資訊的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d3004-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="d3004-110">如果這個參數參考主控電腦系統， *CompatibilityInfo* 參數中所傳回的資料可以用來判斷主控電腦系統上的任何虛擬機器是否可以快速遷移到另一個主控電腦系統。</span><span class="sxs-lookup"><span data-stu-id="d3004-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="d3004-111">*CompatibilityInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3004-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3004-112">可以傳遞至另一部主控電腦系統上 [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) 方法以確認相容性之資料的不透明 blob。</span><span class="sxs-lookup"><span data-stu-id="d3004-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3004-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3004-113">Return value</span></span>

<span data-ttu-id="d3004-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d3004-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d3004-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d3004-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d3004-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d3004-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d3004-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d3004-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="d3004-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d3004-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d3004-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d3004-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="d3004-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="d3004-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d3004-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d3004-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d3004-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d3004-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3004-128">Requirements</span></span>



| <span data-ttu-id="d3004-129">需求</span><span class="sxs-lookup"><span data-stu-id="d3004-129">Requirement</span></span> | <span data-ttu-id="d3004-130">值</span><span class="sxs-lookup"><span data-stu-id="d3004-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3004-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3004-131">Minimum supported client</span></span><br/> | <span data-ttu-id="d3004-132">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3004-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d3004-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3004-133">Minimum supported server</span></span><br/> | <span data-ttu-id="d3004-134">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3004-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3004-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="d3004-135">Namespace</span></span><br/>                | <span data-ttu-id="d3004-136">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="d3004-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d3004-137">MOF</span><span class="sxs-lookup"><span data-stu-id="d3004-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3004-138"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d3004-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d3004-139">DLL</span><span class="sxs-lookup"><span data-stu-id="d3004-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3004-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d3004-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d3004-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3004-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3004-142">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="d3004-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





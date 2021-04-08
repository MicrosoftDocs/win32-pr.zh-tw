---
description: 檢查相容性資訊是否與主控電腦系統相容。
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Msvm_VirtualSystemMigrationService 類別的 CheckSystemCompatibilityInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847772"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="63adf-103">Msvm VirtualSystemMigrationService 類別的 CheckSystemCompatibilityInfo 方法 \_</span><span class="sxs-lookup"><span data-stu-id="63adf-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="63adf-104">檢查相容性資訊是否與主控電腦系統相容。</span><span class="sxs-lookup"><span data-stu-id="63adf-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="63adf-105">語法</span><span class="sxs-lookup"><span data-stu-id="63adf-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="63adf-106">參數</span><span class="sxs-lookup"><span data-stu-id="63adf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63adf-107">*CompatibilityInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="63adf-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63adf-108">在主控電腦系統上呼叫 [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) 方法所取得的資料 blob。</span><span class="sxs-lookup"><span data-stu-id="63adf-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="63adf-109">*原因* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="63adf-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63adf-110">字串陣列，這些字串會接收代表任何警告或錯誤之 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="63adf-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63adf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="63adf-111">Return value</span></span>

<span data-ttu-id="63adf-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="63adf-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="63adf-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="63adf-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="63adf-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="63adf-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="63adf-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="63adf-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="63adf-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="63adf-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="63adf-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="63adf-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="63adf-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="63adf-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="63adf-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="63adf-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="63adf-126">**不相容** (32784) </span><span class="sxs-lookup"><span data-stu-id="63adf-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="63adf-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="63adf-127">Requirements</span></span>



| <span data-ttu-id="63adf-128">需求</span><span class="sxs-lookup"><span data-stu-id="63adf-128">Requirement</span></span> | <span data-ttu-id="63adf-129">值</span><span class="sxs-lookup"><span data-stu-id="63adf-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63adf-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="63adf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="63adf-131">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63adf-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="63adf-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="63adf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="63adf-133">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="63adf-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63adf-134">命名空間</span><span class="sxs-lookup"><span data-stu-id="63adf-134">Namespace</span></span><br/>                | <span data-ttu-id="63adf-135">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="63adf-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="63adf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="63adf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63adf-137"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="63adf-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="63adf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="63adf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63adf-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="63adf-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="63adf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="63adf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63adf-141">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="63adf-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 





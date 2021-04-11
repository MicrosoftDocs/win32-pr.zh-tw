---
description: 捕獲錯誤。
ms.assetid: a30cb74a-4e41-4981-b355-6f46b4b75ce6
title: Msvm_VirtualSystemReferencePointExportJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b26995171059389f7f7afb3fb90e3506b39affd5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104027644"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="03ebf-103">Msvm VirtualSystemReferencePointExportJob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="03ebf-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="03ebf-104">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="03ebf-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ebf-105">語法</span><span class="sxs-lookup"><span data-stu-id="03ebf-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="03ebf-106">參數</span><span class="sxs-lookup"><span data-stu-id="03ebf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ebf-107">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="03ebf-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03ebf-108">取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="03ebf-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ebf-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="03ebf-109">Return value</span></span>

<span data-ttu-id="03ebf-110">成功時，會傳回 0;否則，會包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="03ebf-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="03ebf-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="03ebf-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-112">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="03ebf-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-113">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="03ebf-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-114">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="03ebf-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-115">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="03ebf-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-116">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="03ebf-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-117">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="03ebf-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-118">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="03ebf-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-119">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="03ebf-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-120">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="03ebf-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-121">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="03ebf-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="03ebf-122">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="03ebf-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="03ebf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="03ebf-123">Requirements</span></span>



| <span data-ttu-id="03ebf-124">需求</span><span class="sxs-lookup"><span data-stu-id="03ebf-124">Requirement</span></span> | <span data-ttu-id="03ebf-125">值</span><span class="sxs-lookup"><span data-stu-id="03ebf-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ebf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03ebf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="03ebf-127">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03ebf-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="03ebf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03ebf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="03ebf-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="03ebf-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="03ebf-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="03ebf-130">Namespace</span></span><br/>                | <span data-ttu-id="03ebf-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="03ebf-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="03ebf-132">MOF</span><span class="sxs-lookup"><span data-stu-id="03ebf-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03ebf-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="03ebf-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03ebf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="03ebf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ebf-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03ebf-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03ebf-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03ebf-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ebf-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="03ebf-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 





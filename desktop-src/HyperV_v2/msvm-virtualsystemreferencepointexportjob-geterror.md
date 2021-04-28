---
description: Msvm_VirtualSystemReferencePointExportJob 類別的 GetError 方法-抓取錯誤。
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
ms.openlocfilehash: d1311e4e56b6396266ece72277e8ddadcdb9d835
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109336"
---
# <a name="geterror-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="d170a-103">Msvm VirtualSystemReferencePointExportJob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d170a-103">GetError method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="d170a-104">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="d170a-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="d170a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d170a-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="d170a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d170a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d170a-107">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d170a-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d170a-108">取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="d170a-108">The error retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d170a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d170a-109">Return value</span></span>

<span data-ttu-id="d170a-110">成功時，會傳回 0;否則，會包含錯誤。</span><span class="sxs-lookup"><span data-stu-id="d170a-110">On success, returns a 0; otherwise, contains an error.</span></span>

<dl> <dt>

<span data-ttu-id="d170a-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d170a-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-112">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d170a-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-113">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d170a-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-114">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d170a-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-115">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="d170a-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-116">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d170a-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-117">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d170a-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-118">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="d170a-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-119">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="d170a-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-120">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="d170a-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-121">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d170a-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d170a-122">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d170a-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d170a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="d170a-123">Requirements</span></span>



| <span data-ttu-id="d170a-124">需求</span><span class="sxs-lookup"><span data-stu-id="d170a-124">Requirement</span></span> | <span data-ttu-id="d170a-125">值</span><span class="sxs-lookup"><span data-stu-id="d170a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d170a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d170a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d170a-127">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d170a-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d170a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d170a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d170a-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d170a-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d170a-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="d170a-130">Namespace</span></span><br/>                | <span data-ttu-id="d170a-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d170a-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d170a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="d170a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d170a-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d170a-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d170a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d170a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d170a-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d170a-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d170a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d170a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d170a-137">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="d170a-137">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 





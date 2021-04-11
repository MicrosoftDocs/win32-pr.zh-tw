---
description: 捕獲錯誤。
ms.assetid: 785b83c4-06f4-46b5-81f7-35c6fce16c92
title: Msvm_StorageJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a7d8ff9c2c01bb21343b4859e2db2dbed7ad643e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850280"
---
# <a name="geterror-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="273d7-103">Msvm Get-storagejob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="273d7-103">GetError method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="273d7-104">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="273d7-104">Retrieves the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="273d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="273d7-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="273d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="273d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="273d7-107">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="273d7-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="273d7-108">已取出的錯誤。</span><span class="sxs-lookup"><span data-stu-id="273d7-108">The retrieved error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="273d7-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="273d7-109">Return value</span></span>

<span data-ttu-id="273d7-110">這個方法會傳回下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="273d7-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="273d7-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="273d7-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-112">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="273d7-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-113">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="273d7-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-114">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="273d7-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-115">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="273d7-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-116">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="273d7-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-117">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="273d7-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-118">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="273d7-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-119">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="273d7-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-120">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="273d7-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-121">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="273d7-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="273d7-122">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="273d7-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="273d7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="273d7-123">Requirements</span></span>



| <span data-ttu-id="273d7-124">需求</span><span class="sxs-lookup"><span data-stu-id="273d7-124">Requirement</span></span> | <span data-ttu-id="273d7-125">值</span><span class="sxs-lookup"><span data-stu-id="273d7-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="273d7-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="273d7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="273d7-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="273d7-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="273d7-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="273d7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="273d7-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="273d7-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="273d7-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="273d7-130">Namespace</span></span><br/>                | <span data-ttu-id="273d7-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="273d7-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="273d7-132">MOF</span><span class="sxs-lookup"><span data-stu-id="273d7-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="273d7-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="273d7-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="273d7-134">DLL</span><span class="sxs-lookup"><span data-stu-id="273d7-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="273d7-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="273d7-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="273d7-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="273d7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="273d7-137">**Msvm \_ get-storagejob**</span><span class="sxs-lookup"><span data-stu-id="273d7-137">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 

 





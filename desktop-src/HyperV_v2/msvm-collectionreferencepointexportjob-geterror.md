---
description: 捕獲錯誤。
ms.assetid: 7c47acae-d398-4698-81db-e3c8a812f339
title: Msvm_CollectionReferencePointExportJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ea92bd08a2b65466d11e41bb459200610a89677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027366"
---
# <a name="geterror-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="79624-103">Msvm CollectionReferencePointExportJob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="79624-103">GetError method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="79624-104">捕獲錯誤。</span><span class="sxs-lookup"><span data-stu-id="79624-104">Retrieves an error.</span></span>

## <a name="syntax"></a><span data-ttu-id="79624-105">語法</span><span class="sxs-lookup"><span data-stu-id="79624-105">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="79624-106">參數</span><span class="sxs-lookup"><span data-stu-id="79624-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79624-107">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="79624-107">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79624-108">成功時，會包含錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="79624-108">On success, contains a description of the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79624-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="79624-109">Return value</span></span>

<span data-ttu-id="79624-110">0（成功）;否則，就會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="79624-110">0 on success; otherwise, an error.</span></span>

<dl> <dt>

<span data-ttu-id="79624-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="79624-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="79624-112">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="79624-112">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="79624-113">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="79624-113">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="79624-114">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="79624-114">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="79624-115">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="79624-115">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="79624-116">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="79624-116">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="79624-117">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="79624-117">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="79624-118">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="79624-118">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="79624-119">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="79624-119">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="79624-120">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="79624-120">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="79624-121">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="79624-121">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="79624-122">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="79624-122">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="79624-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="79624-123">Requirements</span></span>



| <span data-ttu-id="79624-124">需求</span><span class="sxs-lookup"><span data-stu-id="79624-124">Requirement</span></span> | <span data-ttu-id="79624-125">值</span><span class="sxs-lookup"><span data-stu-id="79624-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79624-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79624-126">Minimum supported client</span></span><br/> | <span data-ttu-id="79624-127">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79624-127">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="79624-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79624-128">Minimum supported server</span></span><br/> | <span data-ttu-id="79624-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="79624-129">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="79624-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="79624-130">Namespace</span></span><br/>                | <span data-ttu-id="79624-131">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="79624-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="79624-132">MOF</span><span class="sxs-lookup"><span data-stu-id="79624-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="79624-133"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="79624-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="79624-134">DLL</span><span class="sxs-lookup"><span data-stu-id="79624-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79624-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="79624-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="79624-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79624-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79624-137">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="79624-137">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 





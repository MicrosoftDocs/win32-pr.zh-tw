---
description: 抓取有關錯誤的其他資訊。
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Msvm_CollectionReferencePointExportJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c056f7c8a05d8d06d136219fb55699ed5e146bc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992191"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a><span data-ttu-id="f50d8-103">Msvm CollectionReferencePointExportJob 類別的 GetErrorEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f50d8-103">GetErrorEx method of the Msvm\_CollectionReferencePointExportJob class</span></span>

<span data-ttu-id="f50d8-104">抓取有關錯誤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="f50d8-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="f50d8-105">當作業正在執行或已終止而沒有錯誤時， **GetErrorEx** 會傳回沒有 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="f50d8-105">When the job is executing or has terminated without error, **GetErrorEx** returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="f50d8-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止工作，則 **GetErrorEx** 會傳回一或多個 **Msvm \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="f50d8-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more **Msvm\_Error** instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="f50d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="f50d8-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="f50d8-108">參數</span><span class="sxs-lookup"><span data-stu-id="f50d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50d8-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f50d8-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f50d8-110">如果作業的操作狀態不是「確定」，這個參數會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例的陣列。</span><span class="sxs-lookup"><span data-stu-id="f50d8-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="f50d8-111">否則，如果作業為 "OK"，此參數會包含 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f50d8-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f50d8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f50d8-112">Return value</span></span>

<span data-ttu-id="f50d8-113">成功時，會傳回 0;否則，會傳回下列其中一個錯誤值：</span><span class="sxs-lookup"><span data-stu-id="f50d8-113">On success, returns 0; otherwise, returns one of the following error values:</span></span>

<dl> <dt>

<span data-ttu-id="f50d8-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="f50d8-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="f50d8-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="f50d8-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="f50d8-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="f50d8-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="f50d8-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="f50d8-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="f50d8-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="f50d8-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="f50d8-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="f50d8-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f50d8-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="f50d8-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f50d8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f50d8-126">Requirements</span></span>



| <span data-ttu-id="f50d8-127">需求</span><span class="sxs-lookup"><span data-stu-id="f50d8-127">Requirement</span></span> | <span data-ttu-id="f50d8-128">值</span><span class="sxs-lookup"><span data-stu-id="f50d8-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50d8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f50d8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f50d8-130">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f50d8-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f50d8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f50d8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f50d8-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f50d8-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f50d8-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="f50d8-133">Namespace</span></span><br/>                | <span data-ttu-id="f50d8-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="f50d8-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f50d8-135">MOF</span><span class="sxs-lookup"><span data-stu-id="f50d8-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f50d8-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="f50d8-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f50d8-137">DLL</span><span class="sxs-lookup"><span data-stu-id="f50d8-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f50d8-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f50d8-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f50d8-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f50d8-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50d8-140">**Msvm \_ CollectionReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="f50d8-140">**Msvm\_CollectionReferencePointExportJob**</span></span>](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 





---
description: 抓取有關錯誤的其他資訊。
ms.assetid: 63ce4762-e5ce-405f-b5fc-74e505b0eaf1
title: Msvm_VirtualSystemReferencePointExportJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4c6c392adb2b638c2d638b758696252adcb54d7e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106992634"
---
# <a name="geterrorex-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a><span data-ttu-id="ac235-103">Msvm VirtualSystemReferencePointExportJob 類別的 GetErrorEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ac235-103">GetErrorEx method of the Msvm\_VirtualSystemReferencePointExportJob class</span></span>

<span data-ttu-id="ac235-104">抓取有關錯誤的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ac235-104">Retrieves additional information about an error.</span></span> <span data-ttu-id="ac235-105">當作業正在執行或已終止而沒有錯誤時， **GetErrorEx** 會傳回沒有 **GetErrorEx** 實例。</span><span class="sxs-lookup"><span data-stu-id="ac235-105">When the job is executing or has terminated without error, **GetErrorEx** returns no **GetErrorEx** instance.</span></span> <span data-ttu-id="ac235-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止工作，則 **GetErrorEx** 會傳回一或多個 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="ac235-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then **GetErrorEx** returns one or more [**Msvm\_Error**](msvm-error.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac235-107">語法</span><span class="sxs-lookup"><span data-stu-id="ac235-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="ac235-108">參數</span><span class="sxs-lookup"><span data-stu-id="ac235-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac235-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ac235-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ac235-110">如果作業的操作狀態不是「確定」，這個參數會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例的陣列。</span><span class="sxs-lookup"><span data-stu-id="ac235-110">If the operational status of the job is not "OK", this parameter returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="ac235-111">否則，如果作業為 "OK"，此參數會包含 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ac235-111">Otherwise, if the job is "OK", this parameter contains **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac235-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac235-112">Return value</span></span>

<span data-ttu-id="ac235-113">成功時，會傳回 0;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="ac235-113">On success, returns 0; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ac235-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="ac235-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="ac235-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="ac235-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="ac235-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="ac235-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="ac235-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="ac235-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="ac235-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="ac235-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="ac235-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="ac235-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ac235-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="ac235-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ac235-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac235-126">Requirements</span></span>



| <span data-ttu-id="ac235-127">需求</span><span class="sxs-lookup"><span data-stu-id="ac235-127">Requirement</span></span> | <span data-ttu-id="ac235-128">值</span><span class="sxs-lookup"><span data-stu-id="ac235-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac235-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac235-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ac235-130">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac235-130">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ac235-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac235-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ac235-132">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ac235-132">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="ac235-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="ac235-133">Namespace</span></span><br/>                | <span data-ttu-id="ac235-134">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="ac235-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ac235-135">MOF</span><span class="sxs-lookup"><span data-stu-id="ac235-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac235-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="ac235-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac235-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ac235-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac235-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ac235-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ac235-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac235-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac235-140">**Msvm \_ VirtualSystemReferencePointExportJob**</span><span class="sxs-lookup"><span data-stu-id="ac235-140">**Msvm\_VirtualSystemReferencePointExportJob**</span></span>](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 





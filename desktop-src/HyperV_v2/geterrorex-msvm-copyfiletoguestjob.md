---
description: 抓取作業的錯誤物件（如果有的話）。
ms.assetid: 817AF83B-B601-4AE4-AB5B-CFEACB9A7F41
title: Msvm_CopyFileToGuestJob：： GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 179ad3a70a985442d855d447ef4eab955d177f0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971249"
---
# <a name="msvm_copyfiletoguestjobgeterrorex-method"></a><span data-ttu-id="1628d-103">Msvm \_ CopyFileToGuestJob：： GetErrorEx 方法</span><span class="sxs-lookup"><span data-stu-id="1628d-103">Msvm\_CopyFileToGuestJob::GetErrorEx method</span></span>

<span data-ttu-id="1628d-104">抓取作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="1628d-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="1628d-105">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="1628d-105">When the job is executing or has terminated without error, this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="1628d-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="1628d-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="1628d-107">語法</span><span class="sxs-lookup"><span data-stu-id="1628d-107">Syntax</span></span>


```C++
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="1628d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1628d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1628d-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1628d-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1628d-110">如果作業的作業狀態不是 2 (確定) ，這個方法會傳回一或多個 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例（以 CIM XML 格式表示），表示工作中遇到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1628d-110">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="1628d-111">如果作業的操作狀態為 2 (確定) ，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="1628d-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1628d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1628d-112">Return value</span></span>

<span data-ttu-id="1628d-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1628d-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1628d-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="1628d-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="1628d-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="1628d-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="1628d-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="1628d-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="1628d-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="1628d-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="1628d-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="1628d-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="1628d-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="1628d-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="1628d-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="1628d-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1628d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1628d-126">Requirements</span></span>



| <span data-ttu-id="1628d-127">需求</span><span class="sxs-lookup"><span data-stu-id="1628d-127">Requirement</span></span> | <span data-ttu-id="1628d-128">值</span><span class="sxs-lookup"><span data-stu-id="1628d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1628d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1628d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1628d-130">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1628d-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1628d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1628d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1628d-132">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1628d-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1628d-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="1628d-133">Namespace</span></span><br/>                | <span data-ttu-id="1628d-134">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="1628d-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="1628d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="1628d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1628d-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="1628d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1628d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1628d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1628d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1628d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1628d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1628d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1628d-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="1628d-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 





---
description: Msvm_CopyFileToGuestJob：： GetError 方法-抓取作業的錯誤物件（如果有的話）。
ms.assetid: 478E9170-A523-4CE1-BD97-57D713FAF71B
title: Msvm_CopyFileToGuestJob：： GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7cecaf7254788ae064ca42f2ae0c26e8ad83d7e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119366"
---
# <a name="msvm_copyfiletoguestjobgeterror-method"></a><span data-ttu-id="e683e-103">Msvm \_ CopyFileToGuestJob：： GetError 方法</span><span class="sxs-lookup"><span data-stu-id="e683e-103">Msvm\_CopyFileToGuestJob::GetError method</span></span>

<span data-ttu-id="e683e-104">抓取作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e683e-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="e683e-105">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="e683e-105">When the job is executing or has terminated without error, this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="e683e-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回 **CIM \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="e683e-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="e683e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e683e-107">Syntax</span></span>


```C++
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="e683e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e683e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e683e-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e683e-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e683e-110">如果作業的作業狀態不是 2 (確定) ，這個方法會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例（採用 CIM XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="e683e-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="e683e-111">如果作業的操作狀態為 2 (確定) ，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="e683e-111">If the operational status of the job is 2 (OK), **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e683e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e683e-112">Return value</span></span>

<span data-ttu-id="e683e-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e683e-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e683e-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e683e-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e683e-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e683e-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e683e-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e683e-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e683e-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e683e-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="e683e-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e683e-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e683e-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e683e-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e683e-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e683e-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e683e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e683e-126">Requirements</span></span>



| <span data-ttu-id="e683e-127">需求</span><span class="sxs-lookup"><span data-stu-id="e683e-127">Requirement</span></span> | <span data-ttu-id="e683e-128">值</span><span class="sxs-lookup"><span data-stu-id="e683e-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e683e-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e683e-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e683e-130">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e683e-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e683e-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e683e-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e683e-132">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e683e-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e683e-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="e683e-133">Namespace</span></span><br/>                | <span data-ttu-id="e683e-134">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e683e-134">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="e683e-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e683e-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e683e-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e683e-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e683e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e683e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e683e-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e683e-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e683e-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e683e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e683e-140">**Msvm \_ CopyFileToGuestJob**</span><span class="sxs-lookup"><span data-stu-id="e683e-140">**Msvm\_CopyFileToGuestJob**</span></span>](msvm-copyfiletoguestjob.md)
</dt> </dl>

 


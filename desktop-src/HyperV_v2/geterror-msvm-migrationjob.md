---
description: 抓取遷移作業的錯誤物件（如果有的話）。
ms.assetid: 83a68ded-086a-42d9-b76d-e46af70d9b43
title: Msvm_MigrationJob 類別的 GetError 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6dce1cb3728c854b1dac742099a3ca035d4865a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973492"
---
# <a name="geterror-method-of-the-msvm_migrationjob-class"></a><span data-ttu-id="af182-103">Msvm MigrationJob 類別的 GetError 方法 \_</span><span class="sxs-lookup"><span data-stu-id="af182-103">GetError method of the Msvm\_MigrationJob class</span></span>

<span data-ttu-id="af182-104">抓取遷移作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="af182-104">Retrieves the error object for the migration job, if one exists.</span></span> <span data-ttu-id="af182-105">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**CIM \_ 錯誤**](/previous-versions//cc150671(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="af182-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="af182-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回 **CIM \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="af182-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="af182-107">語法</span><span class="sxs-lookup"><span data-stu-id="af182-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="af182-108">參數</span><span class="sxs-lookup"><span data-stu-id="af182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af182-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="af182-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="af182-110">如果作業的作業狀態不是 2 (確定) ，這個方法會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例（採用 CIM XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="af182-110">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="af182-111">如果作業的操作狀態為 2 (確定) ，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="af182-111">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af182-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="af182-112">Return value</span></span>

<span data-ttu-id="af182-113">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="af182-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="af182-114">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="af182-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="af182-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="af182-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="af182-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="af182-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="af182-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="af182-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="af182-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="af182-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="af182-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="af182-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="af182-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="af182-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="af182-121">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="af182-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="af182-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="af182-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="af182-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="af182-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="af182-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="af182-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="af182-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="af182-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="af182-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="af182-126">Requirements</span></span>



| <span data-ttu-id="af182-127">需求</span><span class="sxs-lookup"><span data-stu-id="af182-127">Requirement</span></span> | <span data-ttu-id="af182-128">值</span><span class="sxs-lookup"><span data-stu-id="af182-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af182-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="af182-129">Minimum supported client</span></span><br/> | <span data-ttu-id="af182-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af182-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af182-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="af182-131">Minimum supported server</span></span><br/> | <span data-ttu-id="af182-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="af182-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af182-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="af182-133">Namespace</span></span><br/>                | <span data-ttu-id="af182-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="af182-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af182-135">MOF</span><span class="sxs-lookup"><span data-stu-id="af182-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af182-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="af182-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af182-137">DLL</span><span class="sxs-lookup"><span data-stu-id="af182-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af182-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af182-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af182-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="af182-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af182-140">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="af182-140">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)
</dt> </dl>

 


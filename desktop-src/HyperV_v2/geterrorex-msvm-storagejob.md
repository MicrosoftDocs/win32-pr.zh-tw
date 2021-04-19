---
description: 當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 Msvm \_ 錯誤實例。
ms.assetid: 119E7EFD-78C9-46F1-8A53-C51A7A34B32E
title: Msvm_StorageJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26d5aff37631de00cffccd49cf54f0ba09ce5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973867"
---
# <a name="geterrorex-method-of-the-msvm_storagejob-class"></a><span data-ttu-id="822bf-103">Msvm Get-storagejob 類別的 GetErrorEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="822bf-103">GetErrorEx method of the Msvm\_StorageJob class</span></span>

<span data-ttu-id="822bf-104">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="822bf-104">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="822bf-105">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="822bf-105">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="822bf-106">語法</span><span class="sxs-lookup"><span data-stu-id="822bf-106">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="822bf-107">參數</span><span class="sxs-lookup"><span data-stu-id="822bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822bf-108">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="822bf-108">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="822bf-109">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="822bf-109">Type: **string\[\]**</span></span>

<span data-ttu-id="822bf-110">如果作業的操作狀態不是「確定」，這個方法會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例的陣列。</span><span class="sxs-lookup"><span data-stu-id="822bf-110">If the operational status of the job is not "OK", this method returns an array of [**Msvm\_Error**](msvm-error.md) instances.</span></span> <span data-ttu-id="822bf-111">否則，如果作業是「確定」，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="822bf-111">Otherwise, if the job is "OK", **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822bf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="822bf-112">Return value</span></span>

<span data-ttu-id="822bf-113">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="822bf-113">Type: **uint32**</span></span>

<span data-ttu-id="822bf-114">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="822bf-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="822bf-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="822bf-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-116">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="822bf-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-117">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="822bf-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-118">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="822bf-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-119">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="822bf-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-120">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="822bf-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-121">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="822bf-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-122">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="822bf-122">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-123">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="822bf-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-124">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="822bf-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-125">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="822bf-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="822bf-126">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="822bf-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="822bf-127">備註</span><span class="sxs-lookup"><span data-stu-id="822bf-127">Remarks</span></span>

<span data-ttu-id="822bf-128">存取 [**Msvm \_ get-storagejob**](msvm-storagejob.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="822bf-128">Access to the [**Msvm\_StorageJob**](msvm-storagejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="822bf-129">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="822bf-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="822bf-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="822bf-130">Requirements</span></span>



| <span data-ttu-id="822bf-131">需求</span><span class="sxs-lookup"><span data-stu-id="822bf-131">Requirement</span></span> | <span data-ttu-id="822bf-132">值</span><span class="sxs-lookup"><span data-stu-id="822bf-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="822bf-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="822bf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="822bf-134">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822bf-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="822bf-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="822bf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="822bf-136">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="822bf-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="822bf-137">命名空間</span><span class="sxs-lookup"><span data-stu-id="822bf-137">Namespace</span></span><br/>                | <span data-ttu-id="822bf-138">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="822bf-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="822bf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="822bf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="822bf-140"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="822bf-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="822bf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="822bf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="822bf-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="822bf-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="822bf-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="822bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822bf-144">**Msvm \_ get-storagejob**</span><span class="sxs-lookup"><span data-stu-id="822bf-144">**Msvm\_StorageJob**</span></span>](msvm-storagejob.md)
</dt> </dl>

 


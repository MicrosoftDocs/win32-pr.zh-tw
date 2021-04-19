---
description: 抓取作業的錯誤物件（如果有的話）。
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Msvm_ConcreteJob 類別的 GetErrorEx 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e938d41afad430051bebb08fc77d6edf6da44691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970631"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="a28b7-103">Msvm ConcreteJob 類別的 GetErrorEx 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a28b7-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="a28b7-104">抓取作業的錯誤物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a28b7-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="a28b7-105">當作業正在執行或已終止但沒有錯誤時，此方法不會傳回 [**Msvm \_ 錯誤**](msvm-error.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="a28b7-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="a28b7-106">但是，如果工作因為某些內部問題而失敗，或由於用戶端已終止作業，則會傳回一或多個 **Msvm \_ 錯誤** 實例。</span><span class="sxs-lookup"><span data-stu-id="a28b7-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="a28b7-107">語法</span><span class="sxs-lookup"><span data-stu-id="a28b7-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="a28b7-108">參數</span><span class="sxs-lookup"><span data-stu-id="a28b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28b7-109">*錯誤* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a28b7-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a28b7-110">類型：**字串 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="a28b7-110">Type: **string\[\]**</span></span>

<span data-ttu-id="a28b7-111">如果作業的作業狀態不是 2 (確定) ，這個方法會傳回一或多個 [**Msvm \_ 錯誤**](msvm-error.md) 類別的內嵌實例（以 CIM XML 格式表示），表示工作中遇到的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a28b7-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="a28b7-112">如果作業的操作狀態為 2 (確定) ，則會傳回 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="a28b7-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28b7-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a28b7-113">Return value</span></span>

<span data-ttu-id="a28b7-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="a28b7-114">Type: **uint32**</span></span>

<span data-ttu-id="a28b7-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a28b7-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a28b7-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="a28b7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="a28b7-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="a28b7-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="a28b7-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="a28b7-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="a28b7-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="a28b7-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-123">**System 使用** (32774) </span><span class="sxs-lookup"><span data-stu-id="a28b7-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="a28b7-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="a28b7-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="a28b7-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a28b7-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="a28b7-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a28b7-128">備註</span><span class="sxs-lookup"><span data-stu-id="a28b7-128">Remarks</span></span>

<span data-ttu-id="a28b7-129">存取 [**Msvm \_ ConcreteJob**](msvm-concretejob.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="a28b7-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a28b7-130">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="a28b7-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a28b7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28b7-131">Requirements</span></span>



| <span data-ttu-id="a28b7-132">需求</span><span class="sxs-lookup"><span data-stu-id="a28b7-132">Requirement</span></span> | <span data-ttu-id="a28b7-133">值</span><span class="sxs-lookup"><span data-stu-id="a28b7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a28b7-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a28b7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a28b7-135">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28b7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a28b7-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a28b7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a28b7-137">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28b7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a28b7-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="a28b7-138">Namespace</span></span><br/>                | <span data-ttu-id="a28b7-139">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="a28b7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a28b7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a28b7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a28b7-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="a28b7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a28b7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a28b7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a28b7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a28b7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a28b7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28b7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28b7-145">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="a28b7-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 


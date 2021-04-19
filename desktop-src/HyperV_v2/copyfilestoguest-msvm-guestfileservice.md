---
description: 將檔案從 Hyper-v 主機複製到虛擬機器。
ms.assetid: 76667557-13B2-4286-BC6B-E32FADE62A7A
title: Msvm_GuestFileService：： CopyFilesToGuest 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestFileService.CopyFilesToGuest
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9424dee6d28e0bd9cd6ac43c15ad27cdebdb7017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981006"
---
# <a name="msvm_guestfileservicecopyfilestoguest-method"></a><span data-ttu-id="6e9a9-103">Msvm \_ GuestFileService：： CopyFilesToGuest 方法</span><span class="sxs-lookup"><span data-stu-id="6e9a9-103">Msvm\_GuestFileService::CopyFilesToGuest method</span></span>

<span data-ttu-id="6e9a9-104">將檔案從 Hyper-v 主機複製到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-104">Copies files from the Hyper-V host to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9a9-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e9a9-105">Syntax</span></span>


```C++
uint32 CopyFilesToGuest(
  [in]            string                  CopyFileToGuestSettings[],
  [out]           CIM_ConcreteJob     Job,
  [out, optional] Msvm_CopyFileToGuestJob ParentPools[]
);
```



## <a name="parameters"></a><span data-ttu-id="6e9a9-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e9a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e9a9-107">*CopyFileToGuestSettings* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-107">*CopyFileToGuestSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e9a9-108">[**Msvm \_ CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)類別的實例陣列，代表「來賓檔案」服務作業。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-108">An array of instances of the [**Msvm\_CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md) class that represents a guest file service operation job.</span></span>

</dd> <dt>

<span data-ttu-id="6e9a9-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6e9a9-110">用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="6e9a9-111">如果作業是以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="6e9a9-112">此參數已在 Windows 10 中新增。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-112">This parameter was added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="6e9a9-113">*ParentPools* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-113">*ParentPools* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e9a9-114">[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)參考的選擇性陣列，可用來監視作業的進度。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-114">An optional array of [**Msvm\_CopyFileToGuestJob**](msvm-copyfiletoguestjob.md) references that are used for monitoring progress of the operation.</span></span> <span data-ttu-id="6e9a9-115">如果 **CopyFilesToGuest** 無法同步執行，則會使用 *ParentPools* 。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-115">**CopyFilesToGuest** uses *ParentPools* if it can't execute synchronously.</span></span> <span data-ttu-id="6e9a9-116">如果作業以非同步方式執行，則傳回值為4096。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-116">If the operation executes asynchronously, the return value is 4096.</span></span>

> [!Note]  
> <span data-ttu-id="6e9a9-117">此參數已在 Windows 10 中移除。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-117">This parameter was removed in Windows 10.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e9a9-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e9a9-118">Return value</span></span>

<span data-ttu-id="6e9a9-119">成功時，會傳回 0;否則，會傳回錯誤值。</span><span class="sxs-lookup"><span data-stu-id="6e9a9-119">On success, returns 0; otherwise, returns an error value.</span></span>

<dl> <dt>

<span data-ttu-id="6e9a9-120">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-121">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-122">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-123">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-124">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-125">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-126">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-127">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-128">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-129">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-130">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-131">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6e9a9-132">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="6e9a9-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6e9a9-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e9a9-133">Requirements</span></span>



| <span data-ttu-id="6e9a9-134">需求</span><span class="sxs-lookup"><span data-stu-id="6e9a9-134">Requirement</span></span> | <span data-ttu-id="6e9a9-135">值</span><span class="sxs-lookup"><span data-stu-id="6e9a9-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9a9-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e9a9-136">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9a9-137">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-137">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="6e9a9-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e9a9-138">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9a9-139">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e9a9-139">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="6e9a9-140">命名空間</span><span class="sxs-lookup"><span data-stu-id="6e9a9-140">Namespace</span></span><br/>                | <span data-ttu-id="6e9a9-141">\\\\根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="6e9a9-141">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="6e9a9-142">MOF</span><span class="sxs-lookup"><span data-stu-id="6e9a9-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6e9a9-143"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="6e9a9-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6e9a9-144">DLL</span><span class="sxs-lookup"><span data-stu-id="6e9a9-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e9a9-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e9a9-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6e9a9-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e9a9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9a9-147">**Msvm \_ GuestFileService**</span><span class="sxs-lookup"><span data-stu-id="6e9a9-147">**Msvm\_GuestFileService**</span></span>](msvm-guestfileservice.md)
</dt> </dl>

 

 





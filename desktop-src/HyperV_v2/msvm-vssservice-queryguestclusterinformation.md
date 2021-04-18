---
description: 查詢從 Hyper-v 主機到來賓的叢集資訊。
ms.assetid: 28983984-a2af-4eab-8b1f-2f7d6a3d70ea
title: Msvm_VssService 類別的 QueryGuestClusterInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VssService.QueryGuestClusterInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 36f88441729cc1e6e36bcad9ca84b46049bce2a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510988"
---
# <a name="queryguestclusterinformation-method-of-the-msvm_vssservice-class"></a><span data-ttu-id="02487-103">Msvm VssService 類別的 QueryGuestClusterInformation 方法 \_</span><span class="sxs-lookup"><span data-stu-id="02487-103">QueryGuestClusterInformation method of the Msvm\_VssService class</span></span>

<span data-ttu-id="02487-104">查詢從 Hyper-v 主機到來賓的叢集資訊。</span><span class="sxs-lookup"><span data-stu-id="02487-104">Querying cluster information from the Hyper-V host to the guest.</span></span>

## <a name="syntax"></a><span data-ttu-id="02487-105">語法</span><span class="sxs-lookup"><span data-stu-id="02487-105">Syntax</span></span>


```mof
uint32 QueryGuestClusterInformation(
  [out] Msvm_GuestClusterInformation GuestClusterInformation
);
```



## <a name="parameters"></a><span data-ttu-id="02487-106">參數</span><span class="sxs-lookup"><span data-stu-id="02487-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02487-107">*GuestClusterInformation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="02487-107">*GuestClusterInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02487-108">成功時，會包含描述來賓叢集的 [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md) 。</span><span class="sxs-lookup"><span data-stu-id="02487-108">On success, contains an [**Msvm\_GuestClusterInformation**](msvm-guestclusterinformation.md) that describes the guest cluster.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02487-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="02487-109">Return value</span></span>

<span data-ttu-id="02487-110">成功時，會傳回 0 (完成，沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="02487-110">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="02487-111">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="02487-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="02487-112">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="02487-112">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="02487-113">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="02487-113">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="02487-114">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="02487-114">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="02487-115">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="02487-115">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="02487-116">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="02487-116">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="02487-117">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="02487-117">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="02487-118">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="02487-118">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="02487-119">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="02487-119">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="02487-120">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="02487-120">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="02487-121">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="02487-121">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="02487-122">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="02487-122">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="02487-123">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="02487-123">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="02487-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="02487-124">Requirements</span></span>



| <span data-ttu-id="02487-125">需求</span><span class="sxs-lookup"><span data-stu-id="02487-125">Requirement</span></span> | <span data-ttu-id="02487-126">值</span><span class="sxs-lookup"><span data-stu-id="02487-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02487-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02487-127">Minimum supported client</span></span><br/> | <span data-ttu-id="02487-128">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02487-128">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="02487-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02487-129">Minimum supported server</span></span><br/> | <span data-ttu-id="02487-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="02487-130">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="02487-131">命名空間</span><span class="sxs-lookup"><span data-stu-id="02487-131">Namespace</span></span><br/>                | <span data-ttu-id="02487-132">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="02487-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02487-133">MOF</span><span class="sxs-lookup"><span data-stu-id="02487-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02487-134"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="02487-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02487-135">DLL</span><span class="sxs-lookup"><span data-stu-id="02487-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02487-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02487-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02487-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02487-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02487-138">**Msvm \_ VssService**</span><span class="sxs-lookup"><span data-stu-id="02487-138">**Msvm\_VssService**</span></span>](msvm-vssservice.md)
</dt> </dl>

 

 





---
description: 修改 Hyper-v 複本服務的設定。
ms.assetid: e203f9f5-da4b-4ba7-8637-add7169990d3
title: Msvm_ReplicationService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe20f8e6f113dce05961eb11fbafdc7841f39e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690784"
---
# <a name="modifyservicesettings-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="e5d20-103">Msvm ReplicationService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="e5d20-103">ModifyServiceSettings method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="e5d20-104">修改 Hyper-v 複本服務的設定。</span><span class="sxs-lookup"><span data-stu-id="e5d20-104">Modifies the settings for the Hyper-V Replica service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5d20-105">語法</span><span class="sxs-lookup"><span data-stu-id="e5d20-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="e5d20-106">參數</span><span class="sxs-lookup"><span data-stu-id="e5d20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5d20-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e5d20-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d20-108">[**Msvm \_ ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md)類別的字串表示，其中包含服務已修改的設定資料。</span><span class="sxs-lookup"><span data-stu-id="e5d20-108">A string representation of the [**Msvm\_ReplicationServiceSettingData**](msvm-replicationservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="e5d20-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e5d20-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5d20-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="e5d20-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5d20-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e5d20-111">Return value</span></span>

<span data-ttu-id="e5d20-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e5d20-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e5d20-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="e5d20-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="e5d20-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="e5d20-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="e5d20-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="e5d20-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="e5d20-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="e5d20-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="e5d20-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="e5d20-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="e5d20-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="e5d20-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="e5d20-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e5d20-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="e5d20-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e5d20-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5d20-126">Requirements</span></span>



| <span data-ttu-id="e5d20-127">需求</span><span class="sxs-lookup"><span data-stu-id="e5d20-127">Requirement</span></span> | <span data-ttu-id="e5d20-128">值</span><span class="sxs-lookup"><span data-stu-id="e5d20-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d20-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5d20-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e5d20-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5d20-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e5d20-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e5d20-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e5d20-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e5d20-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e5d20-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="e5d20-133">Namespace</span></span><br/>                | <span data-ttu-id="e5d20-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="e5d20-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e5d20-135">MOF</span><span class="sxs-lookup"><span data-stu-id="e5d20-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5d20-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="e5d20-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5d20-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e5d20-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5d20-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5d20-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5d20-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5d20-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5d20-140">**Msvm \_ ReplicationService**</span><span class="sxs-lookup"><span data-stu-id="e5d20-140">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 


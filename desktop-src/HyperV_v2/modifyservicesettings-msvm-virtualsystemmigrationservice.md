---
description: 修改遷移服務的設定資料。
ms.assetid: 5162fe88-dd39-4fe0-b8e9-e9b70c2b6a5c
title: Msvm_VirtualSystemMigrationService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e1e9dc96196752ec4408939adc418e7c43bc0c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979269"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="28696-103">Msvm VirtualSystemMigrationService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="28696-103">ModifyServiceSettings method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="28696-104">修改遷移服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="28696-104">Modifies the setting data for the migration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="28696-105">語法</span><span class="sxs-lookup"><span data-stu-id="28696-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="28696-106">參數</span><span class="sxs-lookup"><span data-stu-id="28696-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28696-107">*ServiceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28696-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28696-108">包含新服務設定之 [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) 類別的內嵌實例。</span><span class="sxs-lookup"><span data-stu-id="28696-108">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the new service settings.</span></span>

</dd> <dt>

<span data-ttu-id="28696-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="28696-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28696-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="28696-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28696-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="28696-111">Return value</span></span>

<span data-ttu-id="28696-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="28696-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="28696-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="28696-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="28696-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="28696-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="28696-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="28696-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="28696-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="28696-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="28696-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="28696-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="28696-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="28696-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="28696-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="28696-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="28696-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="28696-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="28696-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="28696-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="28696-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="28696-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="28696-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="28696-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="28696-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="28696-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="28696-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="28696-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="28696-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="28696-126">Requirements</span></span>



| <span data-ttu-id="28696-127">需求</span><span class="sxs-lookup"><span data-stu-id="28696-127">Requirement</span></span> | <span data-ttu-id="28696-128">值</span><span class="sxs-lookup"><span data-stu-id="28696-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28696-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28696-129">Minimum supported client</span></span><br/> | <span data-ttu-id="28696-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28696-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="28696-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28696-131">Minimum supported server</span></span><br/> | <span data-ttu-id="28696-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="28696-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="28696-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="28696-133">Namespace</span></span><br/>                | <span data-ttu-id="28696-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="28696-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="28696-135">MOF</span><span class="sxs-lookup"><span data-stu-id="28696-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="28696-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="28696-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="28696-137">DLL</span><span class="sxs-lookup"><span data-stu-id="28696-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28696-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="28696-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="28696-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28696-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28696-140">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="28696-140">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 


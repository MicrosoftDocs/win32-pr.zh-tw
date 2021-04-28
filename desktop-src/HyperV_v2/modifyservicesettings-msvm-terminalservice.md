---
description: Msvm_TerminalService 類別的 ModifyServiceSettings 方法-修改服務的設定資料。
ms.assetid: 76669180-fa95-4d6e-b89a-53e45da664c4
title: Msvm_TerminalService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 930b29c5c07c755b493a0aabad88ae776c0803e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119326"
---
# <a name="modifyservicesettings-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="8a582-103">Msvm TerminalService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8a582-103">ModifyServiceSettings method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="8a582-104">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="8a582-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a582-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a582-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              ServiceSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="8a582-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a582-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a582-107">*ServiceSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a582-107">*ServiceSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a582-108">[**Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md)類別的字串表示，其中包含服務已修改的設定資料。</span><span class="sxs-lookup"><span data-stu-id="8a582-108">A string representation of the [**Msvm\_TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="8a582-109">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8a582-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a582-110">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="8a582-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a582-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a582-111">Return value</span></span>

<span data-ttu-id="8a582-112">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8a582-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="8a582-113">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="8a582-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-114">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="8a582-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-115">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="8a582-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-116">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="8a582-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-117">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="8a582-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-118">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="8a582-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-119">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="8a582-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-120">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="8a582-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-121">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="8a582-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-122">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="8a582-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-123">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="8a582-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-124">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="8a582-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="8a582-125">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="8a582-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8a582-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a582-126">Requirements</span></span>



| <span data-ttu-id="8a582-127">需求</span><span class="sxs-lookup"><span data-stu-id="8a582-127">Requirement</span></span> | <span data-ttu-id="8a582-128">值</span><span class="sxs-lookup"><span data-stu-id="8a582-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a582-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a582-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a582-130">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a582-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a582-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a582-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a582-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a582-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a582-133">命名空間</span><span class="sxs-lookup"><span data-stu-id="8a582-133">Namespace</span></span><br/>                | <span data-ttu-id="8a582-134">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="8a582-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a582-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8a582-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a582-136"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="8a582-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a582-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8a582-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a582-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a582-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8a582-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a582-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a582-140">**Msvm \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="8a582-140">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 


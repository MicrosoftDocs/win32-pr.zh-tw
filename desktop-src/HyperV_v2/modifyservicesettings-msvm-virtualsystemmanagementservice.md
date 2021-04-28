---
description: Msvm_VirtualSystemManagementService 類別的 ModifyServiceSettings 方法-修改服務的設定資料。
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Msvm_VirtualSystemManagementService 類別的 ModifyServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee4e8ae904292bae06770f23cf6c853d5e5448bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112166"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="bf711-103">Msvm VirtualSystemManagementService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="bf711-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="bf711-104">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="bf711-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf711-105">語法</span><span class="sxs-lookup"><span data-stu-id="bf711-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bf711-106">參數</span><span class="sxs-lookup"><span data-stu-id="bf711-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf711-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bf711-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf711-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="bf711-108">Type: **string**</span></span>

<span data-ttu-id="bf711-109">[**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的內嵌實例，其中包含現有服務的修改方面。</span><span class="sxs-lookup"><span data-stu-id="bf711-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="bf711-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bf711-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf711-111">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="bf711-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="bf711-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bf711-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf711-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bf711-113">Return value</span></span>

<span data-ttu-id="bf711-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf711-114">Type: **uint32**</span></span>

<span data-ttu-id="bf711-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bf711-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bf711-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="bf711-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="bf711-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="bf711-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="bf711-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="bf711-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="bf711-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="bf711-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="bf711-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="bf711-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="bf711-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="bf711-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="bf711-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bf711-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="bf711-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bf711-129">備註</span><span class="sxs-lookup"><span data-stu-id="bf711-129">Remarks</span></span>

<span data-ttu-id="bf711-130">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="bf711-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bf711-131">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="bf711-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf711-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf711-132">Requirements</span></span>



| <span data-ttu-id="bf711-133">需求</span><span class="sxs-lookup"><span data-stu-id="bf711-133">Requirement</span></span> | <span data-ttu-id="bf711-134">值</span><span class="sxs-lookup"><span data-stu-id="bf711-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf711-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf711-135">Minimum supported client</span></span><br/> | <span data-ttu-id="bf711-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf711-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bf711-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf711-137">Minimum supported server</span></span><br/> | <span data-ttu-id="bf711-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf711-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf711-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="bf711-139">Namespace</span></span><br/>                | <span data-ttu-id="bf711-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="bf711-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bf711-141">MOF</span><span class="sxs-lookup"><span data-stu-id="bf711-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bf711-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="bf711-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bf711-143">DLL</span><span class="sxs-lookup"><span data-stu-id="bf711-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf711-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bf711-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bf711-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf711-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf711-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="bf711-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="bf711-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="bf711-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="bf711-148">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bf711-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 


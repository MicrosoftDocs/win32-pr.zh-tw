---
description: 修改服務的設定資料。
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
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850943"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="7d8e0-103">Msvm VirtualSystemManagementService 類別的 ModifyServiceSettings 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7d8e0-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="7d8e0-104">修改服務的設定資料。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d8e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="7d8e0-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7d8e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="7d8e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d8e0-107">*SettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7d8e0-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8e0-108">類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-108">Type: **string**</span></span>

<span data-ttu-id="7d8e0-109">[**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md)類別的內嵌實例，其中包含現有服務的修改方面。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="7d8e0-110">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7d8e0-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7d8e0-111">類型： **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="7d8e0-112">如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d8e0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7d8e0-113">Return value</span></span>

<span data-ttu-id="7d8e0-114">類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-114">Type: **uint32**</span></span>

<span data-ttu-id="7d8e0-115">這個方法會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7d8e0-116">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-117">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-118">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-119">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-120">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-121">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-122">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-123">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-124">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-125">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-126">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-127">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7d8e0-128">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="7d8e0-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7d8e0-129">備註</span><span class="sxs-lookup"><span data-stu-id="7d8e0-129">Remarks</span></span>

<span data-ttu-id="7d8e0-130">存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7d8e0-131">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。</span><span class="sxs-lookup"><span data-stu-id="7d8e0-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d8e0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d8e0-132">Requirements</span></span>



| <span data-ttu-id="7d8e0-133">需求</span><span class="sxs-lookup"><span data-stu-id="7d8e0-133">Requirement</span></span> | <span data-ttu-id="7d8e0-134">值</span><span class="sxs-lookup"><span data-stu-id="7d8e0-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d8e0-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7d8e0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7d8e0-136">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d8e0-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d8e0-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7d8e0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7d8e0-138">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7d8e0-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d8e0-139">命名空間</span><span class="sxs-lookup"><span data-stu-id="7d8e0-139">Namespace</span></span><br/>                | <span data-ttu-id="7d8e0-140">根 \\ 虛擬化 \\ V2</span><span class="sxs-lookup"><span data-stu-id="7d8e0-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d8e0-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7d8e0-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d8e0-142"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e0-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d8e0-143">DLL</span><span class="sxs-lookup"><span data-stu-id="7d8e0-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d8e0-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d8e0-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d8e0-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d8e0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d8e0-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="7d8e0-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="7d8e0-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="7d8e0-148">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d8e0-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 


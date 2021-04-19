---
description: 卸載指定的 PCI 裝置，讓它可以指派。
ms.assetid: 8ea3bc27-93ba-4db8-a4aa-cdfea225eaa9
title: Msvm_AssignableDeviceService 類別的 DismountAssignableDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.DismountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 53036cd09113430d1045c8e9eae7a8d782b35960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975166"
---
# <a name="dismountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="d529e-103">Msvm AssignableDeviceService 類別的 DismountAssignableDevice 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d529e-103">DismountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="d529e-104">卸載指定的 PCI 裝置，讓它可以指派。</span><span class="sxs-lookup"><span data-stu-id="d529e-104">Dismounts the specified PCI device so that it can be assigned.</span></span>

## <a name="syntax"></a><span data-ttu-id="d529e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d529e-105">Syntax</span></span>


```mof
uint32 DismountAssignableDevice(
  [in]  string              DismountSettingData,
  [out] string              DismountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d529e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d529e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d529e-107">*DismountSettingData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d529e-107">*DismountSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d529e-108">設定資料物件的內嵌實例，這個物件會指定要卸載的 PCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="d529e-108">Embedded instance of a setting data object that specifies the PCI device to dismount.</span></span>

</dd> <dt>

<span data-ttu-id="d529e-109">*DismountedDeviceInstancePath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d529e-109">*DismountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d529e-110">包含已卸載裝置之裝置實例路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="d529e-110">String containing the device instance path to the dismounted device.</span></span>

</dd> <dt>

<span data-ttu-id="d529e-111">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d529e-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d529e-112">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="d529e-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d529e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d529e-113">Return value</span></span>

<span data-ttu-id="d529e-114">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d529e-114">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="d529e-115">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="d529e-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-116">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="d529e-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-117">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="d529e-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-118">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="d529e-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-119">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="d529e-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-120">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="d529e-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-121">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="d529e-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-122">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="d529e-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-123">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="d529e-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-124">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="d529e-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-125">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="d529e-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-126">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="d529e-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-127">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="d529e-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="d529e-128">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="d529e-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d529e-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d529e-129">Requirements</span></span>



| <span data-ttu-id="d529e-130">需求</span><span class="sxs-lookup"><span data-stu-id="d529e-130">Requirement</span></span> | <span data-ttu-id="d529e-131">值</span><span class="sxs-lookup"><span data-stu-id="d529e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d529e-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d529e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d529e-133">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d529e-133">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="d529e-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d529e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d529e-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d529e-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d529e-136">命名空間</span><span class="sxs-lookup"><span data-stu-id="d529e-136">Namespace</span></span><br/>                | <span data-ttu-id="d529e-137">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="d529e-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d529e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d529e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d529e-139"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="d529e-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d529e-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d529e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d529e-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d529e-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d529e-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d529e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d529e-143">**Msvm \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="d529e-143">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 





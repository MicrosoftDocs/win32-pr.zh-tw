---
description: 裝載指定的 PCI 裝置，使其可供主機電腦系統使用。
ms.assetid: 2a07174e-c221-4c04-81b8-5968aa67e235
title: Msvm_AssignableDeviceService 類別的 MountAssignableDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AssignableDeviceService.MountAssignableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: df5f8a337fbf4baf47a4f695322944ed0b97e82e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996819"
---
# <a name="mountassignabledevice-method-of-the-msvm_assignabledeviceservice-class"></a><span data-ttu-id="b3c22-103">Msvm AssignableDeviceService 類別的 MountAssignableDevice 方法 \_</span><span class="sxs-lookup"><span data-stu-id="b3c22-103">MountAssignableDevice method of the Msvm\_AssignableDeviceService class</span></span>

<span data-ttu-id="b3c22-104">裝載指定的 PCI 裝置，使其可供主機電腦系統使用。</span><span class="sxs-lookup"><span data-stu-id="b3c22-104">Mounts the specified PCI device so that it can be used by the host computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c22-105">語法</span><span class="sxs-lookup"><span data-stu-id="b3c22-105">Syntax</span></span>


```mof
uint32 MountAssignableDevice(
  [in]  string              DeviceInstancePath,
  [in]  string              DeviceLocationPath,
  [out] string              MountedDeviceInstancePath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b3c22-106">參數</span><span class="sxs-lookup"><span data-stu-id="b3c22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c22-107">*DeviceInstancePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3c22-107">*DeviceInstancePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c22-108">包含裝置之裝置實例路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="b3c22-108">String containing the device instance path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="b3c22-109">*DeviceLocationPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b3c22-109">*DeviceLocationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c22-110">字串，包含裝置的裝置位置路徑。</span><span class="sxs-lookup"><span data-stu-id="b3c22-110">String containing the device location path to a device.</span></span>

</dd> <dt>

<span data-ttu-id="b3c22-111">*MountedDeviceInstancePath* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3c22-111">*MountedDeviceInstancePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c22-112">包含掛接裝置之裝置實例路徑的字串。</span><span class="sxs-lookup"><span data-stu-id="b3c22-112">String containing the device instance path to the mounted device.</span></span>

</dd> <dt>

<span data-ttu-id="b3c22-113">*作業* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b3c22-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c22-114">如果工作已完成) ，則作業 (的參考可以是 null。</span><span class="sxs-lookup"><span data-stu-id="b3c22-114">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c22-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="b3c22-115">Return value</span></span>

<span data-ttu-id="b3c22-116">成功時，傳回0或 4096;否則，會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b3c22-116">On success, returns 0 or 4096; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="b3c22-117">**已完成，沒有錯誤** (0) </span><span class="sxs-lookup"><span data-stu-id="b3c22-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-118">**已檢查方法參數-工作已啟動** (4096) </span><span class="sxs-lookup"><span data-stu-id="b3c22-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-119">**無法** (32768) </span><span class="sxs-lookup"><span data-stu-id="b3c22-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-120">**拒絕存取** (32769) </span><span class="sxs-lookup"><span data-stu-id="b3c22-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-121">**不支援** (32770) </span><span class="sxs-lookup"><span data-stu-id="b3c22-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-122">**狀態未知** (32771) </span><span class="sxs-lookup"><span data-stu-id="b3c22-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-123">**Timeout** (32772) </span><span class="sxs-lookup"><span data-stu-id="b3c22-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-124">**不正確參數** (32773) </span><span class="sxs-lookup"><span data-stu-id="b3c22-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-125">**系統正在使用中** (32774) </span><span class="sxs-lookup"><span data-stu-id="b3c22-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-126">**此操作的狀態無效** (32775) </span><span class="sxs-lookup"><span data-stu-id="b3c22-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-127">**不正確的資料類型** (32776) </span><span class="sxs-lookup"><span data-stu-id="b3c22-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-128">**系統無法使用** (32777) </span><span class="sxs-lookup"><span data-stu-id="b3c22-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-129">**記憶體不足** (32778) </span><span class="sxs-lookup"><span data-stu-id="b3c22-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b3c22-130">**找不到** 檔案 (32779) </span><span class="sxs-lookup"><span data-stu-id="b3c22-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b3c22-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3c22-131">Requirements</span></span>



| <span data-ttu-id="b3c22-132">需求</span><span class="sxs-lookup"><span data-stu-id="b3c22-132">Requirement</span></span> | <span data-ttu-id="b3c22-133">值</span><span class="sxs-lookup"><span data-stu-id="b3c22-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c22-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3c22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c22-135">Windows 10， \[ 僅限1703版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3c22-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b3c22-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3c22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c22-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b3c22-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b3c22-138">命名空間</span><span class="sxs-lookup"><span data-stu-id="b3c22-138">Namespace</span></span><br/>                | <span data-ttu-id="b3c22-139">根 \\ 虛擬化 \\ v2</span><span class="sxs-lookup"><span data-stu-id="b3c22-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b3c22-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b3c22-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3c22-141"><dt>WindowsVirtualization。</dt></span><span class="sxs-lookup"><span data-stu-id="b3c22-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3c22-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c22-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c22-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b3c22-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b3c22-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3c22-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c22-145">**Msvm \_ AssignableDeviceService**</span><span class="sxs-lookup"><span data-stu-id="b3c22-145">**Msvm\_AssignableDeviceService**</span></span>](msvm-assignabledeviceservice.md)
</dt> </dl>

 

 





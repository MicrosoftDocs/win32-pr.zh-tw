---
description: 定義 IOCTL \_ 儲存區 \_ 管理 \_ 資料 \_ 集 \_ 屬性控制項程式碼的一組動作。
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: 'DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847284"
---
# <a name="device_data_management_set_action"></a><span data-ttu-id="a8161-103">裝置 \_ 資料 \_ 管理 \_ 設定 \_ 動作</span><span class="sxs-lookup"><span data-stu-id="a8161-103">DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION</span></span>

<span data-ttu-id="a8161-104">下列常數值是 **裝置 \_ 資料 \_ 管理 \_ 集合 \_ 動作** 類型的可能值集合，其定義為 **DWORD** 類型。</span><span class="sxs-lookup"><span data-stu-id="a8161-104">The following constant values are the set of possible values for the **DEVICE\_DATA\_MANAGEMENT\_SET\_ACTION** type, which is defined as type **DWORD**.</span></span>

<dl> <dt>

<span data-ttu-id="a8161-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ 無**</span><span class="sxs-lookup"><span data-stu-id="a8161-105"><span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction\_None**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-106">0</span><span class="sxs-lookup"><span data-stu-id="a8161-106">0</span></span>
</dt> <dt>



<span data-ttu-id="a8161-107">未執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-107">No action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**</span><span class="sxs-lookup"><span data-stu-id="a8161-108"><span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction\_Trim**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-109">1</span><span class="sxs-lookup"><span data-stu-id="a8161-109">1</span></span>
</dt> <dt>



<span data-ttu-id="a8161-110">執行 trim 動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-110">A trim action is performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="a8161-111"><span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**DeviceDsmAction\_Notification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-112">2 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000002) </span><span class="sxs-lookup"><span data-stu-id="a8161-112">2 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000002)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-113">會執行通知動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-113">A notification action is performed.</span></span> <span data-ttu-id="a8161-114">這些參數是在 [**裝置 \_ DSM \_ 通知 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a8161-114">The parameters are in a [**DEVICE\_DSM\_NOTIFICATION\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) structure.</span></span> <span data-ttu-id="a8161-115">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-115">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**</span><span class="sxs-lookup"><span data-stu-id="a8161-116"><span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction\_OffloadRead**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-117">3 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000003) </span><span class="sxs-lookup"><span data-stu-id="a8161-117">3 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000003)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-118">執行卸載讀取動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-118">An offload read action is performed.</span></span> <span data-ttu-id="a8161-119">參數位於 [**裝置 \_ DSM 卸載 \_ \_ 讀取 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a8161-119">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_READ\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) structure.</span></span> <span data-ttu-id="a8161-120">輸出位於 [**儲存體卸載 \_ \_ 讀取 \_ 輸出**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a8161-120">The output is in a [**STORAGE\_OFFLOAD\_READ\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) structure.</span></span> <span data-ttu-id="a8161-121">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-121">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="a8161-122">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-122">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**</span><span class="sxs-lookup"><span data-stu-id="a8161-123"><span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction\_OffloadWrite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-124">4</span><span class="sxs-lookup"><span data-stu-id="a8161-124">4</span></span>
</dt> <dt>



<span data-ttu-id="a8161-125">執行卸載寫入動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-125">An offload write action is performed.</span></span> <span data-ttu-id="a8161-126">參數位於 [**裝置 \_ DSM 卸載 \_ \_ 寫入 \_ 參數**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a8161-126">The parameters are in a [**DEVICE\_DSM\_OFFLOAD\_WRITE\_PARAMETERS**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) structure.</span></span> <span data-ttu-id="a8161-127">輸出位於 [**儲存體卸載 \_ \_ 寫入 \_ 輸出**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) 結構中。</span><span class="sxs-lookup"><span data-stu-id="a8161-127">The output is in a [**STORAGE\_OFFLOAD\_WRITE\_OUTPUT**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) structure.</span></span>

<span data-ttu-id="a8161-128">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-128">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction \_ 配置**</span><span class="sxs-lookup"><span data-stu-id="a8161-129"><span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**DeviceDsmAction\_Allocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-130">5 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000005) </span><span class="sxs-lookup"><span data-stu-id="a8161-130">5 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000005)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-131">傳入的第一個資料集範圍會傳回配置點陣圖。</span><span class="sxs-lookup"><span data-stu-id="a8161-131">An allocation bitmap is returned for the first data set range passed in.</span></span> <span data-ttu-id="a8161-132">輸出為 [**裝置 \_ 資料 \_ 集 LB 布建 \_ \_ \_ 狀態**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) 結構。</span><span class="sxs-lookup"><span data-stu-id="a8161-132">The output is in a [**DEVICE\_DATA\_SET\_LB\_PROVISIONING\_STATE**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) structure.</span></span> <span data-ttu-id="a8161-133">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-133">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="a8161-134">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-134">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction \_ 修復**</span><span class="sxs-lookup"><span data-stu-id="a8161-135"><span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**DeviceDsmAction\_Repair**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-136">6 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000006) </span><span class="sxs-lookup"><span data-stu-id="a8161-136">6 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000006)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-137">執行修復動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-137">A repair action is performed.</span></span> <span data-ttu-id="a8161-138">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-138">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="a8161-139">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-139">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction \_ 清除**</span><span class="sxs-lookup"><span data-stu-id="a8161-140"><span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction\_Scrub**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-141">7 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000007) </span><span class="sxs-lookup"><span data-stu-id="a8161-141">7 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000007)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-142">執行清除動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-142">A scrub action is performed.</span></span> <span data-ttu-id="a8161-143">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-143">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="a8161-144">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-144">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a8161-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction \_ 復原**</span><span class="sxs-lookup"><span data-stu-id="a8161-145"><span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**DeviceDsmAction\_Resiliency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8161-146">8 \| **DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000008) </span><span class="sxs-lookup"><span data-stu-id="a8161-146">8 \| **DeviceDsmActionFlag\_NonDestructive** (0x80000008)</span></span>
</dt> <dt>



<span data-ttu-id="a8161-147">執行復原動作。</span><span class="sxs-lookup"><span data-stu-id="a8161-147">A resiliency action is performed.</span></span> <span data-ttu-id="a8161-148">**DeviceDsmActionFlag 非 \_ 破壞** 性 (0x80000000) 是一個位旗標，用來向驅動程式堆疊指出這項作業是不具破壞性的。</span><span class="sxs-lookup"><span data-stu-id="a8161-148">The **DeviceDsmActionFlag\_NonDestructive** (0x80000000) is a bit flag to indicate to the driver stack that this operation is non-destructive.</span></span>

<span data-ttu-id="a8161-149">**Windows 7 和 Windows Server 2008 R2：** 在 Windows 8 和 Windows Server 2012 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="a8161-149">**Windows 7 and Windows Server 2008 R2:** This value is not supported before Windows 8 and Windows Server 2012.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8161-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8161-150">Requirements</span></span>



| <span data-ttu-id="a8161-151">需求</span><span class="sxs-lookup"><span data-stu-id="a8161-151">Requirement</span></span> | <span data-ttu-id="a8161-152">值</span><span class="sxs-lookup"><span data-stu-id="a8161-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8161-153">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8161-153">Minimum supported client</span></span><br/> | <span data-ttu-id="a8161-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a8161-154">Windows 7</span></span><br/>                                                                                      |
| <span data-ttu-id="a8161-155">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8161-155">Minimum supported server</span></span><br/> | <span data-ttu-id="a8161-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a8161-156">Windows Server 2008 R2</span></span><br/>                                                                         |
| <span data-ttu-id="a8161-157">標頭</span><span class="sxs-lookup"><span data-stu-id="a8161-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8161-158"><dt>WinIoCtl (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="a8161-158"><dt>WinIoCtl.h (include Windows.h)</dt></span></span> </dl> |



 

 





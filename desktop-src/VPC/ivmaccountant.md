---
title: 'IVMAccountant 介面 (VPCCOMInterfaces .h) '
description: 提供虛擬機器的帳戶計量相關資訊的存取權。
ms.assetid: 047fa4c9-cb2e-4830-bab8-0513247eff9b
keywords:
- IVMAccountant 介面 Virtual PC
- IVMAccountant 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMAccountant
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d207833b92794510789e66e31b10e94d70b319fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686415"
---
# <a name="ivmaccountant-interface"></a><span data-ttu-id="76828-105">IVMAccountant 介面</span><span class="sxs-lookup"><span data-stu-id="76828-105">IVMAccountant interface</span></span>

<span data-ttu-id="76828-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="76828-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76828-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="76828-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76828-108">提供虛擬機器的帳戶計量相關資訊的存取權。</span><span class="sxs-lookup"><span data-stu-id="76828-108">Provides access to accounting-related information for a virtual machine.</span></span> <span data-ttu-id="76828-109">若要取得虛擬機器的 **IVMAccountant** ，請使用 [**IVMVirtualMachine：：會計師**](ivmvirtualmachine-accountant.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="76828-109">To retrieve the **IVMAccountant** for a virtual machine, use the [**IVMVirtualMachine::Accountant**](ivmvirtualmachine-accountant.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="76828-110">成員</span><span class="sxs-lookup"><span data-stu-id="76828-110">Members</span></span>

<span data-ttu-id="76828-111">**IVMAccountant** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="76828-111">The **IVMAccountant** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="76828-112">**IVMAccountant** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="76828-112">**IVMAccountant** also has these types of members:</span></span>

-   [<span data-ttu-id="76828-113">屬性</span><span class="sxs-lookup"><span data-stu-id="76828-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="76828-114">屬性</span><span class="sxs-lookup"><span data-stu-id="76828-114">Properties</span></span>

<span data-ttu-id="76828-115">**IVMAccountant** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="76828-115">The **IVMAccountant** interface has these properties.</span></span>



| <span data-ttu-id="76828-116">屬性</span><span class="sxs-lookup"><span data-stu-id="76828-116">Property</span></span>                                                                        | <span data-ttu-id="76828-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="76828-117">Access type</span></span>          | <span data-ttu-id="76828-118">Description</span><span class="sxs-lookup"><span data-stu-id="76828-118">Description</span></span>                                                                                             |
|:--------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76828-119">**CPUUtilization**</span><span class="sxs-lookup"><span data-stu-id="76828-119">**CPUUtilization**</span></span>](ivmaccountant-cpuutilization.md)<br/>               | <span data-ttu-id="76828-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-120">Read-only</span></span><br/> | <span data-ttu-id="76828-121">此虛擬機器目前的 CPU 使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="76828-121">The percentage of current CPU utilization for this virtual machine.</span></span><br/>                          |
| [<span data-ttu-id="76828-122">**CPUUtilizationHistory**</span><span class="sxs-lookup"><span data-stu-id="76828-122">**CPUUtilizationHistory**</span></span>](ivmaccountant-cpuutilizationhistory.md)<br/> | <span data-ttu-id="76828-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-123">Read-only</span></span><br/> | <span data-ttu-id="76828-124">此虛擬機器的最近 CPU 使用率 (為百分比值陣列) 。</span><span class="sxs-lookup"><span data-stu-id="76828-124">The recent CPU utilization of this virtual machine (as an array of percentage values).</span></span><br/>       |
| [<span data-ttu-id="76828-125">**DiskBytesRead**</span><span class="sxs-lookup"><span data-stu-id="76828-125">**DiskBytesRead**</span></span>](ivmaccountant-diskbytesread.md)<br/>                 | <span data-ttu-id="76828-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-126">Read-only</span></span><br/> | <span data-ttu-id="76828-127">此虛擬機器的所有儲存控制器讀取的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="76828-127">The total number of bytes read by all storage controllers for this virtual machine.</span></span><br/>          |
| [<span data-ttu-id="76828-128">**DiskBytesWritten**</span><span class="sxs-lookup"><span data-stu-id="76828-128">**DiskBytesWritten**</span></span>](ivmaccountant-diskbyteswritten.md)<br/>           | <span data-ttu-id="76828-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-129">Read-only</span></span><br/> | <span data-ttu-id="76828-130">此虛擬機器的所有儲存控制器所寫入的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="76828-130">The total number of bytes written by all storage controllers for this virtual machine.</span></span><br/>       |
| [<span data-ttu-id="76828-131">**NetworkBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="76828-131">**NetworkBytesReceived**</span></span>](ivmaccountant-networkbytesreceived.md)<br/>   | <span data-ttu-id="76828-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-132">Read-only</span></span><br/> | <span data-ttu-id="76828-133">此虛擬機器的所有虛擬網路介面卡所接收的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="76828-133">The total number of bytes received by all virtual network adapters for this virtual machine.</span></span><br/> |
| [<span data-ttu-id="76828-134">**NetworkBytesSent**</span><span class="sxs-lookup"><span data-stu-id="76828-134">**NetworkBytesSent**</span></span>](ivmaccountant-networkbytessent.md)<br/>           | <span data-ttu-id="76828-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-135">Read-only</span></span><br/> | <span data-ttu-id="76828-136">此虛擬機器的所有虛擬網路介面卡所傳送的位元組總數。</span><span class="sxs-lookup"><span data-stu-id="76828-136">The total number of bytes sent by all virtual network adapters for this virtual machine.</span></span><br/>     |
| [<span data-ttu-id="76828-137">**99.99**</span><span class="sxs-lookup"><span data-stu-id="76828-137">**UpTime**</span></span>](ivmaccountant-uptime.md)<br/>                               | <span data-ttu-id="76828-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="76828-138">Read-only</span></span><br/> | <span data-ttu-id="76828-139">虛擬機器已執行的秒數。</span><span class="sxs-lookup"><span data-stu-id="76828-139">The number of seconds that the virtual machine has been running.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="76828-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="76828-140">Requirements</span></span>



| <span data-ttu-id="76828-141">需求</span><span class="sxs-lookup"><span data-stu-id="76828-141">Requirement</span></span> | <span data-ttu-id="76828-142">值</span><span class="sxs-lookup"><span data-stu-id="76828-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76828-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76828-143">Minimum supported client</span></span><br/> | <span data-ttu-id="76828-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76828-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76828-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76828-145">Minimum supported server</span></span><br/> | <span data-ttu-id="76828-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="76828-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76828-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="76828-147">End of client support</span></span><br/>    | <span data-ttu-id="76828-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76828-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76828-149">產品</span><span class="sxs-lookup"><span data-stu-id="76828-149">Product</span></span><br/>                  | <span data-ttu-id="76828-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76828-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76828-151">標頭</span><span class="sxs-lookup"><span data-stu-id="76828-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="76828-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="76828-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76828-153">IID</span><span class="sxs-lookup"><span data-stu-id="76828-153">IID</span></span><br/>                      | <span data-ttu-id="76828-154">IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73</span><span class="sxs-lookup"><span data-stu-id="76828-154">IID\_IVMAccountant is defined as 6376c067-7f57-4d63-b754-06e2e4f51d73</span></span><br/>              |



 


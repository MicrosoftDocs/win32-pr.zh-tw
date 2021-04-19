---
title: 'IVMVirtualNetwork 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬網路。
ms.assetid: 1ddafc33-05d4-45fb-924d-9830288aa240
keywords:
- IVMVirtualNetwork 介面 Virtual PC
- IVMVirtualNetwork 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06fb7c759059034874890f1dba7f7e2d1280ea8a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106972693"
---
# <a name="ivmvirtualnetwork-interface"></a><span data-ttu-id="110c0-105">IVMVirtualNetwork 介面</span><span class="sxs-lookup"><span data-stu-id="110c0-105">IVMVirtualNetwork interface</span></span>

<span data-ttu-id="110c0-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="110c0-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="110c0-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="110c0-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="110c0-108">定義虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="110c0-108">Defines a virtual network.</span></span> <span data-ttu-id="110c0-109">**IVMVirtualNetwork** 物件是從 [**IVMVirtualPC**](ivmvirtualpc.md) 方法 [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)傳回。</span><span class="sxs-lookup"><span data-stu-id="110c0-109">**IVMVirtualNetwork** objects are returned from [**IVMVirtualPC**](ivmvirtualpc.md) method [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md).</span></span> <span data-ttu-id="110c0-110">您也可以從 [**IVMVirtualPC：： VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)屬性傳回的 [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)物件中取出 **IVMVirtualNetwork** 物件。</span><span class="sxs-lookup"><span data-stu-id="110c0-110">You can also retrieve an **IVMVirtualNetwork** object from the [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md) object returned from the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

<span data-ttu-id="110c0-111">虛擬網路是由虛擬交換器所組成，它會執行所有的內部路由，以及數個「插入」至虛擬交換器的連接。</span><span class="sxs-lookup"><span data-stu-id="110c0-111">A virtual network consists of a virtual switch, which performs all internal routing, and several connections that are "plugged in" to the virtual switch.</span></span> <span data-ttu-id="110c0-112">這些連線可以是真實的外部主機連線、「內部網路」或共用網路 (NAT) 。</span><span class="sxs-lookup"><span data-stu-id="110c0-112">These connections can be a real external host connection, an "internal network" or shared networking (NAT).</span></span>

## <a name="members"></a><span data-ttu-id="110c0-113">成員</span><span class="sxs-lookup"><span data-stu-id="110c0-113">Members</span></span>

<span data-ttu-id="110c0-114">**IVMVirtualNetwork** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="110c0-114">The **IVMVirtualNetwork** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="110c0-115">**IVMVirtualNetwork** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="110c0-115">**IVMVirtualNetwork** also has these types of members:</span></span>

-   [<span data-ttu-id="110c0-116">方法</span><span class="sxs-lookup"><span data-stu-id="110c0-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="110c0-117">屬性</span><span class="sxs-lookup"><span data-stu-id="110c0-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="110c0-118">方法</span><span class="sxs-lookup"><span data-stu-id="110c0-118">Methods</span></span>

<span data-ttu-id="110c0-119">**IVMVirtualNetwork** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="110c0-119">The **IVMVirtualNetwork** interface has these methods.</span></span>



| <span data-ttu-id="110c0-120">方法</span><span class="sxs-lookup"><span data-stu-id="110c0-120">Method</span></span>                                | <span data-ttu-id="110c0-121">描述</span><span class="sxs-lookup"><span data-stu-id="110c0-121">Description</span></span>                                                          |
|:--------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="110c0-122">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="110c0-122">**\_ID**</span></span>](ivmvirtualnetwork--id.md) | <span data-ttu-id="110c0-123">抓取虛擬網路的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="110c0-123">Retrieves the internal identifier of the virtual network.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="110c0-124">屬性</span><span class="sxs-lookup"><span data-stu-id="110c0-124">Properties</span></span>

<span data-ttu-id="110c0-125">**IVMVirtualNetwork** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="110c0-125">The **IVMVirtualNetwork** interface has these properties.</span></span>



| <span data-ttu-id="110c0-126">屬性</span><span class="sxs-lookup"><span data-stu-id="110c0-126">Property</span></span>                                                                | <span data-ttu-id="110c0-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="110c0-127">Access type</span></span>          | <span data-ttu-id="110c0-128">Description</span><span class="sxs-lookup"><span data-stu-id="110c0-128">Description</span></span>                                                                    |
|:------------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="110c0-129">**HostAdapter**</span><span class="sxs-lookup"><span data-stu-id="110c0-129">**HostAdapter**</span></span>](ivmvirtualnetwork-hostadapter.md)<br/>         | <span data-ttu-id="110c0-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="110c0-130">Read-only</span></span><br/> | <span data-ttu-id="110c0-131">虛擬網路連線的介面卡名稱。</span><span class="sxs-lookup"><span data-stu-id="110c0-131">The name of the adapter to which the virtual network is connected.</span></span><br/>  |
| <span data-ttu-id="110c0-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="110c0-132">[**MediaType**](/previous-versions/windows/desktop/legacy/dd796707(v=vs.85))</span></span><br/>             | <span data-ttu-id="110c0-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="110c0-133">Read-only</span></span><br/> | <span data-ttu-id="110c0-134">判斷虛擬網路實例是否為無線。</span><span class="sxs-lookup"><span data-stu-id="110c0-134">Determines whether the virtual network instance is wireless or not.</span></span><br/> |
| [<span data-ttu-id="110c0-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="110c0-135">**Name**</span></span>](ivmvirtualnetwork-name.md)<br/>                       | <span data-ttu-id="110c0-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="110c0-136">Read-only</span></span><br/> | <span data-ttu-id="110c0-137">虛擬網路實例的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="110c0-137">The unique name of the virtual network instance.</span></span><br/>                    |
| [<span data-ttu-id="110c0-138">**NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="110c0-138">**NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)<br/> | <span data-ttu-id="110c0-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="110c0-139">Read-only</span></span><br/> | <span data-ttu-id="110c0-140">連接至虛擬網路之 Nic 的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="110c0-140">An enumerable collection of NICs attached to the virtual network.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="110c0-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="110c0-141">Requirements</span></span>



| <span data-ttu-id="110c0-142">需求</span><span class="sxs-lookup"><span data-stu-id="110c0-142">Requirement</span></span> | <span data-ttu-id="110c0-143">值</span><span class="sxs-lookup"><span data-stu-id="110c0-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="110c0-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="110c0-144">Minimum supported client</span></span><br/> | <span data-ttu-id="110c0-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="110c0-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="110c0-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="110c0-146">Minimum supported server</span></span><br/> | <span data-ttu-id="110c0-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="110c0-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="110c0-148">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="110c0-148">End of client support</span></span><br/>    | <span data-ttu-id="110c0-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="110c0-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="110c0-150">產品</span><span class="sxs-lookup"><span data-stu-id="110c0-150">Product</span></span><br/>                  | <span data-ttu-id="110c0-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="110c0-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="110c0-152">標頭</span><span class="sxs-lookup"><span data-stu-id="110c0-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="110c0-153"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="110c0-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="110c0-154">IID</span><span class="sxs-lookup"><span data-stu-id="110c0-154">IID</span></span><br/>                      | <span data-ttu-id="110c0-155">IID \_ IVMVirtualNetwork 定義為431cb7a1-2469-4563-b94e-38b987adca63</span><span class="sxs-lookup"><span data-stu-id="110c0-155">IID\_IVMVirtualNetwork is defined as 431cb7a1-2469-4563-b94e-38b987adca63</span></span><br/>          |



 


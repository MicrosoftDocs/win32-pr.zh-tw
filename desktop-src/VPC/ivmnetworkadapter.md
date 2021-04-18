---
title: 'IVMNetworkAdapter 介面 (VPCCOMInterfaces .h) '
description: 作為虛擬網路介面卡的介面。
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- IVMNetworkAdapter 介面 Virtual PC
- IVMNetworkAdapter 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384749"
---
# <a name="ivmnetworkadapter-interface"></a><span data-ttu-id="b7e79-105">IVMNetworkAdapter 介面</span><span class="sxs-lookup"><span data-stu-id="b7e79-105">IVMNetworkAdapter interface</span></span>

<span data-ttu-id="b7e79-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b7e79-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b7e79-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b7e79-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b7e79-108">作為虛擬網路介面卡的介面 (NIC) 。</span><span class="sxs-lookup"><span data-stu-id="b7e79-108">Serves as the interface to a virtual network interface card (NIC).</span></span> <span data-ttu-id="b7e79-109">它是用來設定虛擬機器的網路連線方式。</span><span class="sxs-lookup"><span data-stu-id="b7e79-109">It is used to set up how a virtual machine is networked.</span></span> <span data-ttu-id="b7e79-110">您可以使用 [**IVMVirtualMachine：： AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) 和 [**IVMVirtualMachine：： RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)來新增和移除網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="b7e79-110">Network interface cards can be added and removed by using [**IVMVirtualMachine::AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) and [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md).</span></span> <span data-ttu-id="b7e79-111">您也可以從 [**IVMVirtualMachine：： NetworkAdapters**](ivmvirtualmachine-networkadapters.md)或 [**IVMVirtualNetwork：： NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)屬性傳回的 [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)集合中取出 **IVMNetworkAdapter** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7e79-111">You can also retrieve an **IVMNetworkAdapter** object from the [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md) collection returned from the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md) or [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="b7e79-112">成員</span><span class="sxs-lookup"><span data-stu-id="b7e79-112">Members</span></span>

<span data-ttu-id="b7e79-113">**IVMNetworkAdapter** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="b7e79-113">The **IVMNetworkAdapter** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b7e79-114">**IVMNetworkAdapter** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b7e79-114">**IVMNetworkAdapter** also has these types of members:</span></span>

-   [<span data-ttu-id="b7e79-115">方法</span><span class="sxs-lookup"><span data-stu-id="b7e79-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="b7e79-116">屬性</span><span class="sxs-lookup"><span data-stu-id="b7e79-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b7e79-117">方法</span><span class="sxs-lookup"><span data-stu-id="b7e79-117">Methods</span></span>

<span data-ttu-id="b7e79-118">**IVMNetworkAdapter** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b7e79-118">The **IVMNetworkAdapter** interface has these methods.</span></span>



| <span data-ttu-id="b7e79-119">方法</span><span class="sxs-lookup"><span data-stu-id="b7e79-119">Method</span></span>                                                                         | <span data-ttu-id="b7e79-120">描述</span><span class="sxs-lookup"><span data-stu-id="b7e79-120">Description</span></span>                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="b7e79-121">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="b7e79-121">**\_ID**</span></span>](ivmnetworkadapter--id.md)                                          | <span data-ttu-id="b7e79-122">抓取此網路介面的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7e79-122">Retrieves the internal identifier of this network interface.</span></span><br/>     |
| [<span data-ttu-id="b7e79-123">**AttachToVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="b7e79-123">**AttachToVirtualNetwork**</span></span>](ivmnetworkadapter-attachtovirtualnetwork.md)     | <span data-ttu-id="b7e79-124">將網路介面附加至指定的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b7e79-124">Attaches the network interface to the specified virtual network.</span></span><br/> |
| [<span data-ttu-id="b7e79-125">**DetachFromVirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="b7e79-125">**DetachFromVirtualNetwork**</span></span>](ivmnetworkadapter-detachfromvirtualnetwork.md) | <span data-ttu-id="b7e79-126">從虛擬網路卸離網路介面。</span><span class="sxs-lookup"><span data-stu-id="b7e79-126">Detaches the network interface from its virtual network.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="b7e79-127">屬性</span><span class="sxs-lookup"><span data-stu-id="b7e79-127">Properties</span></span>

<span data-ttu-id="b7e79-128">**IVMNetworkAdapter** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="b7e79-128">The **IVMNetworkAdapter** interface has these properties.</span></span>



| <span data-ttu-id="b7e79-129">屬性</span><span class="sxs-lookup"><span data-stu-id="b7e79-129">Property</span></span>                                                                                  | <span data-ttu-id="b7e79-130">存取類型</span><span class="sxs-lookup"><span data-stu-id="b7e79-130">Access type</span></span>           | <span data-ttu-id="b7e79-131">Description</span><span class="sxs-lookup"><span data-stu-id="b7e79-131">Description</span></span>                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="b7e79-132">**EthernetAddress**</span><span class="sxs-lookup"><span data-stu-id="b7e79-132">**EthernetAddress**</span></span>](ivmnetworkadapter-ethernetaddress.md)<br/>                   | <span data-ttu-id="b7e79-133">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b7e79-133">Read/write</span></span><br/> | <span data-ttu-id="b7e79-134">網路介面的 Ethernet (MAC) 位址。</span><span class="sxs-lookup"><span data-stu-id="b7e79-134">The Ethernet (MAC) address of the network interface.</span></span><br/>             |
| [<span data-ttu-id="b7e79-135">**IsEthernetAddressDynamic**</span><span class="sxs-lookup"><span data-stu-id="b7e79-135">**IsEthernetAddressDynamic**</span></span>](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | <span data-ttu-id="b7e79-136">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="b7e79-136">Read/write</span></span><br/> | <span data-ttu-id="b7e79-137">指出是否動態產生乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="b7e79-137">Indicates whether the Ethernet address is dynamically generated.</span></span><br/> |
| [<span data-ttu-id="b7e79-138">**VirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="b7e79-138">**VirtualMachine**</span></span>](ivmnetworkadapter-virtualmachine.md)<br/>                     | <span data-ttu-id="b7e79-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="b7e79-139">Read-only</span></span><br/>  | <span data-ttu-id="b7e79-140">與此網路介面相關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b7e79-140">The virtual machine associated with this network interface.</span></span><br/>      |
| [<span data-ttu-id="b7e79-141">**VirtualNetwork**</span><span class="sxs-lookup"><span data-stu-id="b7e79-141">**VirtualNetwork**</span></span>](ivmnetworkadapter-virtualnetwork.md)<br/>                     | <span data-ttu-id="b7e79-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="b7e79-142">Read-only</span></span><br/>  | <span data-ttu-id="b7e79-143">網路介面所連接的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b7e79-143">The virtual network to which the network interface is attached.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="b7e79-144">備註</span><span class="sxs-lookup"><span data-stu-id="b7e79-144">Remarks</span></span>

<span data-ttu-id="b7e79-145">網路介面的預設乙太網路位址是 "00-00-00-00-00-00"，大部分的作業系統都會將其視為不正確乙太網路位址。</span><span class="sxs-lookup"><span data-stu-id="b7e79-145">The default Ethernet address for a network interface is "00-00-00-00-00-00", which is considered an invalid Ethernet address by most operating systems.</span></span> <span data-ttu-id="b7e79-146">如果 [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) 設定為 **FALSE**，則必須使用有效的乙太網路位址來初始化 [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) 。</span><span class="sxs-lookup"><span data-stu-id="b7e79-146">If [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) is set to **FALSE**, [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) must be initialized with a valid Ethernet network address.</span></span>

<span data-ttu-id="b7e79-147">下列程式說明如何使用 **IVMNetworkAdapter** 介面。</span><span class="sxs-lookup"><span data-stu-id="b7e79-147">The following procedures explain how to use the **IVMNetworkAdapter** interface.</span></span>

<span data-ttu-id="b7e79-148">**將虛擬 NIC 連結至主機 NIC**</span><span class="sxs-lookup"><span data-stu-id="b7e79-148">**To attach a virtual NIC to a host NIC**</span></span>

-   <span data-ttu-id="b7e79-149">虛擬 (來賓) Nic 不會直接連接至主機 NIC。</span><span class="sxs-lookup"><span data-stu-id="b7e79-149">Virtual (guest) NICs are not attached directly to a host NIC.</span></span> <span data-ttu-id="b7e79-150">相反地，虛擬 NIC 會連接到連接至主機 NIC 的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="b7e79-150">Instead, the virtual NIC is attached to a virtual network that is attached to a host NIC.</span></span> <span data-ttu-id="b7e79-151">如需設定虛擬網路的詳細資訊，請參閱 [**IVMVirtualNetwork**](ivmvirtualnetwork.md)。</span><span class="sxs-lookup"><span data-stu-id="b7e79-151">For more information about configuring virtual networks, see [**IVMVirtualNetwork**](ivmvirtualnetwork.md).</span></span> <span data-ttu-id="b7e79-152">若要將虛擬 NIC 連結至虛擬網路，請使用 [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7e79-152">To attach the virtual NIC to a virtual network, use the [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) method.</span></span>

<span data-ttu-id="b7e79-153">**中斷虛擬 NIC 與虛擬網路的連線**</span><span class="sxs-lookup"><span data-stu-id="b7e79-153">**To disconnect a virtual NIC from the virtual network**</span></span>

-   <span data-ttu-id="b7e79-154">[**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md)方法會將虛擬 NIC 從虛擬網路卸離。</span><span class="sxs-lookup"><span data-stu-id="b7e79-154">The [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) method will detach the virtual NIC from the virtual network.</span></span> <span data-ttu-id="b7e79-155">呼叫這個函數之後， [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) 屬性會傳回不正確虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7e79-155">After this function is called, the [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) property will return a virtual network ID that is not valid.</span></span>

<span data-ttu-id="b7e79-156">**如果您有虛擬 NIC 物件，則從虛擬機器移除虛擬 NIC**</span><span class="sxs-lookup"><span data-stu-id="b7e79-156">**To remove a virtual NIC from a virtual machine if you have the virtual NIC object**</span></span>

1.  <span data-ttu-id="b7e79-157">使用 [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) 屬性，取得與虛擬 NIC 相關聯的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b7e79-157">Get the virtual machine associated with the virtual NIC by using the [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) property.</span></span>
2.  <span data-ttu-id="b7e79-158">使用目前的物件做為 [**IVMVirtualMachine：： RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) 方法的參數。</span><span class="sxs-lookup"><span data-stu-id="b7e79-158">Use the current object as a parameter to the [**IVMVirtualMachine::RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7e79-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7e79-159">Requirements</span></span>



| <span data-ttu-id="b7e79-160">需求</span><span class="sxs-lookup"><span data-stu-id="b7e79-160">Requirement</span></span> | <span data-ttu-id="b7e79-161">值</span><span class="sxs-lookup"><span data-stu-id="b7e79-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7e79-162">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7e79-162">Minimum supported client</span></span><br/> | <span data-ttu-id="b7e79-163">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7e79-163">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7e79-164">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7e79-164">Minimum supported server</span></span><br/> | <span data-ttu-id="b7e79-165">都不支援</span><span class="sxs-lookup"><span data-stu-id="b7e79-165">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b7e79-166">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b7e79-166">End of client support</span></span><br/>    | <span data-ttu-id="b7e79-167">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7e79-167">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b7e79-168">產品</span><span class="sxs-lookup"><span data-stu-id="b7e79-168">Product</span></span><br/>                  | <span data-ttu-id="b7e79-169">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b7e79-169">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b7e79-170">標頭</span><span class="sxs-lookup"><span data-stu-id="b7e79-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7e79-171"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7e79-171"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b7e79-172">IID</span><span class="sxs-lookup"><span data-stu-id="b7e79-172">IID</span></span><br/>                      | <span data-ttu-id="b7e79-173">IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a</span><span class="sxs-lookup"><span data-stu-id="b7e79-173">IID\_IVMNetworkAdapter is defined as e32e4165-22b8-4dc0-8d57-850171ae207a</span></span><br/>          |



 


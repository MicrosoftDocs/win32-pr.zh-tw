---
title: 'IVMNetworkAdapterCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬網路介面卡的集合。 若要取得 IVMNetworkAdapterCollection 物件，請使用 IVMVirtualMachine NetworkAdapters、IVMVirtualNetwork NetworkAdapters 和 IVMVirtualPC UnconnectedNetworkAdapters 屬性。
ms.assetid: cfb03a7c-a568-488c-9284-798b7e21027a
keywords:
- IVMNetworkAdapterCollection 介面 Virtual PC
- IVMNetworkAdapterCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMNetworkAdapterCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8005b88cb873f00708829672cdeb6563b606d42b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025194"
---
# <a name="ivmnetworkadaptercollection-interface"></a><span data-ttu-id="263e0-106">IVMNetworkAdapterCollection 介面</span><span class="sxs-lookup"><span data-stu-id="263e0-106">IVMNetworkAdapterCollection interface</span></span>

<span data-ttu-id="263e0-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="263e0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="263e0-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="263e0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="263e0-109">定義虛擬網路介面卡的集合。</span><span class="sxs-lookup"><span data-stu-id="263e0-109">Defines a collection of virtual network interface cards.</span></span> <span data-ttu-id="263e0-110">若要取得 IVMNetworkAdapterCollection 物件，請使用 [**IVMVirtualMachine：： NetworkAdapters**](ivmvirtualmachine-networkadapters.md)、 [**IVMVirtualNetwork：： NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)和 [**IVMVirtualPC：： UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="263e0-110">To obtain an IVMNetworkAdapterCollection object, use the [**IVMVirtualMachine::NetworkAdapters**](ivmvirtualmachine-networkadapters.md), [**IVMVirtualNetwork::NetworkAdapters**](ivmvirtualnetwork-networkadapters.md), and [**IVMVirtualPC::UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md) properties.</span></span>

## <a name="members"></a><span data-ttu-id="263e0-111">成員</span><span class="sxs-lookup"><span data-stu-id="263e0-111">Members</span></span>

<span data-ttu-id="263e0-112">**IVMNetworkAdapterCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="263e0-112">The **IVMNetworkAdapterCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="263e0-113">**IVMNetworkAdapterCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="263e0-113">**IVMNetworkAdapterCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="263e0-114">屬性</span><span class="sxs-lookup"><span data-stu-id="263e0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="263e0-115">屬性</span><span class="sxs-lookup"><span data-stu-id="263e0-115">Properties</span></span>

<span data-ttu-id="263e0-116">**IVMNetworkAdapterCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="263e0-116">The **IVMNetworkAdapterCollection** interface has these properties.</span></span>



| <span data-ttu-id="263e0-117">屬性</span><span class="sxs-lookup"><span data-stu-id="263e0-117">Property</span></span>                                                             | <span data-ttu-id="263e0-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="263e0-118">Access type</span></span>          | <span data-ttu-id="263e0-119">Description</span><span class="sxs-lookup"><span data-stu-id="263e0-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="263e0-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="263e0-120">**\_NewEnum**</span></span>](ivmnetworkadaptercollection--newenum.md)<br/> | <span data-ttu-id="263e0-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="263e0-121">Read-only</span></span><br/> | <span data-ttu-id="263e0-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="263e0-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="263e0-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="263e0-123">**Count**</span></span>](ivmnetworkadaptercollection-count.md)<br/>        | <span data-ttu-id="263e0-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="263e0-124">Read-only</span></span><br/> | <span data-ttu-id="263e0-125">這個集合中的網路介面數目。</span><span class="sxs-lookup"><span data-stu-id="263e0-125">The number of network interfaces in this collection.</span></span><br/>                                               |
| [<span data-ttu-id="263e0-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="263e0-126">**Item**</span></span>](ivmnetworkadaptercollection-item.md)<br/>          | <span data-ttu-id="263e0-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="263e0-127">Read-only</span></span><br/> | <span data-ttu-id="263e0-128">對應至指定之索引的 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="263e0-128">The [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="263e0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="263e0-129">Requirements</span></span>



| <span data-ttu-id="263e0-130">需求</span><span class="sxs-lookup"><span data-stu-id="263e0-130">Requirement</span></span> | <span data-ttu-id="263e0-131">值</span><span class="sxs-lookup"><span data-stu-id="263e0-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="263e0-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="263e0-132">Minimum supported client</span></span><br/> | <span data-ttu-id="263e0-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="263e0-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="263e0-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="263e0-134">Minimum supported server</span></span><br/> | <span data-ttu-id="263e0-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="263e0-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="263e0-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="263e0-136">End of client support</span></span><br/>    | <span data-ttu-id="263e0-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="263e0-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="263e0-138">產品</span><span class="sxs-lookup"><span data-stu-id="263e0-138">Product</span></span><br/>                  | <span data-ttu-id="263e0-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="263e0-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="263e0-140">標頭</span><span class="sxs-lookup"><span data-stu-id="263e0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="263e0-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="263e0-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="263e0-142">IID</span><span class="sxs-lookup"><span data-stu-id="263e0-142">IID</span></span><br/>                      | <span data-ttu-id="263e0-143">IID \_ IVMNetworkAdapterCollection 定義為 ebaeafe9-ebcd-47cf-866e-ad87d735e479</span><span class="sxs-lookup"><span data-stu-id="263e0-143">IID\_IVMNetworkAdapterCollection is defined as ebaeafe9-ebcd-47cf-866e-ad87d735e479</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="263e0-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="263e0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="263e0-145">**IVMNetworkAdapter**</span><span class="sxs-lookup"><span data-stu-id="263e0-145">**IVMNetworkAdapter**</span></span>](ivmnetworkadapter.md)
</dt> <dt>

[<span data-ttu-id="263e0-146">**IVMVirtualMachine::NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="263e0-146">**IVMVirtualMachine::NetworkAdapters**</span></span>](ivmvirtualmachine-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="263e0-147">**IVMVirtualNetwork::NetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="263e0-147">**IVMVirtualNetwork::NetworkAdapters**</span></span>](ivmvirtualnetwork-networkadapters.md)
</dt> <dt>

[<span data-ttu-id="263e0-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span><span class="sxs-lookup"><span data-stu-id="263e0-148">**IVMVirtualPC::UnconnectedNetworkAdapters**</span></span>](ivmvirtualpc-unconnectednetworkadapters.md)
</dt> </dl>

 


---
title: 'IVMVirtualMachineCollection 介面 (VPCCOMInterfaces .h) '
description: 定義 Windows Virtual PC 中的虛擬機器集合。 若要取得 IVMVirtualMachineCollection 物件，請使用 IVMVirtualPC VirtualMachines 屬性。
ms.assetid: 3d34e791-2dba-4529-b489-96a0c6227294
keywords:
- IVMVirtualMachineCollection 介面 Virtual PC
- IVMVirtualMachineCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualMachineCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27426f96e409a1e67eb519e7a864ee7461879a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105647"
---
# <a name="ivmvirtualmachinecollection-interface"></a><span data-ttu-id="e8813-106">IVMVirtualMachineCollection 介面</span><span class="sxs-lookup"><span data-stu-id="e8813-106">IVMVirtualMachineCollection interface</span></span>

<span data-ttu-id="e8813-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e8813-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e8813-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e8813-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e8813-109">定義 Windows Virtual PC 中的虛擬機器集合。</span><span class="sxs-lookup"><span data-stu-id="e8813-109">Defines the collection of virtual machines within Windows Virtual PC.</span></span> <span data-ttu-id="e8813-110">若要取得 **IVMVirtualMachineCollection** 物件，請使用 [**IVMVirtualPC：： VirtualMachines**](ivmvirtualpc-virtualmachines.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e8813-110">To obtain an **IVMVirtualMachineCollection** object, use the [**IVMVirtualPC::VirtualMachines**](ivmvirtualpc-virtualmachines.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="e8813-111">成員</span><span class="sxs-lookup"><span data-stu-id="e8813-111">Members</span></span>

<span data-ttu-id="e8813-112">**IVMVirtualMachineCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="e8813-112">The **IVMVirtualMachineCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e8813-113">**IVMVirtualMachineCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e8813-113">**IVMVirtualMachineCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="e8813-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e8813-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8813-115">屬性</span><span class="sxs-lookup"><span data-stu-id="e8813-115">Properties</span></span>

<span data-ttu-id="e8813-116">**IVMVirtualMachineCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e8813-116">The **IVMVirtualMachineCollection** interface has these properties.</span></span>



| <span data-ttu-id="e8813-117">屬性</span><span class="sxs-lookup"><span data-stu-id="e8813-117">Property</span></span>                                                             | <span data-ttu-id="e8813-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="e8813-118">Access type</span></span>          | <span data-ttu-id="e8813-119">Description</span><span class="sxs-lookup"><span data-stu-id="e8813-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="e8813-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e8813-120">**\_NewEnum**</span></span>](ivmvirtualmachinecollection--newenum.md)<br/> | <span data-ttu-id="e8813-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="e8813-121">Read-only</span></span><br/> | <span data-ttu-id="e8813-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="e8813-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="e8813-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="e8813-123">**Count**</span></span>](ivmvirtualmachinecollection-count.md)<br/>        | <span data-ttu-id="e8813-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="e8813-124">Read-only</span></span><br/> | <span data-ttu-id="e8813-125">此集合中的虛擬機器數目。</span><span class="sxs-lookup"><span data-stu-id="e8813-125">The number of virtual machines in this collection.</span></span><br/>                  |
| [<span data-ttu-id="e8813-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="e8813-126">**Item**</span></span>](ivmvirtualmachinecollection-item.md)<br/>          | <span data-ttu-id="e8813-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="e8813-127">Read-only</span></span><br/> | <span data-ttu-id="e8813-128">對應至指定之索引的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="e8813-128">The virtual machine object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8813-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8813-129">Requirements</span></span>



| <span data-ttu-id="e8813-130">需求</span><span class="sxs-lookup"><span data-stu-id="e8813-130">Requirement</span></span> | <span data-ttu-id="e8813-131">值</span><span class="sxs-lookup"><span data-stu-id="e8813-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8813-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8813-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e8813-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e8813-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e8813-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8813-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e8813-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="e8813-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e8813-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e8813-136">End of client support</span></span><br/>    | <span data-ttu-id="e8813-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e8813-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="e8813-138">產品</span><span class="sxs-lookup"><span data-stu-id="e8813-138">Product</span></span><br/>                  | <span data-ttu-id="e8813-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e8813-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="e8813-140">標頭</span><span class="sxs-lookup"><span data-stu-id="e8813-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8813-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8813-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="e8813-142">IID</span><span class="sxs-lookup"><span data-stu-id="e8813-142">IID</span></span><br/>                      | <span data-ttu-id="e8813-143">IID \_ IVMVirtualMachineCollection 定義為 59f31786-2a3d-4fbf-9896-d85338ca0da1</span><span class="sxs-lookup"><span data-stu-id="e8813-143">IID\_IVMVirtualMachineCollection is defined as 59f31786-2a3d-4fbf-9896-d85338ca0da1</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8813-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8813-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8813-145">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="e8813-145">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="e8813-146">**IVMVirtualPC：： VirtualMachines**</span><span class="sxs-lookup"><span data-stu-id="e8813-146">**IVMVirtualPC::VirtualMachines**</span></span>](ivmvirtualpc-virtualmachines.md)
</dt> </dl>

 


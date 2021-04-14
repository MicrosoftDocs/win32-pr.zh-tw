---
title: 'IVMParallelPortCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的平行埠集合。 若要取得 IVMParallelPortCollection 物件，請使用 IVMVirtualMachine ParallelPorts 屬性。
ms.assetid: 038a5c08-cd92-426f-a059-9a4c2110548d
keywords:
- IVMParallelPortCollection 介面 Virtual PC
- IVMParallelPortCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMParallelPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8284b3720e0272147c932cfbfd70448babf5606f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106050"
---
# <a name="ivmparallelportcollection-interface"></a><span data-ttu-id="40069-106">IVMParallelPortCollection 介面</span><span class="sxs-lookup"><span data-stu-id="40069-106">IVMParallelPortCollection interface</span></span>

<span data-ttu-id="40069-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="40069-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40069-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="40069-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40069-109">定義虛擬機器內的平行埠集合。</span><span class="sxs-lookup"><span data-stu-id="40069-109">Defines the collection of parallel ports within the virtual machine.</span></span> <span data-ttu-id="40069-110">若要取得 **IVMParallelPortCollection** 物件，請使用 [**IVMVirtualMachine：:P arallelports**](ivmvirtualmachine-parallelports.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="40069-110">To obtain an **IVMParallelPortCollection** object, use the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="40069-111">成員</span><span class="sxs-lookup"><span data-stu-id="40069-111">Members</span></span>

<span data-ttu-id="40069-112">**IVMParallelPortCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="40069-112">The **IVMParallelPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="40069-113">**IVMParallelPortCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="40069-113">**IVMParallelPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="40069-114">屬性</span><span class="sxs-lookup"><span data-stu-id="40069-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40069-115">屬性</span><span class="sxs-lookup"><span data-stu-id="40069-115">Properties</span></span>

<span data-ttu-id="40069-116">**IVMParallelPortCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="40069-116">The **IVMParallelPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="40069-117">屬性</span><span class="sxs-lookup"><span data-stu-id="40069-117">Property</span></span>                                                           | <span data-ttu-id="40069-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="40069-118">Access type</span></span>          | <span data-ttu-id="40069-119">Description</span><span class="sxs-lookup"><span data-stu-id="40069-119">Description</span></span>                                                                  |
|:-------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="40069-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="40069-120">**\_NewEnum**</span></span>](ivmparallelportcollection--newenum.md)<br/> | <span data-ttu-id="40069-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="40069-121">Read-only</span></span><br/> | <span data-ttu-id="40069-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="40069-122">An enumerator for the collection.</span></span><br/>                                 |
| [<span data-ttu-id="40069-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="40069-123">**Count**</span></span>](ivmparallelportcollection-count.md)<br/>        | <span data-ttu-id="40069-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="40069-124">Read-only</span></span><br/> | <span data-ttu-id="40069-125">此集合中的平行埠數目。</span><span class="sxs-lookup"><span data-stu-id="40069-125">The number of parallel ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="40069-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="40069-126">**Item**</span></span>](ivmparallelportcollection-item.md)<br/>          | <span data-ttu-id="40069-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="40069-127">Read-only</span></span><br/> | <span data-ttu-id="40069-128">對應至指定之索引的平行埠物件。</span><span class="sxs-lookup"><span data-stu-id="40069-128">The parallel port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="40069-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="40069-129">Requirements</span></span>



| <span data-ttu-id="40069-130">需求</span><span class="sxs-lookup"><span data-stu-id="40069-130">Requirement</span></span> | <span data-ttu-id="40069-131">值</span><span class="sxs-lookup"><span data-stu-id="40069-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40069-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40069-132">Minimum supported client</span></span><br/> | <span data-ttu-id="40069-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40069-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40069-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40069-134">Minimum supported server</span></span><br/> | <span data-ttu-id="40069-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="40069-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40069-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="40069-136">End of client support</span></span><br/>    | <span data-ttu-id="40069-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40069-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40069-138">產品</span><span class="sxs-lookup"><span data-stu-id="40069-138">Product</span></span><br/>                  | <span data-ttu-id="40069-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40069-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40069-140">標頭</span><span class="sxs-lookup"><span data-stu-id="40069-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="40069-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="40069-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40069-142">IID</span><span class="sxs-lookup"><span data-stu-id="40069-142">IID</span></span><br/>                      | <span data-ttu-id="40069-143">IID \_ IVMParallelPortCollection 定義為27c3e036-198f-430c-8735-6e652f7203fd</span><span class="sxs-lookup"><span data-stu-id="40069-143">IID\_IVMParallelPortCollection is defined as 27c3e036-198f-430c-8735-6e652f7203fd</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="40069-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40069-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40069-145">**IVMParallelPort**</span><span class="sxs-lookup"><span data-stu-id="40069-145">**IVMParallelPort**</span></span>](ivmparallelport.md)
</dt> <dt>

[<span data-ttu-id="40069-146">**IVMVirtualMachine：:P arallelPorts**</span><span class="sxs-lookup"><span data-stu-id="40069-146">**IVMVirtualMachine::ParallelPorts**</span></span>](ivmvirtualmachine-parallelports.md)
</dt> </dl>

 


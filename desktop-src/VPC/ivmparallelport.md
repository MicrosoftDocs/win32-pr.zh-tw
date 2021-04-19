---
title: 'IVMParallelPort 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的平行埠。
ms.assetid: da8daf16-5d22-49be-8fe9-72d5018c0622
keywords:
- IVMParallelPort 介面 Virtual PC
- IVMParallelPort 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMParallelPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b76b23f48e728104a3826afa80a8f272cd7e66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965945"
---
# <a name="ivmparallelport-interface"></a><span data-ttu-id="c96e8-105">IVMParallelPort 介面</span><span class="sxs-lookup"><span data-stu-id="c96e8-105">IVMParallelPort interface</span></span>

<span data-ttu-id="c96e8-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="c96e8-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c96e8-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="c96e8-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c96e8-108">定義虛擬機器內的平行埠。</span><span class="sxs-lookup"><span data-stu-id="c96e8-108">Defines a parallel port inside a virtual machine.</span></span> <span data-ttu-id="c96e8-109">此介面可讓您在虛擬機器內設定平行埠。</span><span class="sxs-lookup"><span data-stu-id="c96e8-109">This interface allows you to configure parallel ports inside a virtual machine.</span></span> <span data-ttu-id="c96e8-110">您可以從 [**IVMVirtualMachine：:P arallelports**](ivmvirtualmachine-parallelports.md)屬性傳回的 [**IVMParallelPortCollection**](ivmparallelportcollection.md)物件中取出 **IVMParallelPort** 物件。</span><span class="sxs-lookup"><span data-stu-id="c96e8-110">You can retrieve an **IVMParallelPort** object from the [**IVMParallelPortCollection**](ivmparallelportcollection.md) object returned from the [**IVMVirtualMachine::ParallelPorts**](ivmvirtualmachine-parallelports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="c96e8-111">成員</span><span class="sxs-lookup"><span data-stu-id="c96e8-111">Members</span></span>

<span data-ttu-id="c96e8-112">**IVMParallelPort** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="c96e8-112">The **IVMParallelPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c96e8-113">**IVMParallelPort** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c96e8-113">**IVMParallelPort** also has these types of members:</span></span>

-   [<span data-ttu-id="c96e8-114">方法</span><span class="sxs-lookup"><span data-stu-id="c96e8-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c96e8-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c96e8-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c96e8-116">方法</span><span class="sxs-lookup"><span data-stu-id="c96e8-116">Methods</span></span>

<span data-ttu-id="c96e8-117">**IVMParallelPort** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c96e8-117">The **IVMParallelPort** interface has these methods.</span></span>



| <span data-ttu-id="c96e8-118">方法</span><span class="sxs-lookup"><span data-stu-id="c96e8-118">Method</span></span>                              | <span data-ttu-id="c96e8-119">描述</span><span class="sxs-lookup"><span data-stu-id="c96e8-119">Description</span></span>                                                        |
|:------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="c96e8-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="c96e8-120">**\_ID**</span></span>](ivmparallelport--id.md) | <span data-ttu-id="c96e8-121">抓取平行埠的內部識別碼。</span><span class="sxs-lookup"><span data-stu-id="c96e8-121">Retrieves the internal identifier of the parallel port.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c96e8-122">屬性</span><span class="sxs-lookup"><span data-stu-id="c96e8-122">Properties</span></span>

<span data-ttu-id="c96e8-123">**IVMParallelPort** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c96e8-123">The **IVMParallelPort** interface has these properties.</span></span>



| <span data-ttu-id="c96e8-124">屬性</span><span class="sxs-lookup"><span data-stu-id="c96e8-124">Property</span></span>                                        | <span data-ttu-id="c96e8-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="c96e8-125">Access type</span></span>           | <span data-ttu-id="c96e8-126">Description</span><span class="sxs-lookup"><span data-stu-id="c96e8-126">Description</span></span>                               |
|:------------------------------------------------|:----------------------|:------------------------------------------|
| [<span data-ttu-id="c96e8-127">**Name**</span><span class="sxs-lookup"><span data-stu-id="c96e8-127">**Name**</span></span>](ivmparallelport-name.md)<br/> | <span data-ttu-id="c96e8-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c96e8-128">Read/write</span></span><br/> | <span data-ttu-id="c96e8-129">平行埠的名稱。</span><span class="sxs-lookup"><span data-stu-id="c96e8-129">The name of the parallel port.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c96e8-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="c96e8-130">Requirements</span></span>



| <span data-ttu-id="c96e8-131">需求</span><span class="sxs-lookup"><span data-stu-id="c96e8-131">Requirement</span></span> | <span data-ttu-id="c96e8-132">值</span><span class="sxs-lookup"><span data-stu-id="c96e8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c96e8-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c96e8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c96e8-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c96e8-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c96e8-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c96e8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c96e8-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="c96e8-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c96e8-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c96e8-137">End of client support</span></span><br/>    | <span data-ttu-id="c96e8-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c96e8-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c96e8-139">產品</span><span class="sxs-lookup"><span data-stu-id="c96e8-139">Product</span></span><br/>                  | <span data-ttu-id="c96e8-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c96e8-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c96e8-141">標頭</span><span class="sxs-lookup"><span data-stu-id="c96e8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c96e8-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="c96e8-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c96e8-143">IID</span><span class="sxs-lookup"><span data-stu-id="c96e8-143">IID</span></span><br/>                      | <span data-ttu-id="c96e8-144">IID \_ IVMParallelPort 定義為097beecb-0a02-474f-abd6-298b22293fc6</span><span class="sxs-lookup"><span data-stu-id="c96e8-144">IID\_IVMParallelPort is defined as 097beecb-0a02-474f-abd6-298b22293fc6</span></span><br/>            |



 


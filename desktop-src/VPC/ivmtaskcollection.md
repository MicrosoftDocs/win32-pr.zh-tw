---
title: 'IVMTaskCollection 介面 (VPCCOMInterfaces .h) '
description: 定義工作物件的集合。 若要取得 IVMTaskCollection 物件，請使用 IVMVirtualPC Tasks 屬性。
ms.assetid: 5cfc543c-81a1-49d2-93a9-9b1db1cb5070
keywords:
- IVMTaskCollection 介面 Virtual PC
- IVMTaskCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMTaskCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ff7a4b12b936f2b5c72a73818eca0f927eef12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385042"
---
# <a name="ivmtaskcollection-interface"></a><span data-ttu-id="14c25-106">IVMTaskCollection 介面</span><span class="sxs-lookup"><span data-stu-id="14c25-106">IVMTaskCollection interface</span></span>

<span data-ttu-id="14c25-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="14c25-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="14c25-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="14c25-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="14c25-109">定義工作物件的集合。</span><span class="sxs-lookup"><span data-stu-id="14c25-109">Defines the collection of task objects.</span></span> <span data-ttu-id="14c25-110">若要取得 **IVMTaskCollection** 物件，請使用 [**IVMVirtualPC：： Tasks**](ivmvirtualpc-tasks.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="14c25-110">To obtain an **IVMTaskCollection** object, use the [**IVMVirtualPC::Tasks**](ivmvirtualpc-tasks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="14c25-111">成員</span><span class="sxs-lookup"><span data-stu-id="14c25-111">Members</span></span>

<span data-ttu-id="14c25-112">**IVMTaskCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="14c25-112">The **IVMTaskCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="14c25-113">**IVMTaskCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="14c25-113">**IVMTaskCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="14c25-114">屬性</span><span class="sxs-lookup"><span data-stu-id="14c25-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="14c25-115">屬性</span><span class="sxs-lookup"><span data-stu-id="14c25-115">Properties</span></span>

<span data-ttu-id="14c25-116">**IVMTaskCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="14c25-116">The **IVMTaskCollection** interface has these properties.</span></span>



| <span data-ttu-id="14c25-117">屬性</span><span class="sxs-lookup"><span data-stu-id="14c25-117">Property</span></span>                                                   | <span data-ttu-id="14c25-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="14c25-118">Access type</span></span>          | <span data-ttu-id="14c25-119">Description</span><span class="sxs-lookup"><span data-stu-id="14c25-119">Description</span></span>                                                         |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="14c25-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="14c25-120">**\_NewEnum**</span></span>](ivmtaskcollection--newenum.md)<br/> | <span data-ttu-id="14c25-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="14c25-121">Read-only</span></span><br/> | <span data-ttu-id="14c25-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="14c25-122">An enumerator for the collection.</span></span><br/>                        |
| [<span data-ttu-id="14c25-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="14c25-123">**Count**</span></span>](ivmtaskcollection-count.md)<br/>        | <span data-ttu-id="14c25-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="14c25-124">Read-only</span></span><br/> | <span data-ttu-id="14c25-125">這個集合中的工作數目。</span><span class="sxs-lookup"><span data-stu-id="14c25-125">The number of tasks in this collection.</span></span><br/>                  |
| [<span data-ttu-id="14c25-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="14c25-126">**Item**</span></span>](ivmtaskcollection-item.md)<br/>          | <span data-ttu-id="14c25-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="14c25-127">Read-only</span></span><br/> | <span data-ttu-id="14c25-128">對應至指定之索引的 task 物件。</span><span class="sxs-lookup"><span data-stu-id="14c25-128">The task object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="14c25-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="14c25-129">Requirements</span></span>



| <span data-ttu-id="14c25-130">需求</span><span class="sxs-lookup"><span data-stu-id="14c25-130">Requirement</span></span> | <span data-ttu-id="14c25-131">值</span><span class="sxs-lookup"><span data-stu-id="14c25-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14c25-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="14c25-132">Minimum supported client</span></span><br/> | <span data-ttu-id="14c25-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="14c25-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="14c25-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="14c25-134">Minimum supported server</span></span><br/> | <span data-ttu-id="14c25-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="14c25-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="14c25-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="14c25-136">End of client support</span></span><br/>    | <span data-ttu-id="14c25-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="14c25-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="14c25-138">產品</span><span class="sxs-lookup"><span data-stu-id="14c25-138">Product</span></span><br/>                  | <span data-ttu-id="14c25-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="14c25-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="14c25-140">標頭</span><span class="sxs-lookup"><span data-stu-id="14c25-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="14c25-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="14c25-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="14c25-142">IID</span><span class="sxs-lookup"><span data-stu-id="14c25-142">IID</span></span><br/>                      | <span data-ttu-id="14c25-143">IID \_ IVMTaskCollection 定義為5c4387c8-0e8b-4b97-8058-84679adf4c40</span><span class="sxs-lookup"><span data-stu-id="14c25-143">IID\_IVMTaskCollection is defined as 5c4387c8-0e8b-4b97-8058-84679adf4c40</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="14c25-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14c25-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c25-145">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="14c25-145">**IVMTask**</span></span>](ivmtask.md)
</dt> <dt>

[<span data-ttu-id="14c25-146">**IVMVirtualPC：： Tasks**</span><span class="sxs-lookup"><span data-stu-id="14c25-146">**IVMVirtualPC::Tasks**</span></span>](ivmvirtualpc-tasks.md)
</dt> </dl>

 


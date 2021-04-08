---
title: 'IVMVirtualNetworkCollection 介面 (VPCCOMInterfaces .h) '
description: 定義 IVMVirtualNetwork 物件的集合。 若要取得 IVMVirtualNetworkCollection 物件，請使用 IVMVirtualPC VirtualNetworks 屬性。
ms.assetid: 3d595bc3-1a8d-4e09-a809-944d4dcdc675
keywords:
- IVMVirtualNetworkCollection 介面 Virtual PC
- IVMVirtualNetworkCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMVirtualNetworkCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76935fd4a67983847e211d8aa53f4a616bed9d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686303"
---
# <a name="ivmvirtualnetworkcollection-interface"></a><span data-ttu-id="67ec6-106">IVMVirtualNetworkCollection 介面</span><span class="sxs-lookup"><span data-stu-id="67ec6-106">IVMVirtualNetworkCollection interface</span></span>

<span data-ttu-id="67ec6-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="67ec6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="67ec6-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="67ec6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="67ec6-109">定義 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="67ec6-109">Defines a collection of [**IVMVirtualNetwork**](ivmvirtualnetwork.md) objects.</span></span> <span data-ttu-id="67ec6-110">若要取得 **IVMVirtualNetworkCollection** 物件，請使用 [**IVMVirtualPC：： VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="67ec6-110">To obtain an **IVMVirtualNetworkCollection** object, use the [**IVMVirtualPC::VirtualNetworks**](ivmvirtualpc-virtualnetworks.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="67ec6-111">成員</span><span class="sxs-lookup"><span data-stu-id="67ec6-111">Members</span></span>

<span data-ttu-id="67ec6-112">**IVMVirtualNetworkCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="67ec6-112">The **IVMVirtualNetworkCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="67ec6-113">**IVMVirtualNetworkCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="67ec6-113">**IVMVirtualNetworkCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="67ec6-114">屬性</span><span class="sxs-lookup"><span data-stu-id="67ec6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67ec6-115">屬性</span><span class="sxs-lookup"><span data-stu-id="67ec6-115">Properties</span></span>

<span data-ttu-id="67ec6-116">**IVMVirtualNetworkCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="67ec6-116">The **IVMVirtualNetworkCollection** interface has these properties.</span></span>



| <span data-ttu-id="67ec6-117">屬性</span><span class="sxs-lookup"><span data-stu-id="67ec6-117">Property</span></span>                                                             | <span data-ttu-id="67ec6-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="67ec6-118">Access type</span></span>          | <span data-ttu-id="67ec6-119">Description</span><span class="sxs-lookup"><span data-stu-id="67ec6-119">Description</span></span>                                                                                                   |
|:---------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67ec6-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="67ec6-120">**\_NewEnum**</span></span>](ivmvirtualnetworkcollection--newenum.md)<br/> | <span data-ttu-id="67ec6-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="67ec6-121">Read-only</span></span><br/> | <span data-ttu-id="67ec6-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="67ec6-122">An enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="67ec6-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="67ec6-123">**Count**</span></span>](ivmvirtualnetworkcollection-count.md)<br/>        | <span data-ttu-id="67ec6-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="67ec6-124">Read-only</span></span><br/> | <span data-ttu-id="67ec6-125">此集合中的虛擬網路數目。</span><span class="sxs-lookup"><span data-stu-id="67ec6-125">The number of virtual networks in this collection.</span></span><br/>                                                 |
| [<span data-ttu-id="67ec6-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="67ec6-126">**Item**</span></span>](ivmvirtualnetworkcollection-item.md)<br/>          | <span data-ttu-id="67ec6-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="67ec6-127">Read-only</span></span><br/> | <span data-ttu-id="67ec6-128">對應至指定之索引的 [**IVMVirtualNetwork**](ivmvirtualnetwork.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="67ec6-128">The [**IVMVirtualNetwork**](ivmvirtualnetwork.md) object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="67ec6-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="67ec6-129">Requirements</span></span>



| <span data-ttu-id="67ec6-130">需求</span><span class="sxs-lookup"><span data-stu-id="67ec6-130">Requirement</span></span> | <span data-ttu-id="67ec6-131">值</span><span class="sxs-lookup"><span data-stu-id="67ec6-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67ec6-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67ec6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67ec6-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67ec6-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="67ec6-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67ec6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67ec6-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="67ec6-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="67ec6-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="67ec6-136">End of client support</span></span><br/>    | <span data-ttu-id="67ec6-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="67ec6-137">Windows 7</span></span><br/>                                                                           |
| <span data-ttu-id="67ec6-138">產品</span><span class="sxs-lookup"><span data-stu-id="67ec6-138">Product</span></span><br/>                  | <span data-ttu-id="67ec6-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="67ec6-139">Windows Virtual PC</span></span><br/>                                                                  |
| <span data-ttu-id="67ec6-140">標頭</span><span class="sxs-lookup"><span data-stu-id="67ec6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="67ec6-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="67ec6-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>  |
| <span data-ttu-id="67ec6-142">IID</span><span class="sxs-lookup"><span data-stu-id="67ec6-142">IID</span></span><br/>                      | <span data-ttu-id="67ec6-143">IID \_ IVMVirtualNetworkCollection 定義為8ed680be-4242-4b2a-a21c-1982d8b0f675</span><span class="sxs-lookup"><span data-stu-id="67ec6-143">IID\_IVMVirtualNetworkCollection is defined as 8ed680be-4242-4b2a-a21c-1982d8b0f675</span></span><br/> |



 


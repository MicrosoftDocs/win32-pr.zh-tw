---
title: 'IVMHardDiskConnectionCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的硬碟連接集合。 若要取得 IVMHardDiskConnectionCollection 物件，請使用 IVMVirtualMachine HardDiskConnections 屬性。
ms.assetid: 3440318c-45f4-4d24-9609-dbe5ca59b005
keywords:
- IVMHardDiskConnectionCollection 介面 Virtual PC
- IVMHardDiskConnectionCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbde67f226c5b2d8cb86a8764c6dd61c24c2a468
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464185"
---
# <a name="ivmharddiskconnectioncollection-interface"></a><span data-ttu-id="43611-106">IVMHardDiskConnectionCollection 介面</span><span class="sxs-lookup"><span data-stu-id="43611-106">IVMHardDiskConnectionCollection interface</span></span>

<span data-ttu-id="43611-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="43611-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="43611-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="43611-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="43611-109">定義虛擬機器內的硬碟連接集合。</span><span class="sxs-lookup"><span data-stu-id="43611-109">Defines the collection of hard disk connections within the virtual machine.</span></span> <span data-ttu-id="43611-110">若要取得 **IVMHardDiskConnectionCollection** 物件，請使用 [**IVMVirtualMachine：： HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="43611-110">To obtain an **IVMHardDiskConnectionCollection** object, use the [**IVMVirtualMachine::HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="43611-111">成員</span><span class="sxs-lookup"><span data-stu-id="43611-111">Members</span></span>

<span data-ttu-id="43611-112">**IVMHardDiskConnectionCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="43611-112">The **IVMHardDiskConnectionCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="43611-113">**IVMHardDiskConnectionCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="43611-113">**IVMHardDiskConnectionCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="43611-114">屬性</span><span class="sxs-lookup"><span data-stu-id="43611-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43611-115">屬性</span><span class="sxs-lookup"><span data-stu-id="43611-115">Properties</span></span>

<span data-ttu-id="43611-116">**IVMHardDiskConnectionCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="43611-116">The **IVMHardDiskConnectionCollection** interface has these properties.</span></span>



| <span data-ttu-id="43611-117">屬性</span><span class="sxs-lookup"><span data-stu-id="43611-117">Property</span></span>                                                                 | <span data-ttu-id="43611-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="43611-118">Access type</span></span>          | <span data-ttu-id="43611-119">Description</span><span class="sxs-lookup"><span data-stu-id="43611-119">Description</span></span>                                                                         |
|:-------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="43611-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="43611-120">**\_NewEnum**</span></span>](ivmharddiskconnectioncollection--newenum.md)<br/> | <span data-ttu-id="43611-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="43611-121">Read-only</span></span><br/> | <span data-ttu-id="43611-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="43611-122">An enumerator for the collection.</span></span><br/>                                        |
| [<span data-ttu-id="43611-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="43611-123">**Count**</span></span>](ivmharddiskconnectioncollection-count.md)<br/>        | <span data-ttu-id="43611-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="43611-124">Read-only</span></span><br/> | <span data-ttu-id="43611-125">此集合中的硬碟連接數目。</span><span class="sxs-lookup"><span data-stu-id="43611-125">The number of hard disk connections in this collection.</span></span><br/>                  |
| [<span data-ttu-id="43611-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="43611-126">**Item**</span></span>](ivmharddiskconnectioncollection-item.md)<br/>          | <span data-ttu-id="43611-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="43611-127">Read-only</span></span><br/> | <span data-ttu-id="43611-128">對應至指定之索引的硬碟連線物件。</span><span class="sxs-lookup"><span data-stu-id="43611-128">The hard disk connection object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43611-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="43611-129">Requirements</span></span>



| <span data-ttu-id="43611-130">需求</span><span class="sxs-lookup"><span data-stu-id="43611-130">Requirement</span></span> | <span data-ttu-id="43611-131">值</span><span class="sxs-lookup"><span data-stu-id="43611-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43611-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="43611-132">Minimum supported client</span></span><br/> | <span data-ttu-id="43611-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="43611-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="43611-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="43611-134">Minimum supported server</span></span><br/> | <span data-ttu-id="43611-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="43611-135">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="43611-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="43611-136">End of client support</span></span><br/>    | <span data-ttu-id="43611-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43611-137">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="43611-138">產品</span><span class="sxs-lookup"><span data-stu-id="43611-138">Product</span></span><br/>                  | <span data-ttu-id="43611-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="43611-139">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="43611-140">標頭</span><span class="sxs-lookup"><span data-stu-id="43611-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="43611-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="43611-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="43611-142">IID</span><span class="sxs-lookup"><span data-stu-id="43611-142">IID</span></span><br/>                      | <span data-ttu-id="43611-143">IID \_ IVMHardDiskconnectionCollection 定義為 b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="43611-143">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43611-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43611-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43611-145">**IVMHardDiskConnection**</span><span class="sxs-lookup"><span data-stu-id="43611-145">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> <dt>

[<span data-ttu-id="43611-146">**IVMVirtualMachine::HardDiskConnections**</span><span class="sxs-lookup"><span data-stu-id="43611-146">**IVMVirtualMachine::HardDiskConnections**</span></span>](ivmvirtualmachine-harddiskconnections.md)
</dt> </dl>

 


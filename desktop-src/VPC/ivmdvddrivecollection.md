---
title: 'IVMDVDDriveCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器中的 CD 和 DVD 光碟機集合。 若要取得 IVMDVDDriveCollection 物件，請使用 IVMVirtualMachine DVDROMDrives 屬性。
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- IVMDVDDriveCollection 介面 Virtual PC
- IVMDVDDriveCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6afcf14a1ffe53dea0dcd7e21fcde8729e0bd0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976357"
---
# <a name="ivmdvddrivecollection-interface"></a><span data-ttu-id="50866-106">IVMDVDDriveCollection 介面</span><span class="sxs-lookup"><span data-stu-id="50866-106">IVMDVDDriveCollection interface</span></span>

<span data-ttu-id="50866-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="50866-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50866-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="50866-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50866-109">定義虛擬機器中的 CD 和 DVD 光碟機集合。</span><span class="sxs-lookup"><span data-stu-id="50866-109">Defines the collection of CD and DVD drives within the virtual machine.</span></span> <span data-ttu-id="50866-110">若要取得 **IVMDVDDriveCollection** 物件，請使用 [**IVMVirtualMachine：:D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="50866-110">To obtain an **IVMDVDDriveCollection** object, use the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="50866-111">成員</span><span class="sxs-lookup"><span data-stu-id="50866-111">Members</span></span>

<span data-ttu-id="50866-112">**IVMDVDDriveCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="50866-112">The **IVMDVDDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="50866-113">**IVMDVDDriveCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="50866-113">**IVMDVDDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="50866-114">屬性</span><span class="sxs-lookup"><span data-stu-id="50866-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50866-115">屬性</span><span class="sxs-lookup"><span data-stu-id="50866-115">Properties</span></span>

<span data-ttu-id="50866-116">**IVMDVDDriveCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="50866-116">The **IVMDVDDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="50866-117">屬性</span><span class="sxs-lookup"><span data-stu-id="50866-117">Property</span></span>                                                       | <span data-ttu-id="50866-118">存取類型</span><span class="sxs-lookup"><span data-stu-id="50866-118">Access type</span></span>          | <span data-ttu-id="50866-119">Description</span><span class="sxs-lookup"><span data-stu-id="50866-119">Description</span></span>                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="50866-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="50866-120">**\_NewEnum**</span></span>](ivmdvddrivecollection--newenum.md)<br/> | <span data-ttu-id="50866-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="50866-121">Read-only</span></span><br/> | <span data-ttu-id="50866-122">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="50866-122">An enumerator for the collection.</span></span><br/>                                   |
| [<span data-ttu-id="50866-123">**計數**</span><span class="sxs-lookup"><span data-stu-id="50866-123">**Count**</span></span>](ivmdvddrivecollection-count.md)<br/>        | <span data-ttu-id="50866-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="50866-124">Read-only</span></span><br/> | <span data-ttu-id="50866-125">此集合中的 CD 和 DVD 光碟機數目。</span><span class="sxs-lookup"><span data-stu-id="50866-125">The number of CD and DVD drives in this collection.</span></span><br/>                 |
| [<span data-ttu-id="50866-126">**項目**</span><span class="sxs-lookup"><span data-stu-id="50866-126">**Item**</span></span>](ivmdvddrivecollection-item.md)<br/>          | <span data-ttu-id="50866-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="50866-127">Read-only</span></span><br/> | <span data-ttu-id="50866-128">對應到指定之索引的 CD 或 DVD 光碟機物件。</span><span class="sxs-lookup"><span data-stu-id="50866-128">The CD or DVD drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50866-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="50866-129">Requirements</span></span>



| <span data-ttu-id="50866-130">需求</span><span class="sxs-lookup"><span data-stu-id="50866-130">Requirement</span></span> | <span data-ttu-id="50866-131">值</span><span class="sxs-lookup"><span data-stu-id="50866-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50866-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50866-132">Minimum supported client</span></span><br/> | <span data-ttu-id="50866-133">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50866-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50866-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50866-134">Minimum supported server</span></span><br/> | <span data-ttu-id="50866-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="50866-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50866-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="50866-136">End of client support</span></span><br/>    | <span data-ttu-id="50866-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50866-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50866-138">產品</span><span class="sxs-lookup"><span data-stu-id="50866-138">Product</span></span><br/>                  | <span data-ttu-id="50866-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50866-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50866-140">標頭</span><span class="sxs-lookup"><span data-stu-id="50866-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="50866-141"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="50866-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50866-142">IID</span><span class="sxs-lookup"><span data-stu-id="50866-142">IID</span></span><br/>                      | <span data-ttu-id="50866-143">IID \_ IVMDVDDriveCollection 定義為 bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="50866-143">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="50866-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50866-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50866-145">**IVMDVDDrive**</span><span class="sxs-lookup"><span data-stu-id="50866-145">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> <dt>

[<span data-ttu-id="50866-146">**IVMVirtualMachine：:D VDROMDrives**</span><span class="sxs-lookup"><span data-stu-id="50866-146">**IVMVirtualMachine::DVDROMDrives**</span></span>](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 


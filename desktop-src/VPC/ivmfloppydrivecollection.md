---
title: 'IVMFloppyDriveCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的一組磁片磁碟機。
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- IVMFloppyDriveCollection 介面 Virtual PC
- IVMFloppyDriveCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385238"
---
# <a name="ivmfloppydrivecollection-interface"></a><span data-ttu-id="47104-105">IVMFloppyDriveCollection 介面</span><span class="sxs-lookup"><span data-stu-id="47104-105">IVMFloppyDriveCollection interface</span></span>

<span data-ttu-id="47104-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="47104-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="47104-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="47104-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="47104-108">定義虛擬機器內的一組磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="47104-108">Defines a collection of floppy drives within the virtual machine.</span></span> <span data-ttu-id="47104-109">若要取得 **IVMFloppyDriveCollection** 物件，請使用 [**IVMVirtualMachine：： FloppyDrives**](ivmvirtualmachine-floppydrives.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="47104-109">To obtain an **IVMFloppyDriveCollection** object, use the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="47104-110">成員</span><span class="sxs-lookup"><span data-stu-id="47104-110">Members</span></span>

<span data-ttu-id="47104-111">**IVMFloppyDriveCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="47104-111">The **IVMFloppyDriveCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="47104-112">**IVMFloppyDriveCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="47104-112">**IVMFloppyDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="47104-113">屬性</span><span class="sxs-lookup"><span data-stu-id="47104-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47104-114">屬性</span><span class="sxs-lookup"><span data-stu-id="47104-114">Properties</span></span>

<span data-ttu-id="47104-115">**IVMFloppyDriveCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="47104-115">The **IVMFloppyDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="47104-116">屬性</span><span class="sxs-lookup"><span data-stu-id="47104-116">Property</span></span>                                                          | <span data-ttu-id="47104-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="47104-117">Access type</span></span>          | <span data-ttu-id="47104-118">Description</span><span class="sxs-lookup"><span data-stu-id="47104-118">Description</span></span>                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="47104-119">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="47104-119">**\_NewEnum**</span></span>](ivmfloppydrivecollection--newenum.md)<br/> | <span data-ttu-id="47104-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="47104-120">Read-only</span></span><br/> | <span data-ttu-id="47104-121">集合的列舉值。</span><span class="sxs-lookup"><span data-stu-id="47104-121">An enumerator for the collection.</span></span><br/>                                |
| [<span data-ttu-id="47104-122">**計數**</span><span class="sxs-lookup"><span data-stu-id="47104-122">**Count**</span></span>](ivmfloppydrivecollection-count.md)<br/>        | <span data-ttu-id="47104-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="47104-123">Read-only</span></span><br/> | <span data-ttu-id="47104-124">此集合中的磁片磁碟機數目。</span><span class="sxs-lookup"><span data-stu-id="47104-124">The number of floppy drives in this collection.</span></span><br/>                  |
| [<span data-ttu-id="47104-125">**項目**</span><span class="sxs-lookup"><span data-stu-id="47104-125">**Item**</span></span>](ivmfloppydrivecollection-item.md)<br/>          | <span data-ttu-id="47104-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="47104-126">Read-only</span></span><br/> | <span data-ttu-id="47104-127">對應至指定之索引的磁片磁碟機物件。</span><span class="sxs-lookup"><span data-stu-id="47104-127">The floppy drive object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="47104-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="47104-128">Requirements</span></span>



| <span data-ttu-id="47104-129">需求</span><span class="sxs-lookup"><span data-stu-id="47104-129">Requirement</span></span> | <span data-ttu-id="47104-130">值</span><span class="sxs-lookup"><span data-stu-id="47104-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="47104-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47104-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47104-132">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="47104-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47104-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="47104-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47104-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="47104-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="47104-135">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="47104-135">End of client support</span></span><br/>    | <span data-ttu-id="47104-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="47104-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="47104-137">產品</span><span class="sxs-lookup"><span data-stu-id="47104-137">Product</span></span><br/>                  | <span data-ttu-id="47104-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="47104-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="47104-139">標頭</span><span class="sxs-lookup"><span data-stu-id="47104-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="47104-140"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="47104-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="47104-141">IID</span><span class="sxs-lookup"><span data-stu-id="47104-141">IID</span></span><br/>                      | <span data-ttu-id="47104-142">IID \_ IVMFloppyDriveCollection 定義為8ba70a25-f698-4ee5-85ce-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="47104-142">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="47104-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47104-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47104-144">**IVMFloppyDrive**</span><span class="sxs-lookup"><span data-stu-id="47104-144">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="47104-145">**IVMVirtualMachine::FloppyDrives**</span><span class="sxs-lookup"><span data-stu-id="47104-145">**IVMVirtualMachine::FloppyDrives**</span></span>](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 


---
title: 'IVMFloppyDrive 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的軟碟磁碟機。
ms.assetid: b652182a-27ae-4390-81b1-b644a82924df
keywords:
- IVMFloppyDrive 介面 Virtual PC
- IVMFloppyDrive 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab1034bc56c5fe10bb12941bd99309e13e22dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934929"
---
# <a name="ivmfloppydrive-interface"></a><span data-ttu-id="65070-105">IVMFloppyDrive 介面</span><span class="sxs-lookup"><span data-stu-id="65070-105">IVMFloppyDrive interface</span></span>

<span data-ttu-id="65070-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="65070-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="65070-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="65070-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="65070-108">控制虛擬機器內的軟碟磁碟機。</span><span class="sxs-lookup"><span data-stu-id="65070-108">Controls a floppy drive within a virtual machine.</span></span> <span data-ttu-id="65070-109">**IVMFloppyDrive** 可以使用 [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) 的輸出介面，通知用戶端有關事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="65070-109">**IVMFloppyDrive** can notify clients about events using the [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md) outgoing interface.</span></span> <span data-ttu-id="65070-110">您可以從 [**IVMVirtualMachine：： FloppyDrives**](ivmvirtualmachine-floppydrives.md)屬性傳回的 [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)物件中取出 **IVMFloppyDrive** 物件。</span><span class="sxs-lookup"><span data-stu-id="65070-110">You can retrieve an **IVMFloppyDrive** object from the [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md) object returned from the [**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="65070-111">成員</span><span class="sxs-lookup"><span data-stu-id="65070-111">Members</span></span>

<span data-ttu-id="65070-112">**IVMFloppyDrive** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="65070-112">The **IVMFloppyDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="65070-113">**IVMFloppyDrive** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65070-113">**IVMFloppyDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="65070-114">方法</span><span class="sxs-lookup"><span data-stu-id="65070-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="65070-115">屬性</span><span class="sxs-lookup"><span data-stu-id="65070-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65070-116">方法</span><span class="sxs-lookup"><span data-stu-id="65070-116">Methods</span></span>

<span data-ttu-id="65070-117">**IVMFloppyDrive** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="65070-117">The **IVMFloppyDrive** interface has these methods.</span></span>



| <span data-ttu-id="65070-118">方法</span><span class="sxs-lookup"><span data-stu-id="65070-118">Method</span></span>                                                      | <span data-ttu-id="65070-119">描述</span><span class="sxs-lookup"><span data-stu-id="65070-119">Description</span></span>                                                                                  |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65070-120">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="65070-120">**AttachHostDrive**</span></span>](ivmfloppydrive-attachhostdrive.md)   | <span data-ttu-id="65070-121">將主機上的實體磁片磁碟機附加至虛擬機器中的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="65070-121">Attaches a physical drive on the host to the floppy drive in the virtual machine.</span></span><br/> |
| [<span data-ttu-id="65070-122">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="65070-122">**AttachImage**</span></span>](ivmfloppydrive-attachimage.md)           | <span data-ttu-id="65070-123">將主機上的軟碟媒體映射連接到磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="65070-123">Attaches a floppy media image on the host to the floppy drive.</span></span><br/>                    |
| [<span data-ttu-id="65070-124">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="65070-124">**ReleaseHostDrive**</span></span>](ivmfloppydrive-releasehostdrive.md) | <span data-ttu-id="65070-125">從軟碟磁碟機釋放主機上的實體磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="65070-125">Releases a physical drive on the host from the floppy drive.</span></span><br/>                      |
| [<span data-ttu-id="65070-126">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="65070-126">**ReleaseImage**</span></span>](ivmfloppydrive-releaseimage.md)         | <span data-ttu-id="65070-127">從軟碟磁碟機釋放主機上的軟碟媒體映射。</span><span class="sxs-lookup"><span data-stu-id="65070-127">Releases a floppy media image on the host from the floppy drive.</span></span><br/>                  |



 

### <a name="properties"></a><span data-ttu-id="65070-128">屬性</span><span class="sxs-lookup"><span data-stu-id="65070-128">Properties</span></span>

<span data-ttu-id="65070-129">**IVMFloppyDrive** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="65070-129">The **IVMFloppyDrive** interface has these properties.</span></span>



| <span data-ttu-id="65070-130">屬性</span><span class="sxs-lookup"><span data-stu-id="65070-130">Property</span></span>                                                             | <span data-ttu-id="65070-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="65070-131">Access type</span></span>          | <span data-ttu-id="65070-132">Description</span><span class="sxs-lookup"><span data-stu-id="65070-132">Description</span></span>                                                                               |
|:---------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65070-133">**附件**</span><span class="sxs-lookup"><span data-stu-id="65070-133">**Attachment**</span></span>](ivmfloppydrive-attachment.md)<br/>           | <span data-ttu-id="65070-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="65070-134">Read-only</span></span><br/> | <span data-ttu-id="65070-135">連接至虛擬機器中之磁片磁碟機的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="65070-135">The type of media attached to the floppy drive within the virtual machine.</span></span><br/>     |
| [<span data-ttu-id="65070-136">**DriveNumber**</span><span class="sxs-lookup"><span data-stu-id="65070-136">**DriveNumber**</span></span>](ivmfloppydrive-drivenumber.md)<br/>         | <span data-ttu-id="65070-137">唯讀</span><span class="sxs-lookup"><span data-stu-id="65070-137">Read-only</span></span><br/> | <span data-ttu-id="65070-138">連接此磁片磁碟機之控制器的以零為起始的索引。</span><span class="sxs-lookup"><span data-stu-id="65070-138">The zero-based index of the controller to which this floppy drive is attached.</span></span><br/> |
| [<span data-ttu-id="65070-139">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="65070-139">**HostDriveLetter**</span></span>](ivmfloppydrive-hostdriveletter.md)<br/> | <span data-ttu-id="65070-140">唯讀</span><span class="sxs-lookup"><span data-stu-id="65070-140">Read-only</span></span><br/> | <span data-ttu-id="65070-141">連接軟碟磁碟機的主機磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="65070-141">The letter of the host drive to which the floppy drive is attached.</span></span><br/>            |
| [<span data-ttu-id="65070-142">**映射檔**</span><span class="sxs-lookup"><span data-stu-id="65070-142">**ImageFile**</span></span>](ivmfloppydrive-imagefile.md)<br/>             | <span data-ttu-id="65070-143">唯讀</span><span class="sxs-lookup"><span data-stu-id="65070-143">Read-only</span></span><br/> | <span data-ttu-id="65070-144">連接軟碟磁碟機之影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="65070-144">The full path of the image file to which the floppy drive is attached.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="65070-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="65070-145">Requirements</span></span>



| <span data-ttu-id="65070-146">需求</span><span class="sxs-lookup"><span data-stu-id="65070-146">Requirement</span></span> | <span data-ttu-id="65070-147">值</span><span class="sxs-lookup"><span data-stu-id="65070-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65070-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65070-148">Minimum supported client</span></span><br/> | <span data-ttu-id="65070-149">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65070-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="65070-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65070-150">Minimum supported server</span></span><br/> | <span data-ttu-id="65070-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="65070-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="65070-152">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="65070-152">End of client support</span></span><br/>    | <span data-ttu-id="65070-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65070-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="65070-154">產品</span><span class="sxs-lookup"><span data-stu-id="65070-154">Product</span></span><br/>                  | <span data-ttu-id="65070-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="65070-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="65070-156">標頭</span><span class="sxs-lookup"><span data-stu-id="65070-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="65070-157"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="65070-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="65070-158">IID</span><span class="sxs-lookup"><span data-stu-id="65070-158">IID</span></span><br/>                      | <span data-ttu-id="65070-159">IID \_ IVMFloppyDrive 定義為661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="65070-159">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



 


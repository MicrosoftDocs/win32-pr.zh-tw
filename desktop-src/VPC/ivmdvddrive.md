---
title: 'IVMDVDDrive 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的 CD-ROM 或 DVD-ROM 光碟機。 IVMDVDDrive 可以使用 IVMDVDDriveEvents 的輸出介面，通知用戶端有關事件的資訊。
ms.assetid: 0900b3a8-ba52-4c26-bd96-b37334d6d03c
keywords:
- IVMDVDDrive 介面 Virtual PC
- IVMDVDDrive 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 951213923f74f8425fc4d9eaec85e76f7481eeb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025232"
---
# <a name="ivmdvddrive-interface"></a><span data-ttu-id="5792e-106">IVMDVDDrive 介面</span><span class="sxs-lookup"><span data-stu-id="5792e-106">IVMDVDDrive interface</span></span>

<span data-ttu-id="5792e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5792e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5792e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5792e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5792e-109">控制虛擬機器內的 CD-ROM 或 DVD-ROM 光碟機。</span><span class="sxs-lookup"><span data-stu-id="5792e-109">Controls a CD-ROM or DVD-ROM drive within a virtual machine.</span></span> <span data-ttu-id="5792e-110">**IVMDVDDrive** 可以使用 [**IVMDVDDriveEvents**](ivmdvddriveevents.md) 的輸出介面，通知用戶端有關事件的資訊。</span><span class="sxs-lookup"><span data-stu-id="5792e-110">**IVMDVDDrive** can notify clients about events using the [**IVMDVDDriveEvents**](ivmdvddriveevents.md) outgoing interface.</span></span>

<span data-ttu-id="5792e-111">您可以使用 [**IVMVirtualMachine：： AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) 方法，將新的 CD-ROM 或 dvd-rom 光碟機新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="5792e-111">You can add a new CD-ROM or DVD-ROM drive to a virtual machine using the [**IVMVirtualMachine::AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md) method.</span></span> <span data-ttu-id="5792e-112">您可以使用 [**IVMVirtualMachine：： RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) 方法，從虛擬機器移除現有的 CD-ROM 或 dvd-rom 光碟機。</span><span class="sxs-lookup"><span data-stu-id="5792e-112">You can remove an existing CD-ROM or DVD-ROM drive from a virtual machine using the [**IVMVirtualMachine::RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md) method.</span></span> <span data-ttu-id="5792e-113">您可以從 [**IVMVirtualMachine：:D vdromdrives**](ivmvirtualmachine-dvdromdrives.md)屬性傳回的 [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)物件中取出 **IVMDVDDrive** 物件。</span><span class="sxs-lookup"><span data-stu-id="5792e-113">You can retrieve an **IVMDVDDrive** object from the [**IVMDVDDriveCollection**](ivmdvddrivecollection.md) object returned from the [**IVMVirtualMachine::DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="5792e-114">成員</span><span class="sxs-lookup"><span data-stu-id="5792e-114">Members</span></span>

<span data-ttu-id="5792e-115">**IVMDVDDrive** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="5792e-115">The **IVMDVDDrive** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5792e-116">**IVMDVDDrive** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5792e-116">**IVMDVDDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="5792e-117">方法</span><span class="sxs-lookup"><span data-stu-id="5792e-117">Methods</span></span>](#methods)
-   [<span data-ttu-id="5792e-118">屬性</span><span class="sxs-lookup"><span data-stu-id="5792e-118">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5792e-119">方法</span><span class="sxs-lookup"><span data-stu-id="5792e-119">Methods</span></span>

<span data-ttu-id="5792e-120">**IVMDVDDrive** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5792e-120">The **IVMDVDDrive** interface has these methods.</span></span>



| <span data-ttu-id="5792e-121">方法</span><span class="sxs-lookup"><span data-stu-id="5792e-121">Method</span></span>                                                   | <span data-ttu-id="5792e-122">描述</span><span class="sxs-lookup"><span data-stu-id="5792e-122">Description</span></span>                                                                             |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5792e-123">**AttachHostDrive**</span><span class="sxs-lookup"><span data-stu-id="5792e-123">**AttachHostDrive**</span></span>](ivmdvddrive-attachhostdrive.md)   | <span data-ttu-id="5792e-124">將主機磁片磁碟機連接到虛擬機器中的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="5792e-124">Attaches a host drive to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="5792e-125">**AttachImage**</span><span class="sxs-lookup"><span data-stu-id="5792e-125">**AttachImage**</span></span>](ivmdvddrive-attachimage.md)           | <span data-ttu-id="5792e-126">將 ISO 映像連接到虛擬機器中的 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="5792e-126">Attaches an ISO image to the DVD drive within the virtual machine.</span></span><br/>           |
| [<span data-ttu-id="5792e-127">**ReleaseHostDrive**</span><span class="sxs-lookup"><span data-stu-id="5792e-127">**ReleaseHostDrive**</span></span>](ivmdvddrive-releasehostdrive.md) | <span data-ttu-id="5792e-128">從 DVD 光碟機釋放已捕捉的主機磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="5792e-128">Releases a captured host drive from the DVD drive.</span></span><br/>                           |
| [<span data-ttu-id="5792e-129">**ReleaseImage**</span><span class="sxs-lookup"><span data-stu-id="5792e-129">**ReleaseImage**</span></span>](ivmdvddrive-releaseimage.md)         | <span data-ttu-id="5792e-130">從 DVD 光碟機釋放已捕獲的 ISO 映像。</span><span class="sxs-lookup"><span data-stu-id="5792e-130">Releases a captured ISO image from the DVD drive.</span></span><br/>                            |
| [<span data-ttu-id="5792e-131">**SetBusLocation**</span><span class="sxs-lookup"><span data-stu-id="5792e-131">**SetBusLocation**</span></span>](ivmdvddrive-setbuslocation.md)     | <span data-ttu-id="5792e-132">將 DVD 光碟機連接到虛擬機器中指定的匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="5792e-132">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5792e-133">屬性</span><span class="sxs-lookup"><span data-stu-id="5792e-133">Properties</span></span>

<span data-ttu-id="5792e-134">**IVMDVDDrive** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="5792e-134">The **IVMDVDDrive** interface has these properties.</span></span>



| <span data-ttu-id="5792e-135">屬性</span><span class="sxs-lookup"><span data-stu-id="5792e-135">Property</span></span>                                                          | <span data-ttu-id="5792e-136">存取類型</span><span class="sxs-lookup"><span data-stu-id="5792e-136">Access type</span></span>          | <span data-ttu-id="5792e-137">Description</span><span class="sxs-lookup"><span data-stu-id="5792e-137">Description</span></span>                                                                        |
|:------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="5792e-138">**附件**</span><span class="sxs-lookup"><span data-stu-id="5792e-138">**Attachment**</span></span>](ivmdvddrive-attachment.md)<br/>           | <span data-ttu-id="5792e-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="5792e-139">Read-only</span></span><br/> | <span data-ttu-id="5792e-140">連接至虛擬機器內 DVD 光碟機的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5792e-140">The type of media attached to the DVD drive within the virtual machine.</span></span><br/> |
| [<span data-ttu-id="5792e-141">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="5792e-141">**BusNumber**</span></span>](ivmdvddrive-busnumber.md)<br/>             | <span data-ttu-id="5792e-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="5792e-142">Read-only</span></span><br/> | <span data-ttu-id="5792e-143">此裝置所連接的匯流排號碼。</span><span class="sxs-lookup"><span data-stu-id="5792e-143">The bus number to which this device is attached.</span></span><br/>                        |
| [<span data-ttu-id="5792e-144">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="5792e-144">**DeviceNumber**</span></span>](ivmdvddrive-devicenumber.md)<br/>       | <span data-ttu-id="5792e-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="5792e-145">Read-only</span></span><br/> | <span data-ttu-id="5792e-146">此磁片磁碟機所連接的裝置編號。</span><span class="sxs-lookup"><span data-stu-id="5792e-146">The device number to which this drive is attached.</span></span><br/>                      |
| [<span data-ttu-id="5792e-147">**HostDriveLetter**</span><span class="sxs-lookup"><span data-stu-id="5792e-147">**HostDriveLetter**</span></span>](ivmdvddrive-hostdriveletter.md)<br/> | <span data-ttu-id="5792e-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="5792e-148">Read-only</span></span><br/> | <span data-ttu-id="5792e-149">為此裝置設定之主機磁片磁碟機的字母。</span><span class="sxs-lookup"><span data-stu-id="5792e-149">The letter of the host drive set for this device.</span></span><br/>                       |
| [<span data-ttu-id="5792e-150">**映射檔**</span><span class="sxs-lookup"><span data-stu-id="5792e-150">**ImageFile**</span></span>](ivmdvddrive-imagefile.md)<br/>             | <span data-ttu-id="5792e-151">唯讀</span><span class="sxs-lookup"><span data-stu-id="5792e-151">Read-only</span></span><br/> | <span data-ttu-id="5792e-152">為此裝置設定之影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="5792e-152">The full path of the image file set for this device.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="5792e-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="5792e-153">Requirements</span></span>



| <span data-ttu-id="5792e-154">需求</span><span class="sxs-lookup"><span data-stu-id="5792e-154">Requirement</span></span> | <span data-ttu-id="5792e-155">值</span><span class="sxs-lookup"><span data-stu-id="5792e-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5792e-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5792e-156">Minimum supported client</span></span><br/> | <span data-ttu-id="5792e-157">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5792e-157">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5792e-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5792e-158">Minimum supported server</span></span><br/> | <span data-ttu-id="5792e-159">都不支援</span><span class="sxs-lookup"><span data-stu-id="5792e-159">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5792e-160">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5792e-160">End of client support</span></span><br/>    | <span data-ttu-id="5792e-161">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5792e-161">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5792e-162">產品</span><span class="sxs-lookup"><span data-stu-id="5792e-162">Product</span></span><br/>                  | <span data-ttu-id="5792e-163">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5792e-163">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5792e-164">標頭</span><span class="sxs-lookup"><span data-stu-id="5792e-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="5792e-165"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5792e-165"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5792e-166">IID</span><span class="sxs-lookup"><span data-stu-id="5792e-166">IID</span></span><br/>                      | <span data-ttu-id="5792e-167">IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="5792e-167">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



 


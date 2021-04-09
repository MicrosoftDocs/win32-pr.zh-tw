---
title: 'IVMDisplay 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器的顯示設定。 您可以使用 IVMVirtualMachine 顯示內容來抓取虛擬機器的 IVMDisplay 介面。
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- IVMDisplay 介面 Virtual PC
- IVMDisplay 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934755"
---
# <a name="ivmdisplay-interface"></a><span data-ttu-id="22202-106">IVMDisplay 介面</span><span class="sxs-lookup"><span data-stu-id="22202-106">IVMDisplay interface</span></span>

<span data-ttu-id="22202-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="22202-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="22202-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="22202-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="22202-109">控制虛擬機器的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="22202-109">Controls the display settings of a virtual machine.</span></span> <span data-ttu-id="22202-110">您可以使用 [**IVMVirtualMachine：:D isplay**](ivmvirtualmachine-display.md)屬性來抓取虛擬機器的 **IVMDisplay** 介面。</span><span class="sxs-lookup"><span data-stu-id="22202-110">The **IVMDisplay** interface for a virtual machine can be retrieved using the [**IVMVirtualMachine::Display**](ivmvirtualmachine-display.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="22202-111">成員</span><span class="sxs-lookup"><span data-stu-id="22202-111">Members</span></span>

<span data-ttu-id="22202-112">**IVMDisplay** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="22202-112">The **IVMDisplay** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="22202-113">**IVMDisplay** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="22202-113">**IVMDisplay** also has these types of members:</span></span>

-   [<span data-ttu-id="22202-114">方法</span><span class="sxs-lookup"><span data-stu-id="22202-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="22202-115">屬性</span><span class="sxs-lookup"><span data-stu-id="22202-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="22202-116">方法</span><span class="sxs-lookup"><span data-stu-id="22202-116">Methods</span></span>

<span data-ttu-id="22202-117">**IVMDisplay** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="22202-117">The **IVMDisplay** interface has these methods.</span></span>



| <span data-ttu-id="22202-118">方法</span><span class="sxs-lookup"><span data-stu-id="22202-118">Method</span></span>                                                       | <span data-ttu-id="22202-119">描述</span><span class="sxs-lookup"><span data-stu-id="22202-119">Description</span></span>                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22202-120">**\_GenerateThumbnail**</span><span class="sxs-lookup"><span data-stu-id="22202-120">**\_GenerateThumbnail**</span></span>](ivmdisplay--generatethumbnail.md) | <span data-ttu-id="22202-121">抓取圖元的陣列，表示虛擬機器畫面的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="22202-121">Retrieves an array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="22202-122">**SetDimensions**</span><span class="sxs-lookup"><span data-stu-id="22202-122">**SetDimensions**</span></span>](ivmdisplay-setdimensions.md)            | <span data-ttu-id="22202-123">設定虛擬機器顯示的高度和寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="22202-123">Sets the height and width of the virtual machine's display, in pixels.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="22202-124">屬性</span><span class="sxs-lookup"><span data-stu-id="22202-124">Properties</span></span>

<span data-ttu-id="22202-125">**IVMDisplay** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="22202-125">The **IVMDisplay** interface has these properties.</span></span>



| <span data-ttu-id="22202-126">屬性</span><span class="sxs-lookup"><span data-stu-id="22202-126">Property</span></span>                                             | <span data-ttu-id="22202-127">存取類型</span><span class="sxs-lookup"><span data-stu-id="22202-127">Access type</span></span>          | <span data-ttu-id="22202-128">Description</span><span class="sxs-lookup"><span data-stu-id="22202-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22202-129">**Graphicswindow.canresize**</span><span class="sxs-lookup"><span data-stu-id="22202-129">**CanResize**</span></span>](ivmdisplay-canresize.md)<br/> | <span data-ttu-id="22202-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="22202-130">Read-only</span></span><br/> | <span data-ttu-id="22202-131">指出來賓是否允許解析變更。</span><span class="sxs-lookup"><span data-stu-id="22202-131">Indicates whether the Guest allows resolution changes.</span></span><br/>                             |
| [<span data-ttu-id="22202-132">**高度**</span><span class="sxs-lookup"><span data-stu-id="22202-132">**Height**</span></span>](ivmdisplay-height.md)<br/>       | <span data-ttu-id="22202-133">唯讀</span><span class="sxs-lookup"><span data-stu-id="22202-133">Read-only</span></span><br/> | <span data-ttu-id="22202-134">虛擬機器的顯示高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="22202-134">The height of the virtual machine's display, in pixels.</span></span><br/>                            |
| [<span data-ttu-id="22202-135">**縮圖**</span><span class="sxs-lookup"><span data-stu-id="22202-135">**Thumbnail**</span></span>](ivmdisplay-thumbnail.md)<br/> | <span data-ttu-id="22202-136">唯讀</span><span class="sxs-lookup"><span data-stu-id="22202-136">Read-only</span></span><br/> | <span data-ttu-id="22202-137">圖元的陣列，表示虛擬機器畫面的縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="22202-137">An array of pixels representing a thumbnail image of the virtual machine's screen.</span></span><br/> |
| [<span data-ttu-id="22202-138">**VideoMode**</span><span class="sxs-lookup"><span data-stu-id="22202-138">**VideoMode**</span></span>](ivmdisplay-videomode.md)<br/> | <span data-ttu-id="22202-139">唯讀</span><span class="sxs-lookup"><span data-stu-id="22202-139">Read-only</span></span><br/> | <span data-ttu-id="22202-140">目前的影片模式 (文字、VGA、SVGA 等) 。</span><span class="sxs-lookup"><span data-stu-id="22202-140">The current video mode (Text, VGA, SVGA, and so on).</span></span><br/>                               |
| [<span data-ttu-id="22202-141">**寬度**</span><span class="sxs-lookup"><span data-stu-id="22202-141">**Width**</span></span>](ivmdisplay-width.md)<br/>         | <span data-ttu-id="22202-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="22202-142">Read-only</span></span><br/> | <span data-ttu-id="22202-143">虛擬機器的顯示寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="22202-143">The width of the virtual machine's display, in pixels.</span></span><br/>                             |



 

## <a name="requirements"></a><span data-ttu-id="22202-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="22202-144">Requirements</span></span>



| <span data-ttu-id="22202-145">需求</span><span class="sxs-lookup"><span data-stu-id="22202-145">Requirement</span></span> | <span data-ttu-id="22202-146">值</span><span class="sxs-lookup"><span data-stu-id="22202-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="22202-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22202-147">Minimum supported client</span></span><br/> | <span data-ttu-id="22202-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22202-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22202-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22202-149">Minimum supported server</span></span><br/> | <span data-ttu-id="22202-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="22202-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="22202-151">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="22202-151">End of client support</span></span><br/>    | <span data-ttu-id="22202-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="22202-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="22202-153">產品</span><span class="sxs-lookup"><span data-stu-id="22202-153">Product</span></span><br/>                  | <span data-ttu-id="22202-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="22202-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="22202-155">標頭</span><span class="sxs-lookup"><span data-stu-id="22202-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="22202-156"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="22202-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="22202-157">IID</span><span class="sxs-lookup"><span data-stu-id="22202-157">IID</span></span><br/>                      | <span data-ttu-id="22202-158">IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="22202-158">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



 


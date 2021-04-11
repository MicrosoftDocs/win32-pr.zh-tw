---
title: 'IVMMouse 介面 (VPCCOMInterfaces .h) '
description: 控制 VM 內的滑鼠裝置。
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- IVMMouse 介面 Virtual PC
- IVMMouse 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844148"
---
# <a name="ivmmouse-interface"></a><span data-ttu-id="a4641-105">IVMMouse 介面</span><span class="sxs-lookup"><span data-stu-id="a4641-105">IVMMouse interface</span></span>

<span data-ttu-id="a4641-106">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="a4641-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a4641-107">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="a4641-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a4641-108">控制虛擬機器 (VM) 內的滑鼠裝置。</span><span class="sxs-lookup"><span data-stu-id="a4641-108">Controls the mouse device within a virtual machine (VM).</span></span> <span data-ttu-id="a4641-109">您可以使用 [**IVMVirtualMachine：：滑鼠**](ivmvirtualmachine-mouse.md)屬性來抓取虛擬機器的 **IVMMouse** 。</span><span class="sxs-lookup"><span data-stu-id="a4641-109">The **IVMMouse** for a virtual machine can be retrieved using the [**IVMVirtualMachine::Mouse**](ivmvirtualmachine-mouse.md) property.</span></span> <span data-ttu-id="a4641-110">滑鼠裝置的座標可以用絕對座標或 delta 座標表示。</span><span class="sxs-lookup"><span data-stu-id="a4641-110">Coordinates for the mouse device can be represented either in absolute coordinates or in delta coordinates.</span></span> <span data-ttu-id="a4641-111">您可以使用 [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) 屬性來區別兩個座標標記法。</span><span class="sxs-lookup"><span data-stu-id="a4641-111">Use the [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md) property to distinguish between the two methods of coordinate representation.</span></span> <span data-ttu-id="a4641-112">請注意，只有在客體作業系統已安裝整合元件時，才支援抓取目前的資料指標位置和絕對座標的使用。</span><span class="sxs-lookup"><span data-stu-id="a4641-112">Note that retrieving the current cursor position and the use of absolute coordinates are only supported if the guest operating system has the integration components installed.</span></span>

## <a name="members"></a><span data-ttu-id="a4641-113">成員</span><span class="sxs-lookup"><span data-stu-id="a4641-113">Members</span></span>

<span data-ttu-id="a4641-114">**IVMMouse** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="a4641-114">The **IVMMouse** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="a4641-115">**IVMMouse** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a4641-115">**IVMMouse** also has these types of members:</span></span>

-   [<span data-ttu-id="a4641-116">方法</span><span class="sxs-lookup"><span data-stu-id="a4641-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="a4641-117">屬性</span><span class="sxs-lookup"><span data-stu-id="a4641-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a4641-118">方法</span><span class="sxs-lookup"><span data-stu-id="a4641-118">Methods</span></span>

<span data-ttu-id="a4641-119">**IVMMouse** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="a4641-119">The **IVMMouse** interface has these methods.</span></span>



| <span data-ttu-id="a4641-120">方法</span><span class="sxs-lookup"><span data-stu-id="a4641-120">Method</span></span>                                  | <span data-ttu-id="a4641-121">描述</span><span class="sxs-lookup"><span data-stu-id="a4641-121">Description</span></span>                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a4641-122">**按一下**</span><span class="sxs-lookup"><span data-stu-id="a4641-122">**Click**</span></span>](ivmmouse-click.md)         | <span data-ttu-id="a4641-123">模擬滑鼠按鍵的點擊。</span><span class="sxs-lookup"><span data-stu-id="a4641-123">Simulates a mouse button click.</span></span><br/>                                         |
| [<span data-ttu-id="a4641-124">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="a4641-124">**GetButton**</span></span>](ivmmouse-getbutton.md) | <span data-ttu-id="a4641-125">抓取所指定滑鼠按鍵的目前狀態 (向上或向下) 。</span><span class="sxs-lookup"><span data-stu-id="a4641-125">Retrieves the current state (up or down) of the specified mouse button.</span></span><br/> |
| [<span data-ttu-id="a4641-126">**SetButton**</span><span class="sxs-lookup"><span data-stu-id="a4641-126">**SetButton**</span></span>](ivmmouse-setbutton.md) | <span data-ttu-id="a4641-127">將目前狀態 () 指定的滑鼠按鍵。</span><span class="sxs-lookup"><span data-stu-id="a4641-127">Sets the current state (up or down) of the specified mouse button.</span></span><br/>      |



 

### <a name="properties"></a><span data-ttu-id="a4641-128">屬性</span><span class="sxs-lookup"><span data-stu-id="a4641-128">Properties</span></span>

<span data-ttu-id="a4641-129">**IVMMouse** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a4641-129">The **IVMMouse** interface has these properties.</span></span>



| <span data-ttu-id="a4641-130">屬性</span><span class="sxs-lookup"><span data-stu-id="a4641-130">Property</span></span>                                                                         | <span data-ttu-id="a4641-131">存取類型</span><span class="sxs-lookup"><span data-stu-id="a4641-131">Access type</span></span>           | <span data-ttu-id="a4641-132">Description</span><span class="sxs-lookup"><span data-stu-id="a4641-132">Description</span></span>                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a4641-133">**HorizontalPosition**</span><span class="sxs-lookup"><span data-stu-id="a4641-133">**HorizontalPosition**</span></span>](ivmmouse-horizontalposition.md)<br/>             | <span data-ttu-id="a4641-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4641-134">Read/write</span></span><br/> | <span data-ttu-id="a4641-135">滑鼠的絕對 x 座標。</span><span class="sxs-lookup"><span data-stu-id="a4641-135">The absolute x-coordinate of the mouse.</span></span><br/>                                         |
| [<span data-ttu-id="a4641-136">**ScrollWheelPosition**</span><span class="sxs-lookup"><span data-stu-id="a4641-136">**ScrollWheelPosition**</span></span>](ivmmouse-scrollwheelposition.md)<br/>           | <span data-ttu-id="a4641-137">唯寫</span><span class="sxs-lookup"><span data-stu-id="a4641-137">Write-only</span></span><br/> | <span data-ttu-id="a4641-138">滑鼠 (相對於) 的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="a4641-138">The z-coordinate of the mouse (relative only).</span></span><br/>                                  |
| [<span data-ttu-id="a4641-139">**UsingAbsoluteCoordinates**</span><span class="sxs-lookup"><span data-stu-id="a4641-139">**UsingAbsoluteCoordinates**</span></span>](ivmmouse-usingabsolutecoordinates.md)<br/> | <span data-ttu-id="a4641-140">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4641-140">Read/write</span></span><br/> | <span data-ttu-id="a4641-141">指出滑鼠座標是否代表絕對或相對座標。</span><span class="sxs-lookup"><span data-stu-id="a4641-141">Indicates whether mouse coordinates represent absolute or relative coordinates.</span></span><br/> |
| [<span data-ttu-id="a4641-142">**VerticalPosition**</span><span class="sxs-lookup"><span data-stu-id="a4641-142">**VerticalPosition**</span></span>](ivmmouse-verticalposition.md)<br/>                 | <span data-ttu-id="a4641-143">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="a4641-143">Read/write</span></span><br/> | <span data-ttu-id="a4641-144">滑鼠的絕對 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a4641-144">The absolute y-coordinate of the mouse.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="a4641-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4641-145">Requirements</span></span>



| <span data-ttu-id="a4641-146">需求</span><span class="sxs-lookup"><span data-stu-id="a4641-146">Requirement</span></span> | <span data-ttu-id="a4641-147">值</span><span class="sxs-lookup"><span data-stu-id="a4641-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4641-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4641-148">Minimum supported client</span></span><br/> | <span data-ttu-id="a4641-149">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4641-149">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4641-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4641-150">Minimum supported server</span></span><br/> | <span data-ttu-id="a4641-151">都不支援</span><span class="sxs-lookup"><span data-stu-id="a4641-151">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a4641-152">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a4641-152">End of client support</span></span><br/>    | <span data-ttu-id="a4641-153">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a4641-153">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a4641-154">產品</span><span class="sxs-lookup"><span data-stu-id="a4641-154">Product</span></span><br/>                  | <span data-ttu-id="a4641-155">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a4641-155">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a4641-156">標頭</span><span class="sxs-lookup"><span data-stu-id="a4641-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4641-157"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="a4641-157"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a4641-158">IID</span><span class="sxs-lookup"><span data-stu-id="a4641-158">IID</span></span><br/>                      | <span data-ttu-id="a4641-159">IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="a4641-159">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



 


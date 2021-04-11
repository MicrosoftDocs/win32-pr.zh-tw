---
description: IWiaItem2 介面提供與 IWiaItem 介面相同功能的應用程式 (能夠查詢裝置以探索其功能、存取資料傳輸介面和專案屬性，以及控制裝置) 。
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: 'IWiaItem2 介面 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848071"
---
# <a name="iwiaitem2-interface"></a><span data-ttu-id="1284c-103">IWiaItem2 介面</span><span class="sxs-lookup"><span data-stu-id="1284c-103">IWiaItem2 interface</span></span>

<span data-ttu-id="1284c-104">**IWiaItem2** 介面提供與 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面相同功能的應用程式 (能夠查詢裝置以探索其功能、存取資料傳輸介面和專案屬性，以及控制裝置) 。</span><span class="sxs-lookup"><span data-stu-id="1284c-104">The **IWiaItem2** interface provides applications with the same functionality as the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface (the ability to query devices to discover their capabilities, to access data transfer interfaces and item properties, and to control the device).</span></span> <span data-ttu-id="1284c-105">它也提供應用程式動態建立和使用影像處理篩選的能力，而這些篩選器可作為 windows Vista 中提供的 Windows 映像取得 (WIA) 2.0 設備磁碟機的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="1284c-105">It also provides application with the ability to dynamically create and use image processing filters that can come as extensions of the Windows Image Acquisition (WIA) 2.0 device drivers provided in Windows Vista.</span></span>

## <a name="members"></a><span data-ttu-id="1284c-106">成員</span><span class="sxs-lookup"><span data-stu-id="1284c-106">Members</span></span>

<span data-ttu-id="1284c-107">**IWiaItem2** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="1284c-107">The **IWiaItem2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1284c-108">**IWiaItem2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1284c-108">**IWiaItem2** also has these types of members:</span></span>

-   [<span data-ttu-id="1284c-109">方法</span><span class="sxs-lookup"><span data-stu-id="1284c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1284c-110">方法</span><span class="sxs-lookup"><span data-stu-id="1284c-110">Methods</span></span>

<span data-ttu-id="1284c-111">**IWiaItem2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="1284c-111">The **IWiaItem2** interface has these methods.</span></span>



| <span data-ttu-id="1284c-112">方法</span><span class="sxs-lookup"><span data-stu-id="1284c-112">Method</span></span>                                                                  | <span data-ttu-id="1284c-113">描述</span><span class="sxs-lookup"><span data-stu-id="1284c-113">Description</span></span>                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1284c-114">**CheckExtension**</span><span class="sxs-lookup"><span data-stu-id="1284c-114">**CheckExtension**</span></span>](-wia-iwiaitem2-checkextension.md)                 | <span data-ttu-id="1284c-115">檢查指定的延伸模組是否可在電腦上使用，並可供 [**IWiaItem2：： GetExtension**](-wia-iwiaitem2-getextension.md) 方法使用。</span><span class="sxs-lookup"><span data-stu-id="1284c-115">Checks whether a specified extension is available on the machine and can be used by the [**IWiaItem2::GetExtension**](-wia-iwiaitem2-getextension.md) method.</span></span> <br/>                                   |
| [<span data-ttu-id="1284c-116">**CreateChildItem**</span><span class="sxs-lookup"><span data-stu-id="1284c-116">**CreateChildItem**</span></span>](-wia-iwiaitem2-createchilditem.md)               | <span data-ttu-id="1284c-117">建立新的子專案。</span><span class="sxs-lookup"><span data-stu-id="1284c-117">Create a new child item.</span></span> <span data-ttu-id="1284c-118">將 **IWiaItem2** 物件新增至裝置的 **IWiaItem2** 樹狀目錄。</span><span class="sxs-lookup"><span data-stu-id="1284c-118">Adds **IWiaItem2** objects to a device's **IWiaItem2** tree.</span></span> <br/>                                                                                                            |
| [<span data-ttu-id="1284c-119">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="1284c-119">**DeleteItem**</span></span>](-wia-iwiaitem2-deleteitem.md)                         | <span data-ttu-id="1284c-120">從裝置的物件樹狀結構中移除目前的 **IWiaItem2** 物件。</span><span class="sxs-lookup"><span data-stu-id="1284c-120">Removes the current **IWiaItem2** object from the device's object tree.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="1284c-121">**DeviceCommand**</span><span class="sxs-lookup"><span data-stu-id="1284c-121">**DeviceCommand**</span></span>](-wia-iwiaitem2-devicecommand.md)                   | <span data-ttu-id="1284c-122">發出命令給 WIA 2.0 硬體裝置。</span><span class="sxs-lookup"><span data-stu-id="1284c-122">Issues a command to a WIA 2.0 hardware device.</span></span> <br/>                                                                                                                                                   |
| [<span data-ttu-id="1284c-123">**DeviceDlg**</span><span class="sxs-lookup"><span data-stu-id="1284c-123">**DeviceDlg**</span></span>](-wia-iwiaitem2-devicedlg.md)                           | <span data-ttu-id="1284c-124">顯示對話方塊，讓使用者準備取得影像。</span><span class="sxs-lookup"><span data-stu-id="1284c-124">Displays a dialog box to the user to prepare for image acquisition.</span></span> <br/>                                                                                                                              |
| [<span data-ttu-id="1284c-125">**Diagnostic**</span><span class="sxs-lookup"><span data-stu-id="1284c-125">**Diagnostic**</span></span>](-wia-iwiaitem2-diagnostic.md)                         | <span data-ttu-id="1284c-126">目前不支援。</span><span class="sxs-lookup"><span data-stu-id="1284c-126">Not currently supported.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="1284c-127">**EnumChildItems**</span><span class="sxs-lookup"><span data-stu-id="1284c-127">**EnumChildItems**</span></span>](-wia-iwiaitem2-enumchilditems.md)                 | <span data-ttu-id="1284c-128">建立列舉值物件，並將其 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面的指標傳回給 WIA 2.0 裝置之 **IWiaItem2** 樹狀目錄中的專案資料夾。</span><span class="sxs-lookup"><span data-stu-id="1284c-128">Creates an enumerator object and passes back a pointer to its [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) interface for folders with items in the **IWiaItem2** tree of a WIA 2.0 device.</span></span> <br/>        |
| [<span data-ttu-id="1284c-129">**EnumDeviceCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1284c-129">**EnumDeviceCapabilities**</span></span>](-wia-iwiaitem2-enumdevicecapabilities.md) | <span data-ttu-id="1284c-130">建立用來確定 WIA 2.0 裝置支援的命令和事件的列舉值。</span><span class="sxs-lookup"><span data-stu-id="1284c-130">Creates an enumerator that is used to ascertain the commands and events a WIA 2.0 device supports.</span></span> <br/>                                                                                               |
| [<span data-ttu-id="1284c-131">**EnumRegisterEventInfo**</span><span class="sxs-lookup"><span data-stu-id="1284c-131">**EnumRegisterEventInfo**</span></span>](-wia-iwiaitem2-enumregistereventinfo.md)   | <span data-ttu-id="1284c-132">[**IWiaItem2：： EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)方法會建立用來取得已註冊應用程式之事件相關資訊的列舉值。</span><span class="sxs-lookup"><span data-stu-id="1284c-132">The [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) method creates an enumerator used to obtain information about events for which an application is registered.</span></span><br/> |
| [<span data-ttu-id="1284c-133">**FindItemByName**</span><span class="sxs-lookup"><span data-stu-id="1284c-133">**FindItemByName**</span></span>](-wia-iwiaitem2-finditembyname.md)                 | <span data-ttu-id="1284c-134">使用名稱做為搜尋索引鍵，在專案的子專案樹狀目錄中搜尋。</span><span class="sxs-lookup"><span data-stu-id="1284c-134">Searches an item's tree of subitems using the name as the search key.</span></span> <br/>                                                                                                                            |
| [<span data-ttu-id="1284c-135">**GetExtension**</span><span class="sxs-lookup"><span data-stu-id="1284c-135">**GetExtension**</span></span>](-wia-iwiaitem2-getextension.md)                     | <span data-ttu-id="1284c-136">取得可能隨附于 WIA 2.0 設備磁碟機的延伸模組介面。</span><span class="sxs-lookup"><span data-stu-id="1284c-136">Gets the extension interfaces that might come with a WIA 2.0 device driver.</span></span> <br/>                                                                                                                      |
| [<span data-ttu-id="1284c-137">**GetItemCategory**</span><span class="sxs-lookup"><span data-stu-id="1284c-137">**GetItemCategory**</span></span>](-wia-iwiaitem2-getitemcategory.md)               | <span data-ttu-id="1284c-138">取得專案的類別目錄資訊。</span><span class="sxs-lookup"><span data-stu-id="1284c-138">Gets an item's category information.</span></span> <br/>                                                                                                                                                             |
| [<span data-ttu-id="1284c-139">**GetItemType**</span><span class="sxs-lookup"><span data-stu-id="1284c-139">**GetItemType**</span></span>](-wia-iwiaitem2-getitemtype.md)                       | <span data-ttu-id="1284c-140">取得專案的類型資訊。</span><span class="sxs-lookup"><span data-stu-id="1284c-140">Gets an item's type information.</span></span> <br/>                                                                                                                                                                 |
| [<span data-ttu-id="1284c-141">**GetParentItem**</span><span class="sxs-lookup"><span data-stu-id="1284c-141">**GetParentItem**</span></span>](-wia-iwiaitem2-getparentitem.md)                   | <span data-ttu-id="1284c-142">取得樹狀結構中表示 WIA 2.0 硬體裝置的父專案。</span><span class="sxs-lookup"><span data-stu-id="1284c-142">Gets the parent item in the tree that represents a WIA 2.0 hardware device.</span></span> <br/>                                                                                                                      |
| [<span data-ttu-id="1284c-143">**GetPreviewComponent**</span><span class="sxs-lookup"><span data-stu-id="1284c-143">**GetPreviewComponent**</span></span>](-wia-iwiaitem2-getpreviewcomponent.md)       | <span data-ttu-id="1284c-144">取得 WIA 2.0 預覽元件。</span><span class="sxs-lookup"><span data-stu-id="1284c-144">Gets the WIA 2.0 preview component.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="1284c-145">**GetRootItem**</span><span class="sxs-lookup"><span data-stu-id="1284c-145">**GetRootItem**</span></span>](-wia-iwiaitem2-getrootitem.md)                       | <span data-ttu-id="1284c-146">取得用來表示 WIA 2.0 硬體裝置之專案物件樹狀結構的根專案。</span><span class="sxs-lookup"><span data-stu-id="1284c-146">Gets the root item of a tree of item objects used to represent a WIA 2.0 hardware device.</span></span> <br/>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="1284c-147">備註</span><span class="sxs-lookup"><span data-stu-id="1284c-147">Remarks</span></span>

<span data-ttu-id="1284c-148">應用程式可以看到的 WIA 2.0 專案樹狀結構與 WIA 2.0 迷你驅動程式所建立和維護的樹狀結構不同。</span><span class="sxs-lookup"><span data-stu-id="1284c-148">The WIA 2.0 item tree that an application can see is separate from the tree that is created and maintained by a WIA 2.0 minidriver.</span></span> <span data-ttu-id="1284c-149">當迷你驅動程式建立專案樹狀時，WIA 2.0 服務會使用此 WIA 2.0 專案樹狀結構作為指南，以建立可供影像處理應用程式查看的相同複本。</span><span class="sxs-lookup"><span data-stu-id="1284c-149">When a minidriver creates a tree of items, the WIA 2.0 Service uses this WIA 2.0 item tree as a guide to create identical copies that can be viewed by imaging applications.</span></span> <span data-ttu-id="1284c-150">複製之樹狀結構中的專案稱為應用程式專案。</span><span class="sxs-lookup"><span data-stu-id="1284c-150">Items in the copied tree are called application items.</span></span> <span data-ttu-id="1284c-151">迷你驅動程式所建立之樹狀結構中的專案稱為驅動程式專案。</span><span class="sxs-lookup"><span data-stu-id="1284c-151">Items in the tree created by a minidriver are called driver items.</span></span> <span data-ttu-id="1284c-152">在 Windows Vista 中，WIA 2.0 專案樹狀結構是內建的 **IWiaItem2** 物件，其中每個物件都會執行 **IWiaItem2** 介面) 。</span><span class="sxs-lookup"><span data-stu-id="1284c-152">In Windows Vista the WIA 2.0 item trees are built of **IWiaItem2** objects, each one of which implements the **IWiaItem2** interface).</span></span>

<span data-ttu-id="1284c-153">**IWiaItem2** 介面（如同所有元件物件模型 (COM) 介面）會繼承 [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面方法。</span><span class="sxs-lookup"><span data-stu-id="1284c-153">The **IWiaItem2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="1284c-154">IUnknown 方法</span><span class="sxs-lookup"><span data-stu-id="1284c-154">IUnknown Methods</span></span>                                        | <span data-ttu-id="1284c-155">Description</span><span class="sxs-lookup"><span data-stu-id="1284c-155">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="1284c-156">[IUnknown：： QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="1284c-156">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="1284c-157">傳回受支援介面的指標。</span><span class="sxs-lookup"><span data-stu-id="1284c-157">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="1284c-158">IUnknown：： AddRef</span><span class="sxs-lookup"><span data-stu-id="1284c-158">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="1284c-159">遞增參考次數。</span><span class="sxs-lookup"><span data-stu-id="1284c-159">Increments reference count.</span></span>               |
| [<span data-ttu-id="1284c-160">IUnknown：： Release</span><span class="sxs-lookup"><span data-stu-id="1284c-160">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="1284c-161">遞減參考次數。</span><span class="sxs-lookup"><span data-stu-id="1284c-161">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="1284c-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="1284c-162">Requirements</span></span>



| <span data-ttu-id="1284c-163">需求</span><span class="sxs-lookup"><span data-stu-id="1284c-163">Requirement</span></span> | <span data-ttu-id="1284c-164">值</span><span class="sxs-lookup"><span data-stu-id="1284c-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1284c-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1284c-165">Minimum supported client</span></span><br/> | <span data-ttu-id="1284c-166">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1284c-166">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1284c-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1284c-167">Minimum supported server</span></span><br/> | <span data-ttu-id="1284c-168">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1284c-168">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1284c-169">標頭</span><span class="sxs-lookup"><span data-stu-id="1284c-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="1284c-170"><dt>Wia</dt></span><span class="sxs-lookup"><span data-stu-id="1284c-170"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="1284c-171">Idl</span><span class="sxs-lookup"><span data-stu-id="1284c-171">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1284c-172"><dt>Wia .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1284c-172"><dt>Wia.idl</dt></span></span> </dl> |



 

 

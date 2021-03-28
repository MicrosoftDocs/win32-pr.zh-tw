---
description: 當使用者以滑鼠右鍵按一下 Shell 物件時，顯示的快捷方式功能表通常會包含屬性專案。
title: 屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 72233ab5-212d-498c-8df1-1a96c8eda892
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 40ccb8d1cee0fffb993aef417b979816597cf707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850035"
---
# <a name="property-sheet-handlers"></a><span data-ttu-id="22cc0-103">屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="22cc0-103">Property Sheet Handlers</span></span>

<span data-ttu-id="22cc0-104">當使用者以滑鼠右鍵按一下 Shell 物件時，顯示的快捷方式功能表通常會包含 **屬性** 專案。</span><span class="sxs-lookup"><span data-stu-id="22cc0-104">When a user right-clicks a Shell object, the shortcut menu that is displayed normally includes a **Properties** item.</span></span> <span data-ttu-id="22cc0-105">選取該專案會啟動屬性工作表，讓使用者能夠在某些情況下，修改物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="22cc0-105">Selecting that item launches a property sheet that allows the user to view, and in some cases modify, the object's properties.</span></span> <span data-ttu-id="22cc0-106">您可以藉由執行和註冊 *屬性工作表處理常式* 來自訂此屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-106">You can customize this property sheet by implementing and registering a *property sheet handler*.</span></span>

<span data-ttu-id="22cc0-107">[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。</span><span class="sxs-lookup"><span data-stu-id="22cc0-107">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="22cc0-108">本檔著重于屬性工作表處理常式特定的執行層面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-108">This document focuses on those aspects of implementation that are specific to property sheet handlers.</span></span>

-   [<span data-ttu-id="22cc0-109">屬性工作表處理常式的運作方式</span><span class="sxs-lookup"><span data-stu-id="22cc0-109">How Property Sheet Handlers Work</span></span>](#how-property-sheet-handlers-work)
-   [<span data-ttu-id="22cc0-110">註冊和執行已載入之磁片磁碟機的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="22cc0-110">Registering and Implementing a Property Sheet Handler for a Mounted Drive</span></span>](#registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive)
-   [<span data-ttu-id="22cc0-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="22cc0-111">Related topics</span></span>](#related-topics)

## <a name="how-property-sheet-handlers-work"></a><span data-ttu-id="22cc0-112">屬性工作表處理常式的運作方式</span><span class="sxs-lookup"><span data-stu-id="22cc0-112">How Property Sheet Handlers Work</span></span>

<span data-ttu-id="22cc0-113">下圖顯示 Windows XP 文字檔的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-113">The following illustration shows the Properties property sheet for a Windows XP text file.</span></span>

![屬性工作表](images/propsheethandler1.jpg)

<span data-ttu-id="22cc0-115">下圖顯示針對任何檔案顯示的 [預設屬性] 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-115">This illustration shows the default Properties property sheet that is displayed for any file.</span></span> <span data-ttu-id="22cc0-116">針對許多這類屬性工作表，您可以藉由執行和註冊屬性工作表處理常式，將一或多個頁面加入至屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-116">For many such property sheets, you can add one or more pages to the property sheet by implementing and registering a property sheet handler.</span></span>

<span data-ttu-id="22cc0-117">屬性工作表處理常式最常針對 [檔案類型](fa-file-types.md)進行註冊。</span><span class="sxs-lookup"><span data-stu-id="22cc0-117">Property sheet handlers are most commonly registered for a [file type](fa-file-types.md).</span></span> <span data-ttu-id="22cc0-118">每個處理常式都可以將一個自訂頁面加入至類別的 [屬性] 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-118">Each handler can add one custom page to the Properties property sheet for the class.</span></span> <span data-ttu-id="22cc0-119">這些頁面通常會讓使用者存取特定檔案類型的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="22cc0-119">These pages typically give users access to properties that are specific to the particular file type.</span></span> <span data-ttu-id="22cc0-120">例如，包含文字檔的檔案類型可以顯示列出標題和作者的頁面，以及檔的摘要。</span><span class="sxs-lookup"><span data-stu-id="22cc0-120">A file type consisting of text documents could, for instance, display a page that listed the title and author, and an abstract of the document.</span></span> <span data-ttu-id="22cc0-121">這種屬性工作表處理常式類型的特殊案例，是用來將頁面新增至載入之磁片磁碟機的 [屬性] 屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-121">A special case of this type of property sheet handler is used to add a page to the Properties property sheet for a mounted drive.</span></span>

<span data-ttu-id="22cc0-122">屬性工作表處理常式的另一個用法是取代主控台應用程式所顯示之屬性工作表中的頁面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-122">The other use for property sheet handlers is to replace pages in the property sheets displayed by Control Panel applications.</span></span> <span data-ttu-id="22cc0-123">比方說，滑鼠製造商可以使用屬性工作表處理常式來取代主控台的 **滑鼠屬性**] 屬性頁上的 [**按鈕**] 頁面，以及針對其滑鼠特性自訂的頁面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-123">A mouse manufacturer, for instance, can use a property sheet handler to replace the **Buttons** page on the Control Panel's **Mouse Properties** property sheet with a page that is customized for the characteristics of its mouse.</span></span>

<span data-ttu-id="22cc0-124">就像所有 Shell 擴充處理常式一樣，屬性工作表處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。</span><span class="sxs-lookup"><span data-stu-id="22cc0-124">Like all Shell extension handlers, property sheet handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="22cc0-125">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 和 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)之外，它們還必須匯出兩個介面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-125">They must export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext).</span></span>

<span data-ttu-id="22cc0-126">Shell 會使用 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面來初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="22cc0-126">The [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface is used by the Shell to initialize the handler.</span></span> <span data-ttu-id="22cc0-127">當 Shell 呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)時，它會傳入具有物件名稱的資料物件，而專案識別碼清單的指標 (PIDL 包含該檔案之資料夾的) 。</span><span class="sxs-lookup"><span data-stu-id="22cc0-127">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name, and the pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="22cc0-128">*HRegKey* 參數未與屬性工作表處理常式一起使用。</span><span class="sxs-lookup"><span data-stu-id="22cc0-128">The *hRegKey* parameter is not used with property sheet handlers.</span></span> <span data-ttu-id="22cc0-129">**IShellExtInit：： Initialize** 方法必須從資料物件中解壓縮檔案名稱，並儲存名稱和資料夾的 PIDL，以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="22cc0-129">The **IShellExtInit::Initialize** method must extract the file name from the data object, and store the name and the folder's PIDL for later use.</span></span> <span data-ttu-id="22cc0-130">For further details, see the *Implementing IShellExtInit* section of [Creating Shell Extension Handlers](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="22cc0-130">For further details, see the *Implementing IShellExtInit* section of [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="22cc0-131">作業的其餘部分會透過處理常式的 [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) 介面進行。</span><span class="sxs-lookup"><span data-stu-id="22cc0-131">The remainder of the operation takes place through the handler's [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="22cc0-132">如果屬性工作表與檔案類型相關聯，則 Shell 會呼叫 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) ，以允許處理常式將頁面加入至屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-132">If the property sheet is associated with a file type, the Shell calls [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) to allow the handler to add a page to the property sheet.</span></span> <span data-ttu-id="22cc0-133">如果屬性工作表與主控台的應用程式相關聯，則 Shell 會呼叫 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) ，以允許處理常式取代頁面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-133">If the property sheet is associated with a Control Panel application, the Shell calls [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) to allow the handler to replace a page.</span></span>

## <a name="registering-and-implementing-a-property-sheet-handler-for-a-mounted-drive"></a><span data-ttu-id="22cc0-134">註冊和執行已載入之磁片磁碟機的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="22cc0-134">Registering and Implementing a Property Sheet Handler for a Mounted Drive</span></span>

<span data-ttu-id="22cc0-135">每個掛接的磁片磁碟機都有一個可由使用者顯示的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-135">Each mounted drive has a Properties sheet that can be displayed by the user.</span></span> <span data-ttu-id="22cc0-136">下圖顯示 CD-ROM 光碟機的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="22cc0-136">The following illustration shows a Properties property sheet for a CD-ROM drive.</span></span>

![cd-rom 屬性工作表](images/propsheethandler2.jpg)

<span data-ttu-id="22cc0-138">有各式各樣的裝置可掛接為磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="22cc0-138">There are a wide variety of devices that can be mounted as drives.</span></span> <span data-ttu-id="22cc0-139">由於預設的屬性工作表（專為磁片磁碟機設計）可能無法滿足某些裝置的需求，因此可以實行屬性工作表處理常式來新增所掛接裝置的特定頁面。</span><span class="sxs-lookup"><span data-stu-id="22cc0-139">Because the default property sheet, designed for disk drives, might not be sufficient for some devices, a property sheet handler can be implemented to add a page that is specific to the mounted device.</span></span> <span data-ttu-id="22cc0-140">這種類型的屬性工作表處理常式的基本執行 [方式與如何針對檔案類型註冊和執行屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)中所討論的一樣，有兩個例外狀況。</span><span class="sxs-lookup"><span data-stu-id="22cc0-140">The basic implementation of this type of property sheet handler is identical to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md), with two exceptions.</span></span>

-   <span data-ttu-id="22cc0-141">傳遞給處理常式之 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) 方法的資料物件可能包含 [CFSTR \_ MOUNTEDVOLUME](clipboard.md) 格式的磁片磁碟機路徑，而不是 [CF \_ HDROP](clipboard.md) 格式。</span><span class="sxs-lookup"><span data-stu-id="22cc0-141">The data object passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method may contain the drive path in the [CFSTR\_MOUNTEDVOLUME](clipboard.md) format instead of the [CF\_HDROP](clipboard.md) format.</span></span> <span data-ttu-id="22cc0-142">\_當裝置掛接到磁碟機號時，會使用 CF HDROP 格式。</span><span class="sxs-lookup"><span data-stu-id="22cc0-142">The CF\_HDROP format is used when the device is mounted to a drive letter.</span></span> <span data-ttu-id="22cc0-143">\_當遠端裝置掛接到資料夾而非磁碟機號時，CFSTR MOUNTEDVOLUME 格式會與 NTFS 檔案系統搭配使用。</span><span class="sxs-lookup"><span data-stu-id="22cc0-143">The CFSTR\_MOUNTEDVOLUME format is used with NTFS file systems when the remote device is mounted to a folder rather than to a drive letter.</span></span>
-   <span data-ttu-id="22cc0-144">處理常式的 GUID 會在 **HKEY 類別的 \_ \_ 根** \\ **磁片磁碟機** \\ **shellex** \\ **PropertySheetHandlers** 金鑰下註冊。</span><span class="sxs-lookup"><span data-stu-id="22cc0-144">The handler's GUID is registered under the **HKEY\_CLASSES\_ROOT**\\**Drive**\\**shellex**\\**PropertySheetHandlers** key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22cc0-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="22cc0-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22cc0-146">如何註冊及執行檔案類型的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="22cc0-146">How to Register and Implement a Property Sheet Handler for a File Type</span></span>](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)
</dt> <dt>

[<span data-ttu-id="22cc0-147">如何註冊和執行主控台應用程式的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="22cc0-147">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>](how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application.md)
</dt> </dl>

 

 

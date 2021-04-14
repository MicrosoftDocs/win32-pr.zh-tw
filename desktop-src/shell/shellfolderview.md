---
description: 代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: 'ShellFolderView 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991722"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="8b248-103">ShellFolderView 物件</span><span class="sxs-lookup"><span data-stu-id="8b248-103">ShellFolderView object</span></span>

<span data-ttu-id="8b248-104">代表視圖中的物件，並提供用來取得視圖內容相關資訊的屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="8b248-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="8b248-105">成員</span><span class="sxs-lookup"><span data-stu-id="8b248-105">Members</span></span>

<span data-ttu-id="8b248-106">**ShellFolderView** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="8b248-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="8b248-107">事件</span><span class="sxs-lookup"><span data-stu-id="8b248-107">Events</span></span>](#events)
-   [<span data-ttu-id="8b248-108">方法</span><span class="sxs-lookup"><span data-stu-id="8b248-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="8b248-109">屬性</span><span class="sxs-lookup"><span data-stu-id="8b248-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="8b248-110">事件</span><span class="sxs-lookup"><span data-stu-id="8b248-110">Events</span></span>

<span data-ttu-id="8b248-111">**ShellFolderView** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="8b248-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="8b248-112">事件</span><span class="sxs-lookup"><span data-stu-id="8b248-112">Event</span></span>                                                        | <span data-ttu-id="8b248-113">描述</span><span class="sxs-lookup"><span data-stu-id="8b248-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b248-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="8b248-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="8b248-115">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="8b248-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="8b248-116">方法</span><span class="sxs-lookup"><span data-stu-id="8b248-116">Methods</span></span>

<span data-ttu-id="8b248-117">**ShellFolderView** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="8b248-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="8b248-118">方法</span><span class="sxs-lookup"><span data-stu-id="8b248-118">Method</span></span>                                                 | <span data-ttu-id="8b248-119">描述</span><span class="sxs-lookup"><span data-stu-id="8b248-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b248-120">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="8b248-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="8b248-121">為指定的專案建立快捷方式功能表，並傳回選取的命令字串。</span><span class="sxs-lookup"><span data-stu-id="8b248-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="8b248-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="8b248-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="8b248-123">取得 [**FolderItems**](folderitems.md) 物件，這個物件表示視圖中所有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="8b248-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="8b248-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="8b248-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="8b248-125">在視圖中設定專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="8b248-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="8b248-126">屬性</span><span class="sxs-lookup"><span data-stu-id="8b248-126">Properties</span></span>

<span data-ttu-id="8b248-127">**ShellFolderView** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="8b248-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="8b248-128">屬性</span><span class="sxs-lookup"><span data-stu-id="8b248-128">Property</span></span>                                                      | <span data-ttu-id="8b248-129">存取類型</span><span class="sxs-lookup"><span data-stu-id="8b248-129">Access type</span></span>          | <span data-ttu-id="8b248-130">Description</span><span class="sxs-lookup"><span data-stu-id="8b248-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8b248-131">**Application**</span><span class="sxs-lookup"><span data-stu-id="8b248-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="8b248-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-132">Read-only</span></span><br/> | <span data-ttu-id="8b248-133">包含物件的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="8b248-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="8b248-134">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="8b248-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="8b248-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-135">Read-only</span></span><br/> | <span data-ttu-id="8b248-136">取得代表具有輸入焦點之專案的 [**FolderItem**](folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8b248-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="8b248-137">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="8b248-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="8b248-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-138">Read-only</span></span><br/> | <span data-ttu-id="8b248-139">取得代表視圖的 [**資料夾**](folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8b248-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="8b248-140">**父代**</span><span class="sxs-lookup"><span data-stu-id="8b248-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="8b248-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-141">Read-only</span></span><br/> | <span data-ttu-id="8b248-142">未實作。</span><span class="sxs-lookup"><span data-stu-id="8b248-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="8b248-143">**腳本**</span><span class="sxs-lookup"><span data-stu-id="8b248-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="8b248-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-144">Read-only</span></span><br/> | <span data-ttu-id="8b248-145">已取代。</span><span class="sxs-lookup"><span data-stu-id="8b248-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="8b248-146">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="8b248-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="8b248-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="8b248-147">Read-only</span></span><br/> | <span data-ttu-id="8b248-148">取得一組旗標，指出視圖的目前選項。</span><span class="sxs-lookup"><span data-stu-id="8b248-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="8b248-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b248-149">Requirements</span></span>



| <span data-ttu-id="8b248-150">需求</span><span class="sxs-lookup"><span data-stu-id="8b248-150">Requirement</span></span> | <span data-ttu-id="8b248-151">值</span><span class="sxs-lookup"><span data-stu-id="8b248-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b248-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b248-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8b248-153">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b248-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8b248-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b248-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8b248-155">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b248-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8b248-156">標頭</span><span class="sxs-lookup"><span data-stu-id="8b248-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b248-157"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="8b248-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8b248-158">Idl</span><span class="sxs-lookup"><span data-stu-id="8b248-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8b248-159"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8b248-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8b248-160">DLL</span><span class="sxs-lookup"><span data-stu-id="8b248-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b248-161"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8b248-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="8b248-162">IID</span><span class="sxs-lookup"><span data-stu-id="8b248-162">IID</span></span><br/>                      | <span data-ttu-id="8b248-163">CLSID \_ ShellFolderView</span><span class="sxs-lookup"><span data-stu-id="8b248-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="8b248-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8b248-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b248-165">**ShellFolderViewOptions 旗標**</span><span class="sxs-lookup"><span data-stu-id="8b248-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 





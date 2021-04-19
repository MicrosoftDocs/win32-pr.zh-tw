---
title: WebViewFolderContents 物件 (Shldisp.h)
description: 由 Shell 所執行，可在 Web 工作內使用。
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- WebViewFolderContents 物件舊版 Windows 環境功能
- WebViewFolderContents 物件舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980285"
---
# <a name="webviewfoldercontents-object"></a><span data-ttu-id="d18a3-105">WebViewFolderContents 物件</span><span class="sxs-lookup"><span data-stu-id="d18a3-105">WebViewFolderContents object</span></span>

<span data-ttu-id="d18a3-106">由 Shell 所執行，可在 *web* 工作內使用。</span><span class="sxs-lookup"><span data-stu-id="d18a3-106">Implemented by the Shell for use inside a *WebView*.</span></span> <span data-ttu-id="d18a3-107">**WebViewFolderContents** 會自動將自己初始化為 web 上的目前資料夾。</span><span class="sxs-lookup"><span data-stu-id="d18a3-107">**WebViewFolderContents** automatically initializes itself to WebView's current folder.</span></span> <span data-ttu-id="d18a3-108">它會建立 Shell 資料夾檢視，以下列五種格式的其中一種來顯示資料夾的內容：小型圖示、大型圖示、清單、詳細資料或縮圖。</span><span class="sxs-lookup"><span data-stu-id="d18a3-108">It creates a Shell folder view that displays the contents of the folder in one of five formats: Small Icon, Large Icon, List, Details, or Thumbnail.</span></span> <span data-ttu-id="d18a3-109">它在 Web 程式外部無效。</span><span class="sxs-lookup"><span data-stu-id="d18a3-109">It is not valid outside of a WebView.</span></span>

<span data-ttu-id="d18a3-110">**WebViewFolderContents** 所公開的方法和屬性與 [**ShellFolderView**](/windows/desktop/shell/shellfolderview)物件的方法和屬性相同。</span><span class="sxs-lookup"><span data-stu-id="d18a3-110">The methods and properties exposed by **WebViewFolderContents** are identical to those of the [**ShellFolderView**](/windows/desktop/shell/shellfolderview) object.</span></span>

## <a name="members"></a><span data-ttu-id="d18a3-111">成員</span><span class="sxs-lookup"><span data-stu-id="d18a3-111">Members</span></span>

<span data-ttu-id="d18a3-112">**WebViewFolderContents** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d18a3-112">The **WebViewFolderContents** object has these types of members:</span></span>

-   [<span data-ttu-id="d18a3-113">事件</span><span class="sxs-lookup"><span data-stu-id="d18a3-113">Events</span></span>](#events)
-   [<span data-ttu-id="d18a3-114">方法</span><span class="sxs-lookup"><span data-stu-id="d18a3-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="d18a3-115">屬性</span><span class="sxs-lookup"><span data-stu-id="d18a3-115">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="d18a3-116">事件</span><span class="sxs-lookup"><span data-stu-id="d18a3-116">Events</span></span>

<span data-ttu-id="d18a3-117">**WebViewFolderContents** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="d18a3-117">The **WebViewFolderContents** object has these events.</span></span>



| <span data-ttu-id="d18a3-118">事件</span><span class="sxs-lookup"><span data-stu-id="d18a3-118">Event</span></span>                                                              | <span data-ttu-id="d18a3-119">描述</span><span class="sxs-lookup"><span data-stu-id="d18a3-119">Description</span></span>                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d18a3-120">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="d18a3-120">**SelectionChanged**</span></span>](webviewfoldercontents-selectionchanged.md) | <span data-ttu-id="d18a3-121">發生于視圖中任何專案或專案的選取狀態變更時。</span><span class="sxs-lookup"><span data-stu-id="d18a3-121">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d18a3-122">方法</span><span class="sxs-lookup"><span data-stu-id="d18a3-122">Methods</span></span>

<span data-ttu-id="d18a3-123">**WebViewFolderContents** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d18a3-123">The **WebViewFolderContents** object has these methods.</span></span>



| <span data-ttu-id="d18a3-124">方法</span><span class="sxs-lookup"><span data-stu-id="d18a3-124">Method</span></span>                                                       | <span data-ttu-id="d18a3-125">描述</span><span class="sxs-lookup"><span data-stu-id="d18a3-125">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d18a3-126">**PopupItemMenu**</span><span class="sxs-lookup"><span data-stu-id="d18a3-126">**PopupItemMenu**</span></span>](webviewfoldercontents-popupitemmenu.md) | <span data-ttu-id="d18a3-127">為指定的專案建立快捷方式功能表，並傳回選取的命令字串。</span><span class="sxs-lookup"><span data-stu-id="d18a3-127">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                   |
| [<span data-ttu-id="d18a3-128">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="d18a3-128">**SelectedItems**</span></span>](webviewfoldercontents-selecteditems.md) | <span data-ttu-id="d18a3-129">取得 [**FolderItems**](../shell/folderitems.md) 物件，這個物件表示視圖中所有選取的專案。</span><span class="sxs-lookup"><span data-stu-id="d18a3-129">Gets a [**FolderItems**](../shell/folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="d18a3-130">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="d18a3-130">**SelectItem**</span></span>](webviewfoldercontents-selectitem.md)       | <span data-ttu-id="d18a3-131">在視圖中設定專案的選取狀態。</span><span class="sxs-lookup"><span data-stu-id="d18a3-131">Sets the selection state of an item in the view.</span></span><br/>                                                          |



 

### <a name="properties"></a><span data-ttu-id="d18a3-132">屬性</span><span class="sxs-lookup"><span data-stu-id="d18a3-132">Properties</span></span>

<span data-ttu-id="d18a3-133">**WebViewFolderContents** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d18a3-133">The **WebViewFolderContents** object has these properties.</span></span>



| <span data-ttu-id="d18a3-134">屬性</span><span class="sxs-lookup"><span data-stu-id="d18a3-134">Property</span></span>                                                            | <span data-ttu-id="d18a3-135">存取類型</span><span class="sxs-lookup"><span data-stu-id="d18a3-135">Access type</span></span>          | <span data-ttu-id="d18a3-136">Description</span><span class="sxs-lookup"><span data-stu-id="d18a3-136">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d18a3-137">**Application**</span><span class="sxs-lookup"><span data-stu-id="d18a3-137">**Application**</span></span>](webviewfoldercontents-application.md)<br/> | <span data-ttu-id="d18a3-138">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-138">Read-only</span></span><br/> | <span data-ttu-id="d18a3-139">未實作。</span><span class="sxs-lookup"><span data-stu-id="d18a3-139">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d18a3-140">**FocusedItem**</span><span class="sxs-lookup"><span data-stu-id="d18a3-140">**FocusedItem**</span></span>](webviewfoldercontents-focuseditem.md)<br/> | <span data-ttu-id="d18a3-141">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-141">Read-only</span></span><br/> | <span data-ttu-id="d18a3-142">取得代表具有輸入焦點之專案的 [**FolderItem**](../shell/folderitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d18a3-142">Gets a [**FolderItem**](../shell/folderitem.md) object that represents the item that has the input focus.</span></span><br/>                           |
| [<span data-ttu-id="d18a3-143">**資料夾**</span><span class="sxs-lookup"><span data-stu-id="d18a3-143">**Folder**</span></span>](webviewfoldercontents-folder.md)<br/>           | <span data-ttu-id="d18a3-144">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-144">Read-only</span></span><br/> | <span data-ttu-id="d18a3-145">取得代表視圖的 [**資料夾**](../shell/folder.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d18a3-145">Gets a [**Folder**](../shell/folder.md) object that represents the view.</span></span><br/>                                                            |
| [<span data-ttu-id="d18a3-146">**父代**</span><span class="sxs-lookup"><span data-stu-id="d18a3-146">**Parent**</span></span>](webviewfoldercontents-parent.md)<br/>           | <span data-ttu-id="d18a3-147">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-147">Read-only</span></span><br/> | <span data-ttu-id="d18a3-148">未實作。</span><span class="sxs-lookup"><span data-stu-id="d18a3-148">Not implemented.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d18a3-149">**腳本**</span><span class="sxs-lookup"><span data-stu-id="d18a3-149">**Script**</span></span>](webviewfoldercontents-script.md)<br/>           | <span data-ttu-id="d18a3-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-150">Read-only</span></span><br/> | <span data-ttu-id="d18a3-151">取得視圖的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="d18a3-151">Gets the scripting object for the view.</span></span><br/>                                                                                       |
| [<span data-ttu-id="d18a3-152">**ViewOptions**</span><span class="sxs-lookup"><span data-stu-id="d18a3-152">**ViewOptions**</span></span>](webviewfoldercontents-viewoptions.md)<br/> | <span data-ttu-id="d18a3-153">唯讀</span><span class="sxs-lookup"><span data-stu-id="d18a3-153">Read-only</span></span><br/> | <span data-ttu-id="d18a3-154">取得一組 [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) 旗標，指出視圖的目前選項。</span><span class="sxs-lookup"><span data-stu-id="d18a3-154">Gets a set of [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) flags that indicate the current options of the view.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d18a3-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="d18a3-155">Requirements</span></span>



| <span data-ttu-id="d18a3-156">需求</span><span class="sxs-lookup"><span data-stu-id="d18a3-156">Requirement</span></span> | <span data-ttu-id="d18a3-157">值</span><span class="sxs-lookup"><span data-stu-id="d18a3-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d18a3-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d18a3-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d18a3-159">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d18a3-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d18a3-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d18a3-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d18a3-161">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d18a3-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d18a3-162">標頭</span><span class="sxs-lookup"><span data-stu-id="d18a3-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="d18a3-163"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d18a3-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d18a3-164">Idl</span><span class="sxs-lookup"><span data-stu-id="d18a3-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d18a3-165"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d18a3-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d18a3-166">DLL</span><span class="sxs-lookup"><span data-stu-id="d18a3-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d18a3-167"><dt>Shell32.dll (4.71 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d18a3-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 


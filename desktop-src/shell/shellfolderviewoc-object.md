---
description: 將指定之 ShellFolderView 物件所引發的事件轉送到對應的 ShellFolderViewOC 事件處理常式。
title: 'ShellFolderViewOC 物件 (Shldisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945005"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="0c874-103">ShellFolderViewOC 物件</span><span class="sxs-lookup"><span data-stu-id="0c874-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="0c874-104">將指定之 [**ShellFolderView**](shellfolderview.md) 物件所引發的事件轉送到對應的 **ShellFolderViewOC** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0c874-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="0c874-105">成員</span><span class="sxs-lookup"><span data-stu-id="0c874-105">Members</span></span>

<span data-ttu-id="0c874-106">**ShellFolderViewOC** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0c874-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="0c874-107">事件</span><span class="sxs-lookup"><span data-stu-id="0c874-107">Events</span></span>](#events)
-   [<span data-ttu-id="0c874-108">方法</span><span class="sxs-lookup"><span data-stu-id="0c874-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="0c874-109">事件</span><span class="sxs-lookup"><span data-stu-id="0c874-109">Events</span></span>

<span data-ttu-id="0c874-110">**ShellFolderViewOC** 物件具有這些事件。</span><span class="sxs-lookup"><span data-stu-id="0c874-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="0c874-111">事件</span><span class="sxs-lookup"><span data-stu-id="0c874-111">Event</span></span>                                                          | <span data-ttu-id="0c874-112">描述</span><span class="sxs-lookup"><span data-stu-id="0c874-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c874-113">**EnumDone**</span><span class="sxs-lookup"><span data-stu-id="0c874-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="0c874-114">指出 [**ShellFolderView**](shellfolderview.md) 物件已完成資料夾內容的列舉。</span><span class="sxs-lookup"><span data-stu-id="0c874-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="0c874-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="0c874-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="0c874-116">指出視圖中一個或多個專案的選取狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="0c874-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="0c874-117">方法</span><span class="sxs-lookup"><span data-stu-id="0c874-117">Methods</span></span>

<span data-ttu-id="0c874-118">**ShellFolderViewOC** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0c874-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="0c874-119">方法</span><span class="sxs-lookup"><span data-stu-id="0c874-119">Method</span></span>                                                   | <span data-ttu-id="0c874-120">描述</span><span class="sxs-lookup"><span data-stu-id="0c874-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c874-121">**SetFolderView**</span><span class="sxs-lookup"><span data-stu-id="0c874-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="0c874-122">將指定之 [**ShellFolderView**](shellfolderview.md) 物件的事件轉送至對應的 **ShellFolderViewOC** 事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="0c874-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c874-123">備註</span><span class="sxs-lookup"><span data-stu-id="0c874-123">Remarks</span></span>

<span data-ttu-id="0c874-124">[**ShellFolderView**](shellfolderview.md)物件會引發兩個 [**EnumDone**](shellfolderviewoc-enumdone.md)和 [**SelectionChanged**](shellfolderviewoc-selectionchanged.md)這兩個事件，通常是由應用程式處理。</span><span class="sxs-lookup"><span data-stu-id="0c874-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="0c874-125">不過，有些應用程式必須處理來自一系列 **ShellFolderView** 物件的事件。</span><span class="sxs-lookup"><span data-stu-id="0c874-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="0c874-126">例如，應用程式可能會裝載 WebBrowser 控制項，讓使用者能夠流覽一系列的資料夾。</span><span class="sxs-lookup"><span data-stu-id="0c874-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="0c874-127">每個資料夾都有自己的 **ShellFolderView** 物件及其相關聯的事件。</span><span class="sxs-lookup"><span data-stu-id="0c874-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="0c874-128">處理這些事件可能很困難。</span><span class="sxs-lookup"><span data-stu-id="0c874-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="0c874-129">**ShellFolderViewOC** 物件可簡化這類案例的事件處理。</span><span class="sxs-lookup"><span data-stu-id="0c874-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="0c874-130">它可讓應用程式使用一對 **ShellFolderViewOC** 事件處理常式來處理所有 [**ShellFolderView**](shellfolderview.md)物件的事件。</span><span class="sxs-lookup"><span data-stu-id="0c874-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="0c874-131">每次使用者流覽至新資料夾時，應用程式會藉由呼叫 [**SetFolderView**](shellfolderviewoc-setfolderview.md)將相關聯的 **ShellFolderView** 物件傳遞至 **ShellFolderViewOC** 物件。</span><span class="sxs-lookup"><span data-stu-id="0c874-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="0c874-132">然後，當引發 [**EnumDone**](shellfolderviewoc-enumdone.md) 或 [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) 事件時， **ShellFolderViewOC** 物件會將事件轉送至它自己的處理常式以進行處理。</span><span class="sxs-lookup"><span data-stu-id="0c874-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c874-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0c874-133">Requirements</span></span>



| <span data-ttu-id="0c874-134">需求</span><span class="sxs-lookup"><span data-stu-id="0c874-134">Requirement</span></span> | <span data-ttu-id="0c874-135">值</span><span class="sxs-lookup"><span data-stu-id="0c874-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c874-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0c874-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0c874-137">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c874-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0c874-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0c874-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0c874-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0c874-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0c874-140">標頭</span><span class="sxs-lookup"><span data-stu-id="0c874-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c874-141"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="0c874-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="0c874-142">Idl</span><span class="sxs-lookup"><span data-stu-id="0c874-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c874-143"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c874-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="0c874-144">DLL</span><span class="sxs-lookup"><span data-stu-id="0c874-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c874-145"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="0c874-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c874-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0c874-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c874-147">**ShellFolderView**</span><span class="sxs-lookup"><span data-stu-id="0c874-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 





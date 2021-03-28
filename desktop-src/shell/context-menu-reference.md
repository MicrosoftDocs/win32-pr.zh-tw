---
description: 本主題列出用於快捷方式 (內容) 功能表和快捷方式功能表處理常式的主要程式設計項目。 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。
ms.assetid: efd96a52-6455-40bc-9c21-65f89728e771
title: 快速鍵功能表參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cb1552c8f2f383b08984e9142e464b6831a3c8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191182"
---
# <a name="shortcut-menu-reference"></a><span data-ttu-id="6e34a-104">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="6e34a-104">Shortcut Menu Reference</span></span>

<span data-ttu-id="6e34a-105">本主題列出用於快捷方式 (內容) 功能表和快捷方式功能表處理常式的主要程式設計項目。</span><span class="sxs-lookup"><span data-stu-id="6e34a-105">This topic lists the main programming elements used with shortcut (context) menus, and shortcut menu handlers.</span></span> <span data-ttu-id="6e34a-106">快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。</span><span class="sxs-lookup"><span data-stu-id="6e34a-106">Shortcut menu handlers, which also known as context menu handlers or verb handlers, are a type of file type handler.</span></span>

## <a name="about-shortcut-menu-implemetation"></a><span data-ttu-id="6e34a-107">關於快捷方式功能表實作</span><span class="sxs-lookup"><span data-stu-id="6e34a-107">About Shortcut Menu Implemetation</span></span>

<span data-ttu-id="6e34a-108">強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="6e34a-108">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="6e34a-109">請參閱下列指示：</span><span class="sxs-lookup"><span data-stu-id="6e34a-109">Please review the following instructions:</span></span>

-   <span data-ttu-id="6e34a-110">若要使用靜態動詞方法來執行快捷方式功能表，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)的「使用靜態動詞自訂快捷方式功能表」一節。</span><span class="sxs-lookup"><span data-stu-id="6e34a-110">To use a static verb method to implement a shortcut menu, see the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>
-   <span data-ttu-id="6e34a-111">若要在 Windows 7 及更新版本中取得靜態動詞命令的動態行為，請參閱 [建立快捷方式功能表處理常式](context-menu-handlers.md)中的「取得靜態動詞的動態行為」。</span><span class="sxs-lookup"><span data-stu-id="6e34a-111">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>
-   <span data-ttu-id="6e34a-112">如需靜態動詞命令的執行，以及要避免哪些動態動詞的詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。</span><span class="sxs-lookup"><span data-stu-id="6e34a-112">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>
-   <span data-ttu-id="6e34a-113">如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)中提供的指示進行。</span><span class="sxs-lookup"><span data-stu-id="6e34a-113">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="interfaces"></a><span data-ttu-id="6e34a-114">介面</span><span class="sxs-lookup"><span data-stu-id="6e34a-114">Interfaces</span></span>



| <span data-ttu-id="6e34a-115">主題</span><span class="sxs-lookup"><span data-stu-id="6e34a-115">Topic</span></span>                                        | <span data-ttu-id="6e34a-116">目錄</span><span class="sxs-lookup"><span data-stu-id="6e34a-116">Contents</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e34a-117">**ICoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="6e34a-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)         | <span data-ttu-id="6e34a-118">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="6e34a-118">Exposes methods that either create or merge a shortcut menu associated with a Shell object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6e34a-119">**ICoNtextMenu2**</span><span class="sxs-lookup"><span data-stu-id="6e34a-119">**IContextMenu2**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2)       | <span data-ttu-id="6e34a-120">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式 (內容) 功能表。</span><span class="sxs-lookup"><span data-stu-id="6e34a-120">Exposes methods that either create or merge a shortcut (context) menu associated with a Shell object.</span></span> <span data-ttu-id="6e34a-121">藉由新增方法來擴充 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) ，以允許用戶端物件處理與主控描繪功能表項目相關聯的訊息。</span><span class="sxs-lookup"><span data-stu-id="6e34a-121">Extends [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) by adding a method that allows client objects to handle messages associated with owner-drawn menu items.</span></span><br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="6e34a-122">**ICoNtextMenu3**</span><span class="sxs-lookup"><span data-stu-id="6e34a-122">**IContextMenu3**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3)       | <span data-ttu-id="6e34a-123">公開方法，以建立或合併與 Shell 物件相關聯的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="6e34a-123">Exposes methods that either create or merge a shortcut menu associated with a Shell object.</span></span> <span data-ttu-id="6e34a-124">允許用戶端物件處理與主控描繪功能表項目相關聯的訊息，並接受來自該訊息處理的傳回值來擴充 [**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) 。</span><span class="sxs-lookup"><span data-stu-id="6e34a-124">Allows client objects to handle messages associated with owner-drawn menu items and extends [**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) by accepting a return value from that message handling.</span></span><br/>                                                                                                                                                                                                                         |
| [<span data-ttu-id="6e34a-125">**ICoNtextMenuCB**</span><span class="sxs-lookup"><span data-stu-id="6e34a-125">**IContextMenuCB**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb)     | <span data-ttu-id="6e34a-126">公開啟用內容功能表回呼的方法。</span><span class="sxs-lookup"><span data-stu-id="6e34a-126">Exposes a method that enables the callback of a context menu.</span></span> <span data-ttu-id="6e34a-127">例如，在需要提高許可權的 **menuItem** 中加入盾牌圖示。</span><span class="sxs-lookup"><span data-stu-id="6e34a-127">For example, to add a shield icon to a **menuItem** that requires elevation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="6e34a-128">**ICoNtextMenuSite**</span><span class="sxs-lookup"><span data-stu-id="6e34a-128">**IContextMenuSite**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) | <span data-ttu-id="6e34a-129">由使用 [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview)建立的預設資料夾視圖所執行。</span><span class="sxs-lookup"><span data-stu-id="6e34a-129">Implemented by the default folder view created using [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).</span></span> <span data-ttu-id="6e34a-130">[**ICoNtextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite)的執行支援 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)、 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)和 [**trackpopupmenu 讓**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu)，以及該函式所需的任何訊息轉送。</span><span class="sxs-lookup"><span data-stu-id="6e34a-130">An implementation of [**IContextMenuSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenusite) supports [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand), and [**TrackPopupMenu**](/windows/win32/api/winuser/nf-winuser-trackpopupmenu) and any message forwarding necessary for that function.</span></span> <span data-ttu-id="6e34a-131">**ICoNtextMenuSite** 通常也會更新狀態列。</span><span class="sxs-lookup"><span data-stu-id="6e34a-131">**IContextMenuSite** typically updates the status bar as well.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="6e34a-132">函式</span><span class="sxs-lookup"><span data-stu-id="6e34a-132">Functions</span></span>



| <span data-ttu-id="6e34a-133">主題</span><span class="sxs-lookup"><span data-stu-id="6e34a-133">Topic</span></span>                                                            | <span data-ttu-id="6e34a-134">目錄</span><span class="sxs-lookup"><span data-stu-id="6e34a-134">Contents</span></span>                                                                                                                                |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e34a-135">**CDefFolderMenu \_ Create2**</span><span class="sxs-lookup"><span data-stu-id="6e34a-135">**CDefFolderMenu\_Create2**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)        | <span data-ttu-id="6e34a-136">建立所選檔案資料夾物件群組的內容功能表。</span><span class="sxs-lookup"><span data-stu-id="6e34a-136">Creates a context menu for a selected group of file folder objects.</span></span><br/>                                                          |
| [<span data-ttu-id="6e34a-137">**LPFNDFMCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="6e34a-137">**LPFNDFMCALLBACK**</span></span>](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback)                       | <span data-ttu-id="6e34a-138">定義回呼函式的原型，此函式會從 Shell 的預設內容功能表執行接收訊息。</span><span class="sxs-lookup"><span data-stu-id="6e34a-138">Defines the prototype for the callback function that receives messages from the Shell's default context menu implementation.</span></span><br/> |
| [<span data-ttu-id="6e34a-139">**SHCreateDefaultCoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="6e34a-139">**SHCreateDefaultContextMenu**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu) | <span data-ttu-id="6e34a-140">建立物件，這個物件表示 Shell 的預設內容功能表執行。</span><span class="sxs-lookup"><span data-stu-id="6e34a-140">Creates an object that represents the Shell's default context menu implementation.</span></span><br/>                                           |



 

### <a name="structures"></a><span data-ttu-id="6e34a-141">結構</span><span class="sxs-lookup"><span data-stu-id="6e34a-141">Structures</span></span>



| <span data-ttu-id="6e34a-142">主題</span><span class="sxs-lookup"><span data-stu-id="6e34a-142">Topic</span></span>                                                  | <span data-ttu-id="6e34a-143">目錄</span><span class="sxs-lookup"><span data-stu-id="6e34a-143">Contents</span></span>                                                                                                                                                                                                   |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e34a-144">**CMINVOKECOMMANDINFO**</span><span class="sxs-lookup"><span data-stu-id="6e34a-144">**CMINVOKECOMMANDINFO**</span></span>](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)     | <span data-ttu-id="6e34a-145">包含 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 用來叫用快捷方式功能表命令所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="6e34a-145">Contains information needed by [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) to invoke a shortcut menu command.</span></span><br/>                                                             |
| [<span data-ttu-id="6e34a-146">**CMINVOKECOMMANDINFOEX**</span><span class="sxs-lookup"><span data-stu-id="6e34a-146">**CMINVOKECOMMANDINFOEX**</span></span>](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) | <span data-ttu-id="6e34a-147">包含快捷方式功能表命令的延伸資訊。</span><span class="sxs-lookup"><span data-stu-id="6e34a-147">Contains extended information about a shortcut menu command.</span></span> <span data-ttu-id="6e34a-148">此結構是 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 的延伸版本，可允許使用 Unicode 值。</span><span class="sxs-lookup"><span data-stu-id="6e34a-148">This structure is an extended version of [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) that allows the use of Unicode values.</span></span><br/> |
| [<span data-ttu-id="6e34a-149">**DEFCONTEXTMENU**</span><span class="sxs-lookup"><span data-stu-id="6e34a-149">**DEFCONTEXTMENU**</span></span>](/windows/desktop/api/shlobj_core/ns-shlobj_core-defcontextmenu)               | <span data-ttu-id="6e34a-150">包含 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)所使用的內容功能表資訊。</span><span class="sxs-lookup"><span data-stu-id="6e34a-150">Contains context menu information used by [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span><br/>                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="6e34a-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e34a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e34a-152">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="6e34a-152">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="6e34a-153">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="6e34a-153">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="6e34a-154">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="6e34a-154">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="6e34a-155">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="6e34a-155">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="6e34a-156">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="6e34a-156">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="6e34a-157">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="6e34a-157">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> </dl>

 

 

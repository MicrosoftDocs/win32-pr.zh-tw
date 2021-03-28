---
description: 快速鍵功能表處理常式也稱為內容功能表處理常式或動詞處理常式。 快捷方式功能表處理常式是檔案類型處理常式的類型。
ms.assetid: 7FC65C6F-3798-404c-B359-2BC75D3F54E7
title: 使用動態動詞自訂快捷方式功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b24f035e84f0bde6dccde09f1ed94fefce421b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973464"
---
# <a name="customizing-a-shortcut-menu-using-dynamic-verbs"></a><span data-ttu-id="df800-104">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="df800-104">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>

<span data-ttu-id="df800-105">快速鍵功能表處理常式也稱為內容功能表處理常式或動詞處理常式。</span><span class="sxs-lookup"><span data-stu-id="df800-105">Shortcut menu handlers are also known as context menu handlers or verb handlers.</span></span> <span data-ttu-id="df800-106">快捷方式功能表處理常式是檔案類型處理常式的類型。</span><span class="sxs-lookup"><span data-stu-id="df800-106">A shortcut menu handler is a type of file type handler.</span></span>

<span data-ttu-id="df800-107">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="df800-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="df800-108">關於靜態和動態動詞</span><span class="sxs-lookup"><span data-stu-id="df800-108">About Static and Dynamic Verbs</span></span>](#about-static-and-dynamic-verbs)
-   [<span data-ttu-id="df800-109">快速鍵功能表處理常式如何搭配動態動詞</span><span class="sxs-lookup"><span data-stu-id="df800-109">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>](#how-shortcut-menu-handlers-work-with-dynamic-verbs)
-   [<span data-ttu-id="df800-110">避免因為不合格的動詞名稱而發生衝突</span><span class="sxs-lookup"><span data-stu-id="df800-110">Avoiding Collisions Due to Unqualified Verb Names</span></span>](#avoiding-collisions-due-to-unqualified-verb-names)
-   [<span data-ttu-id="df800-111">使用動態動詞來註冊快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="df800-111">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>](#registering-a-shortcut-menu-handler-with-a-dynamic-verb)
-   [<span data-ttu-id="df800-112">執行 ICoNtextMenu 介面</span><span class="sxs-lookup"><span data-stu-id="df800-112">Implementing the IContextMenu Interface</span></span>](#implementing-the-icontextmenu-interface)
    -   [<span data-ttu-id="df800-113">ICoNtextMenu：： GetCommandString 方法</span><span class="sxs-lookup"><span data-stu-id="df800-113">IContextMenu::GetCommandString Method</span></span>](#icontextmenugetcommandstring-method)
    -   [<span data-ttu-id="df800-114">ICoNtextMenu：： InvokeCommand 方法</span><span class="sxs-lookup"><span data-stu-id="df800-114">IContextMenu::InvokeCommand Method</span></span>](#icontextmenuinvokecommand-method)
    -   [<span data-ttu-id="df800-115">ICoNtextMenu：： QueryCoNtextMenu 方法</span><span class="sxs-lookup"><span data-stu-id="df800-115">IContextMenu::QueryContextMenu Method</span></span>](#icontextmenuquerycontextmenu-method)
-   [<span data-ttu-id="df800-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="df800-116">Related topics</span></span>](#related-topics)

## <a name="about-static-and-dynamic-verbs"></a><span data-ttu-id="df800-117">關於靜態和動態動詞</span><span class="sxs-lookup"><span data-stu-id="df800-117">About Static and Dynamic Verbs</span></span>

<span data-ttu-id="df800-118">強烈建議您使用其中一個靜態動詞方法來執行快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="df800-118">We strongly encourage you to implement a shortcut menu using one of the static verb methods.</span></span> <span data-ttu-id="df800-119">建議您依照「使用靜態動詞來自訂快捷方式功能表」一節中所提供的指示，來 [建立內容功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-119">We recommend that you follow the instructions provided in the "Customizing a Shortcut Menu using Static Verbs" section of [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="df800-120">若要在 Windows 7 及更新版本中取得靜態動詞命令的動態行為，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)中的「取得靜態動詞的動態行為」。</span><span class="sxs-lookup"><span data-stu-id="df800-120">To get dynamic behavior for static verbs in Windows 7 and later, see "Getting Dynamic Behavior for Static Verbs" in [Creating Context Menu Handlers](context-menu-handlers.md).</span></span> <span data-ttu-id="df800-121">如需靜態動詞命令的執行，以及要避免哪些動態動詞的詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-121">For details on static verb implementation, and which dynamic verbs to avoid, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span>

<span data-ttu-id="df800-122">如果您必須註冊檔案類型的動態動詞命令以擴充檔案類型的快捷方式功能表，請依照本主題稍後提供的指示進行。</span><span class="sxs-lookup"><span data-stu-id="df800-122">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided later in this topic.</span></span>

> [!Note]  
> <span data-ttu-id="df800-123">註冊在32位應用程式內容中運作的處理常式時，會有64位 Windows 的特殊考慮：當 Shell 動詞命令在32位應用程式的內容中叫用時，WOW64 子系統會將檔案系統存取重新導向至某些路徑。</span><span class="sxs-lookup"><span data-stu-id="df800-123">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="df800-124">如果您的 .exe 處理常式儲存在其中一個路徑中，就無法在此內容中存取。</span><span class="sxs-lookup"><span data-stu-id="df800-124">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="df800-125">因此，若要解決這個問題，請將 .exe 儲存在未重新導向的路徑中，或儲存啟動實際版本之 .exe 的存根版本。</span><span class="sxs-lookup"><span data-stu-id="df800-125">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

## <a name="how-shortcut-menu-handlers-work-with-dynamic-verbs"></a><span data-ttu-id="df800-126">快速鍵功能表處理常式如何搭配動態動詞</span><span class="sxs-lookup"><span data-stu-id="df800-126">How Shortcut Menu Handlers Work with Dynamic Verbs</span></span>

<span data-ttu-id="df800-127">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)之外，快速鍵功能表處理常式也會匯出下列其他介面，以處理執行主控描繪功能表項目所需的訊息：</span><span class="sxs-lookup"><span data-stu-id="df800-127">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), shortcut menu handlers export the following additional interfaces to handle the messaging needed to implement owner-drawn menu items:</span></span>

-   <span data-ttu-id="df800-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (強制) </span><span class="sxs-lookup"><span data-stu-id="df800-128">[**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) (mandatory)</span></span>
-   <span data-ttu-id="df800-129">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (強制) </span><span class="sxs-lookup"><span data-stu-id="df800-129">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) (mandatory)</span></span>
-   <span data-ttu-id="df800-130">[**ICoNtextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (選用) </span><span class="sxs-lookup"><span data-stu-id="df800-130">[**IContextMenu2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2) (optional)</span></span>
-   <span data-ttu-id="df800-131">[**ICoNtextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (選用) </span><span class="sxs-lookup"><span data-stu-id="df800-131">[**IContextMenu3**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3) (optional)</span></span>

<span data-ttu-id="df800-132">如需主控描繪功能表項目的詳細資訊，請參閱 [使用功能表](../menurc/using-menus.md)中的 *建立 Owner-Drawn 功能表項目* 一節。</span><span class="sxs-lookup"><span data-stu-id="df800-132">For more information on owner-drawn menu items, see the *Creating Owner-Drawn Menu Items* section in [Using Menus](../menurc/using-menus.md).</span></span>

<span data-ttu-id="df800-133">Shell 會使用 [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) 介面來初始化處理常式。</span><span class="sxs-lookup"><span data-stu-id="df800-133">Shell uses the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) interface to initialize the handler.</span></span> <span data-ttu-id="df800-134">當 Shell 呼叫 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)時，它會將物件的名稱和指標傳遞至專案識別碼清單的資料物件， (PIDL 包含該檔案之資料夾的) 。</span><span class="sxs-lookup"><span data-stu-id="df800-134">When the Shell calls [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize), it passes in a data object with the object's name and a pointer to an item identifier list (PIDL) of the folder that contains the file.</span></span> <span data-ttu-id="df800-135">*HkeyProgID* 參數是用來註冊快捷方式功能表控制碼的登錄位置。</span><span class="sxs-lookup"><span data-stu-id="df800-135">The *hkeyProgID* parameter is the registry location under which the shortcut menu handle is registered.</span></span> <span data-ttu-id="df800-136">**IShellExtInit：： Initialize** 方法必須從資料物件中解壓縮檔案名稱，並將名稱和資料夾指標儲存至專案識別碼清單， (PIDL) 以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="df800-136">The **IShellExtInit::Initialize** method must extract the file name from the data object and store the name and the folder's pointer to an item identifier list (PIDL) for later use.</span></span> <span data-ttu-id="df800-137">如需處理常式初始化的詳細資訊，請參閱 [執行 IShellExtInit](handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-137">For more information on handler initialization, see [Implementing IShellExtInit](handlers.md).</span></span>

<span data-ttu-id="df800-138">在快捷方式功能表中顯示動詞命令時，會先探索到動詞，然後向使用者顯示，最後叫用。</span><span class="sxs-lookup"><span data-stu-id="df800-138">When verbs are presented in a shortcut menu, they are first discovered, then presented to the user, and finally invoked.</span></span> <span data-ttu-id="df800-139">下列清單會更詳細地說明這三個步驟：</span><span class="sxs-lookup"><span data-stu-id="df800-139">The following list describes these three steps in more detail:</span></span>

1.  <span data-ttu-id="df800-140">Shell 會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)，它會傳回一組可以根據專案或系統狀態的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="df800-140">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu), which returns a set of verbs that can be based on the state of the items or the system.</span></span>
2.  <span data-ttu-id="df800-141">系統會傳入 **HMENU** 控制碼，該控制碼可讓方法用來將專案加入至快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="df800-141">The system passes in an **HMENU** handle that the method can use to add items to the shortcut menu.</span></span>
3.  <span data-ttu-id="df800-142">如果使用者按一下其中一個處理常式的專案，則 Shell 會呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)。</span><span class="sxs-lookup"><span data-stu-id="df800-142">If the user clicks one of the handler's items, the Shell calls [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span> <span data-ttu-id="df800-143">然後，處理常式可以執行適當的命令。</span><span class="sxs-lookup"><span data-stu-id="df800-143">The handler can then execute the appropriate command.</span></span>

## <a name="avoiding-collisions-due-to-unqualified-verb-names"></a><span data-ttu-id="df800-144">避免因為不合格的動詞名稱而發生衝突</span><span class="sxs-lookup"><span data-stu-id="df800-144">Avoiding Collisions Due to Unqualified Verb Names</span></span>

<span data-ttu-id="df800-145">由於動詞是針對每個類型註冊，因此相同的動詞名稱可用於不同專案的動詞。</span><span class="sxs-lookup"><span data-stu-id="df800-145">Because verbs are registered per type, the same verb name can be used for verbs on different items.</span></span> <span data-ttu-id="df800-146">這樣做可讓應用程式參考與專案類型無關的一般動詞。</span><span class="sxs-lookup"><span data-stu-id="df800-146">Doing so enables applications to refer to common verbs independent of the item type.</span></span> <span data-ttu-id="df800-147">雖然這項功能很有用，但使用不合格的名稱可能會導致選擇相同動詞名稱的多個獨立軟體廠商 (Isv) 發生衝突。</span><span class="sxs-lookup"><span data-stu-id="df800-147">While this functionality is useful, the use of unqualified names can result in collisions with multiple independent software vendors (ISVs) that choose the same verb name.</span></span> <span data-ttu-id="df800-148">若要避免這種情況，請一律在動詞命令前面加上 ISV 名稱，如下所示：</span><span class="sxs-lookup"><span data-stu-id="df800-148">To avoid this, always prefix verbs with the ISV name as follows:</span></span>

`ISV_Name.verb`

<span data-ttu-id="df800-149">一律使用應用程式特定的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="df800-149">Always use an application specific ProgID.</span></span> <span data-ttu-id="df800-150">採用將副檔名對應至 ISV 提供之 ProgID 的慣例，可避免可能發生的衝突。</span><span class="sxs-lookup"><span data-stu-id="df800-150">Adopting the convention of mapping the file name extension to an ISV provided ProgID avoids potential collisions.</span></span> <span data-ttu-id="df800-151">不過，由於某些專案類型不會使用此對應，因此需要廠商唯一的名稱。</span><span class="sxs-lookup"><span data-stu-id="df800-151">However, because some item types do not use this mapping, there is a need for vendor-unique names.</span></span> <span data-ttu-id="df800-152">將動詞新增至可能已註冊該動詞的現有 ProgID 時，您必須先移除舊動詞命令的登錄機碼，再新增您自己的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="df800-152">When adding a verb to an existing ProgID that might already have that verb registered, you must first remove the registry key for the old verb before adding your own verb.</span></span> <span data-ttu-id="df800-153">您必須這樣做，才能避免合併來自兩個動詞的動詞資訊。</span><span class="sxs-lookup"><span data-stu-id="df800-153">You must do so to avoid merging the verb information from the two verbs.</span></span> <span data-ttu-id="df800-154">若未這麼做，會導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="df800-154">Failure to do so results in unpredictable behavior.</span></span>

## <a name="registering-a-shortcut-menu-handler-with-a-dynamic-verb"></a><span data-ttu-id="df800-155">使用動態動詞來註冊快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="df800-155">Registering a Shortcut Menu Handler with a Dynamic Verb</span></span>

<span data-ttu-id="df800-156">快速鍵功能表處理常式會與檔案類型或資料夾相關聯。</span><span class="sxs-lookup"><span data-stu-id="df800-156">Shortcut menu handlers are associated with either a file type or a folder.</span></span> <span data-ttu-id="df800-157">針對檔案類型，會在下列子機碼下註冊處理常式。</span><span class="sxs-lookup"><span data-stu-id="df800-157">For file types, the handler is registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Program ID
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="df800-158">若要建立快捷方式功能表處理常式與檔案類型或資料夾的關聯，請先在 **CoNtextMenuHandlers** 子機碼底下建立子機碼。</span><span class="sxs-lookup"><span data-stu-id="df800-158">To associate a shortcut menu handler with either a file type or a folder, first create a subkey under the **ContextMenuHandlers** subkey.</span></span> <span data-ttu-id="df800-159">命名處理常式的子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串形式 (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="df800-159">Name the subkey for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="df800-160">然後，若要將快捷方式功能表處理常式與不同類型的資料夾產生關聯，請使用與檔案類型相同的方式來註冊處理常式，但在 *FolderType* 子機碼底下，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="df800-160">Then to associate a shortcut menu handler with different kinds of folders, register the handler the same way you would for a file type, but under the *FolderType* subkey as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   FolderType
      shellex
         ContextMenuHandlers
```

<span data-ttu-id="df800-161">如需您可以註冊處理常式之資料夾類型的詳細資訊，請參閱 [註冊 Shell 擴充處理常式](handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-161">For more information about about which folder types you can register handlers for, see [Registering Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="df800-162">如果檔案類型有相關聯的快捷方式功能表，則按兩下物件通常會啟動預設的命令，且不會呼叫處理常式的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 方法。</span><span class="sxs-lookup"><span data-stu-id="df800-162">If a file type has a shortcut menu associated with it, then double-clicking an object normally launches the default command, and the handler's [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) method is not called.</span></span> <span data-ttu-id="df800-163">若要指定按兩下物件時應呼叫處理常式的 **ICoNtextMenu：： QueryCoNtextMenu** 方法，請在處理常式的 **CLSID** 子機碼底下建立子機碼，如下所示。</span><span class="sxs-lookup"><span data-stu-id="df800-163">To specify that the handler's **IContextMenu::QueryContextMenu** method should be called when an object is double-clicked, create a subkey under the handler's **CLSID** subkey as shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {00000000-1111-2222-3333-444444444444}
         shellex
            MayChangeDefaultMenu
```

<span data-ttu-id="df800-164">按兩下與處理常式相關聯的物件時，會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ，並在 *uFlags* 參數中設定 **CMF \_ DEFAULTONLY** 旗標。</span><span class="sxs-lookup"><span data-stu-id="df800-164">When an object associated with the handler is double-clicked, [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) is called with the **CMF\_DEFAULTONLY** flag set in the *uFlags* parameter.</span></span>

<span data-ttu-id="df800-165">只有當快捷方式功能表處理常式可能需要變更快捷方式功能表的預設動詞時，才應該設定 **MayChangeDefaultMenu** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="df800-165">Shortcut menu handlers should set the **MayChangeDefaultMenu** subkey only if they might need to change the shortcut menu's default verb.</span></span> <span data-ttu-id="df800-166">設定這個子機碼會強制系統在相關聯的專案按兩下時載入處理常式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="df800-166">Setting this subkey forces the system to load the handler's DLL when an associated item is double-clicked.</span></span> <span data-ttu-id="df800-167">如果您的處理常式未變更預設動詞命令，您就不應該設定此子機碼，因為這樣做會導致系統不必要地載入您的 DLL。</span><span class="sxs-lookup"><span data-stu-id="df800-167">If your handler does not change the default verb, you should not set this subkey because doing so causes the system to load your DLL unnecessarily.</span></span>

<span data-ttu-id="df800-168">下列範例說明啟用 myp 檔案類型之快捷方式功能表處理常式的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="df800-168">The following example illustrates registry entries that enable a shortcut menu handler for an .myp file type.</span></span> <span data-ttu-id="df800-169">處理常式的 **CLSID** 子機碼包含 **MayChangeDefaultMenu** 子機碼，以保證當使用者按兩下相關物件時，會呼叫此處理程式。</span><span class="sxs-lookup"><span data-stu-id="df800-169">The handler's **CLSID** subkey includes a **MayChangeDefaultMenu** subkey to guarantee that the handler is called when the user double-clicks a related object.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
         shellex
            MayChangeDefaultMenu
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         ContextMenuHandler
            MyCommand = {00000000-1111-2222-3333-444444444444}
```

## <a name="implementing-the-icontextmenu-interface"></a><span data-ttu-id="df800-170">執行 ICoNtextMenu 介面</span><span class="sxs-lookup"><span data-stu-id="df800-170">Implementing the IContextMenu Interface</span></span>

<span data-ttu-id="df800-171">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 是最強大的功能，但也是最複雜的方法來執行。</span><span class="sxs-lookup"><span data-stu-id="df800-171">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="df800-172">強烈建議您使用其中一個靜態動詞方法來執行動詞。</span><span class="sxs-lookup"><span data-stu-id="df800-172">We strongly recommend that you implement a verb by using one of the static verb methods.</span></span> <span data-ttu-id="df800-173">如需詳細資訊，請參閱 [為您的快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-173">For more information, see [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md).</span></span> <span data-ttu-id="df800-174">[**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 有三種方法： **GetCommandString**、 **InvokeCommand** 和 **QueryCoNtextMenu**，在這裡會詳細討論。</span><span class="sxs-lookup"><span data-stu-id="df800-174">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) has three methods, **GetCommandString**, **InvokeCommand**, and **QueryContextMenu**, which are discussed here in detail.</span></span>

### <a name="icontextmenugetcommandstring-method"></a><span data-ttu-id="df800-175">ICoNtextMenu：： GetCommandString 方法</span><span class="sxs-lookup"><span data-stu-id="df800-175">IContextMenu::GetCommandString Method</span></span>

<span data-ttu-id="df800-176">處理常式的 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 方法是用來傳回動詞的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="df800-176">The handler's [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) method is used to return the canonical name for a verb.</span></span> <span data-ttu-id="df800-177">這個方法是一個選擇項目。</span><span class="sxs-lookup"><span data-stu-id="df800-177">This method is optional.</span></span> <span data-ttu-id="df800-178">在 Windows XP 和舊版的 Windows 中，當 Windows 檔案總管有狀態列時，就會使用這個方法來取得顯示在功能表項目狀態列中的解說文字。</span><span class="sxs-lookup"><span data-stu-id="df800-178">In Windows XP and earlier versions of Windows, when Windows Explorer has a Status bar, this method is used to retrieve the help text that is displayed in the Status bar for a menu item.</span></span>

<span data-ttu-id="df800-179">*IdCmd* 參數會保存呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)時所定義命令的識別碼位移。</span><span class="sxs-lookup"><span data-stu-id="df800-179">The *idCmd* parameter holds the identifier offset of the command that was defined when [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) was called.</span></span> <span data-ttu-id="df800-180">如果要求了說明字串，則 *uFlags* 會設定為 **gc \_ HELPTEXTW**。</span><span class="sxs-lookup"><span data-stu-id="df800-180">If a help string is requested, *uFlags* will be set to **GCS\_HELPTEXTW**.</span></span> <span data-ttu-id="df800-181">將說明字串複製到 *pszName* 緩衝區，並將其轉換成 **PWSTR**。</span><span class="sxs-lookup"><span data-stu-id="df800-181">Copy the help string to the *pszName* buffer, casting it to a **PWSTR**.</span></span> <span data-ttu-id="df800-182">將 *uFlags* 設定為 **gc \_ VERBW**，即可要求動詞字串。</span><span class="sxs-lookup"><span data-stu-id="df800-182">The verb string is requested by setting *uFlags* to **GCS\_VERBW**.</span></span> <span data-ttu-id="df800-183">將適當的字串複製到 *pszName*，就像使用說明字串一樣。</span><span class="sxs-lookup"><span data-stu-id="df800-183">Copy the appropriate string to *pszName*, just as with the help string.</span></span> <span data-ttu-id="df800-184">快速鍵功能表處理常式不會使用 **gc \_ VALIDATEA** 和 **gc \_ VALIDATEW** 旗標。</span><span class="sxs-lookup"><span data-stu-id="df800-184">The **GCS\_VALIDATEA** and **GCS\_VALIDATEW** flags are not used by shortcut menu handlers.</span></span>

<span data-ttu-id="df800-185">下列範例示範 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring)的簡單執行，其對應至本主題的 [ICoNtextMenu：： QueryCoNtextMenu 方法](#icontextmenuquerycontextmenu-method)一節中提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)範例。</span><span class="sxs-lookup"><span data-stu-id="df800-185">The following example shows a simple implementation of [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) example given in the [IContextMenu::QueryContextMenu Method](#icontextmenuquerycontextmenu-method) section of this topic.</span></span> <span data-ttu-id="df800-186">因為處理常式只會新增一個功能表項目，所以只能傳回一組字串。</span><span class="sxs-lookup"><span data-stu-id="df800-186">Because the handler adds only one menu item, there is only one set of strings that can be returned.</span></span> <span data-ttu-id="df800-187">方法會測試 *idCmd* 是否有效，如果是，則會傳回要求的字串。</span><span class="sxs-lookup"><span data-stu-id="df800-187">The method tests whether *idCmd* is valid and, if it is, returns the requested string.</span></span>

<span data-ttu-id="df800-188">[**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya)函式可用來將要求的字串複製到 *pszName* ，以確保複製的字串不會超過 *cchName* 所指定的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="df800-188">The [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya) function is used to copy the requested string to *pszName* to ensure that the copied string does not exceed the size of the buffer specified by *cchName*.</span></span> <span data-ttu-id="df800-189">此範例只會支援 *uFlags* 的 Unicode 值，因為 Windows 2000 之後的 Windows 檔案總管中只會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="df800-189">This example only implements support for the Unicode values of *uFlags*, because only those have been used in Windows Explorer since Windows 2000.</span></span>


```C++
IFACEMETHODIMP CMenuExtension::GetCommandString(UINT idCommand, 
                                                UINT uFlags, 
                                                UINT *pReserved, 
                                                PSTR pszName, 
                                                UINT cchName)
{
    HRESULT hr = E_INVALIDARG;

    if (idCommand == IDM_DISPLAY)
    {
        switch (uFlags)
        {
            case GCS_HELPTEXTW:
                // Only useful for pre-Vista versions of Windows that 
                // have a Status bar.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"Display File Name");
                break; 

            case GCS_VERBW:
                // GCS_VERBW is an optional feature that enables a caller
                // to discover the canonical name for the verb passed in
                // through idCommand.
                hr = StringCchCopyW(reinterpret_cast<PWSTR>(pszName), 
                                    cchName, 
                                    L"DisplayFileName");
                break; 
        }
    }
    return hr;
}
```



### <a name="icontextmenuinvokecommand-method"></a><span data-ttu-id="df800-190">ICoNtextMenu：： InvokeCommand 方法</span><span class="sxs-lookup"><span data-stu-id="df800-190">IContextMenu::InvokeCommand Method</span></span>

<span data-ttu-id="df800-191">當使用者按一下功能表項目來指示處理常式執行相關聯的命令時，會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="df800-191">This method is called when a user clicks a menu item to tell the handler to run the associated command.</span></span> <span data-ttu-id="df800-192">*Pici* 參數指向包含所需資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="df800-192">The *pici* parameter points to a structure that contains the information required.</span></span>

<span data-ttu-id="df800-193">雖然 *pici* 是在 shlobj.h 中宣告為 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) 結構，但實際上它通常會指向 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構。</span><span class="sxs-lookup"><span data-stu-id="df800-193">Although *pici* is declared in Shlobj.h as a [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo) structure, in practice it often points to a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure.</span></span> <span data-ttu-id="df800-194">此結構是 **CMINVOKECOMMANDINFO** 的延伸版本，而且有數個額外的成員可以傳遞 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="df800-194">This structure is an extended version of **CMINVOKECOMMANDINFO** and has several additional members that make it possible to pass Unicode strings.</span></span>

<span data-ttu-id="df800-195">檢查 *pici* 的 **cbSize** 成員，以判斷傳入的結構。</span><span class="sxs-lookup"><span data-stu-id="df800-195">Check the **cbSize** member of *pici* to determine which structure was passed in.</span></span> <span data-ttu-id="df800-196">如果它是 [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) 結構，而且 **fMask** 成員已設定 **CMIC \_ MASK \_ UNICODE** 旗標，請將 *pici* 轉換成 **CMINVOKECOMMANDINFOEX**。</span><span class="sxs-lookup"><span data-stu-id="df800-196">If it is a [**CMINVOKECOMMANDINFOEX**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfoex) structure and the **fMask** member has the **CMIC\_MASK\_UNICODE** flag set, cast *pici* to **CMINVOKECOMMANDINFOEX**.</span></span> <span data-ttu-id="df800-197">這可讓您的應用程式使用結構最後五個成員中包含的 Unicode 資訊。</span><span class="sxs-lookup"><span data-stu-id="df800-197">This enables your application to use the Unicode information contained in the last five members of the structure.</span></span>

<span data-ttu-id="df800-198">結構的 **lpVerb** 或 **lpVerbW** 成員是用來識別要執行的命令。</span><span class="sxs-lookup"><span data-stu-id="df800-198">The structure's **lpVerb** or **lpVerbW** member is used to identify the command to be executed.</span></span> <span data-ttu-id="df800-199">您可以透過下列兩種方式之一來識別命令：</span><span class="sxs-lookup"><span data-stu-id="df800-199">Commands are identified in one of the following two ways:</span></span>

-   <span data-ttu-id="df800-200">依命令的動詞字串</span><span class="sxs-lookup"><span data-stu-id="df800-200">By the command's verb string</span></span>
-   <span data-ttu-id="df800-201">依命令的識別碼位移</span><span class="sxs-lookup"><span data-stu-id="df800-201">By the command's identifier offset</span></span>

<span data-ttu-id="df800-202">若要區分這兩種情況，請檢查 **lpVerb** 的高序位單字是否有 Unicode 案例或 **lpVerbW** 。</span><span class="sxs-lookup"><span data-stu-id="df800-202">To distinguish between these two cases, check the high-order word of **lpVerb** for the ANSI case or **lpVerbW** for the Unicode case.</span></span> <span data-ttu-id="df800-203">如果高序位單字為非零值，則 **lpVerb** 或 **lpVerbW** 會保存動詞字串。</span><span class="sxs-lookup"><span data-stu-id="df800-203">If the high-order word is nonzero, **lpVerb** or **lpVerbW** holds a verb string.</span></span> <span data-ttu-id="df800-204">如果高序位字是零，命令位移就會是 **lpVerb** 的低序位字組。</span><span class="sxs-lookup"><span data-stu-id="df800-204">If the high-order word is zero, the command offset is in the low-order word of **lpVerb**.</span></span>

<span data-ttu-id="df800-205">下列範例示範 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 的簡單執行，其對應于在此區段之前和之後提供的 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 和 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 範例。</span><span class="sxs-lookup"><span data-stu-id="df800-205">The following example shows a simple implementation of [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) that corresponds to the [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) and [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) examples given before and after this section.</span></span> <span data-ttu-id="df800-206">方法會先決定要傳入的結構。</span><span class="sxs-lookup"><span data-stu-id="df800-206">The method first determines which structure is being passed in.</span></span> <span data-ttu-id="df800-207">接著，它會判斷命令是否以其位移或其動詞來識別。</span><span class="sxs-lookup"><span data-stu-id="df800-207">It then determines whether the command is identified by its offset or its verb.</span></span> <span data-ttu-id="df800-208">如果 **lpVerb** 或 **lpVerbW** 保存有效的動詞或位移，則方法會顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="df800-208">If **lpVerb** or **lpVerbW** holds a valid verb or offset, the method displays a message box.</span></span>


```C++
STDMETHODIMP CShellExtension::InvokeCommand(LPCMINVOKECOMMANDINFO lpcmi)
{
    BOOL fEx = FALSE;
    BOOL fUnicode = FALSE;

    if(lpcmi->cbSize == sizeof(CMINVOKECOMMANDINFOEX))
    {
        fEx = TRUE;
        if((lpcmi->fMask & CMIC_MASK_UNICODE))
        {
            fUnicode = TRUE;
        }
    }

    if( !fUnicode && HIWORD(lpcmi->lpVerb))
    {
        if(StrCmpIA(lpcmi->lpVerb, m_pszVerb))
        {
            return E_FAIL;
        }
    }

    else if( fUnicode && HIWORD(((CMINVOKECOMMANDINFOEX *) lpcmi)->lpVerbW))
    {
        if(StrCmpIW(((CMINVOKECOMMANDINFOEX *)lpcmi)->lpVerbW, m_pwszVerb))
        {
            return E_FAIL;
        }
    }

    else if(LOWORD(lpcmi->lpVerb) != IDM_DISPLAY)
    {
        return E_FAIL;
    }

    else
    {
        MessageBox(lpcmi->hwnd,
                   "The File Name",
                   "File Name",
                   MB_OK|MB_ICONINFORMATION);
    }

    return S_OK;
}
```



### <a name="icontextmenuquerycontextmenu-method"></a><span data-ttu-id="df800-209">ICoNtextMenu：： QueryCoNtextMenu 方法</span><span class="sxs-lookup"><span data-stu-id="df800-209">IContextMenu::QueryContextMenu Method</span></span>

<span data-ttu-id="df800-210">Shell 會呼叫 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) ，以啟用快捷方式功能表處理常式，將其功能表項目加入功能表中。</span><span class="sxs-lookup"><span data-stu-id="df800-210">The Shell calls [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) to enable the shortcut menu handler to add its menu items to the menu.</span></span> <span data-ttu-id="df800-211">它會傳入 *HMENU* 參數中的 **HMENU** 控制碼。</span><span class="sxs-lookup"><span data-stu-id="df800-211">It passes in the **HMENU** handle in the *hmenu* parameter.</span></span> <span data-ttu-id="df800-212">*IndexMenu* 參數會設定為要用於要加入之第一個功能表項目的索引。</span><span class="sxs-lookup"><span data-stu-id="df800-212">The *indexMenu* parameter is set to the index to be used for the first menu item that is to be added.</span></span>

<span data-ttu-id="df800-213">處理常式所加入的任何功能表項目都必須有介於 *idCmdFirst* 和 *idCmdLast* 參數值之間的識別碼。</span><span class="sxs-lookup"><span data-stu-id="df800-213">Any menu items that are added by the handler must have identifiers that fall between the values in the *idCmdFirst* and *idCmdLast* parameters.</span></span> <span data-ttu-id="df800-214">一般來說，第一個命令識別碼會設定為 *idCmdFirst*，每個額外的命令 (1) 遞增一次。</span><span class="sxs-lookup"><span data-stu-id="df800-214">Typically, the first command identifier is set to *idCmdFirst*, which is incremented by one (1) for each additional command.</span></span> <span data-ttu-id="df800-215">這種做法可協助您避免超出 *idCmdLast* ，並在 Shell 呼叫多個處理常式時，將可用識別碼的數目最大化。</span><span class="sxs-lookup"><span data-stu-id="df800-215">This practice helps you avoid exceeding *idCmdLast* and maximizes the number of available identifiers in case the Shell calls more than one handler.</span></span>

<span data-ttu-id="df800-216">專案識別碼的 *命令位移* 是 *idCmdFirst* 中識別碼和值之間的差異。</span><span class="sxs-lookup"><span data-stu-id="df800-216">An item identifier's *command offset* is the difference between the identifier and the value in *idCmdFirst*.</span></span> <span data-ttu-id="df800-217">將您的處理常式所加入之每個專案的位移儲存至快捷方式功能表，因為如果其後呼叫 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)，Shell 可能會使用它來識別該專案。</span><span class="sxs-lookup"><span data-stu-id="df800-217">Store the offset of each item that your handler adds to the shortcut menu because the Shell might use it to identify the item if it subsequently calls [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) or [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand).</span></span>

<span data-ttu-id="df800-218">您也應該將 [動詞](launch.md) 指派給您新增的每個命令。</span><span class="sxs-lookup"><span data-stu-id="df800-218">You should also assign a [verb](launch.md) to each command you add.</span></span> <span data-ttu-id="df800-219">動詞是可在呼叫 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 時，用來取代位移以識別命令的字串。</span><span class="sxs-lookup"><span data-stu-id="df800-219">A verb is a string that can be used instead of the offset to identify the command when [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) is called.</span></span> <span data-ttu-id="df800-220">函式（例如 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) ）也會用來執行快捷方式功能表命令。</span><span class="sxs-lookup"><span data-stu-id="df800-220">It is also used by functions such as [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to execute shortcut menu commands.</span></span>

<span data-ttu-id="df800-221">有三個旗標可以透過與快捷方式功能表處理常式相關的 *uFlags* 參數傳入。</span><span class="sxs-lookup"><span data-stu-id="df800-221">There are three flags that can be passed in through the *uFlags* parameter that are relevant to shortcut menu handlers.</span></span> <span data-ttu-id="df800-222">如下表中所述。</span><span class="sxs-lookup"><span data-stu-id="df800-222">They are described in the following table.</span></span>



| <span data-ttu-id="df800-223">旗標</span><span class="sxs-lookup"><span data-stu-id="df800-223">Flag</span></span>             | <span data-ttu-id="df800-224">描述</span><span class="sxs-lookup"><span data-stu-id="df800-224">Description</span></span>                                                                                                                                                                                                              |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df800-225">CMF \_ DEFAULTONLY</span><span class="sxs-lookup"><span data-stu-id="df800-225">CMF\_DEFAULTONLY</span></span> | <span data-ttu-id="df800-226">使用者選取了預設的命令，通常是按兩下物件。</span><span class="sxs-lookup"><span data-stu-id="df800-226">The user has selected the default command, usually by double-clicking the object.</span></span> <span data-ttu-id="df800-227">[**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 應該將控制權交還給 Shell，而不需修改功能表。</span><span class="sxs-lookup"><span data-stu-id="df800-227">[**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) should return control to the Shell without modifying the menu.</span></span> |
| <span data-ttu-id="df800-228">CMF \_ NODEFAULT</span><span class="sxs-lookup"><span data-stu-id="df800-228">CMF\_NODEFAULT</span></span>   | <span data-ttu-id="df800-229">功能表中的專案都不應該是預設專案。</span><span class="sxs-lookup"><span data-stu-id="df800-229">No item in the menu should be the default item.</span></span> <span data-ttu-id="df800-230">方法應該將其命令新增至功能表。</span><span class="sxs-lookup"><span data-stu-id="df800-230">The method should add its commands to the menu.</span></span>                                                                                                                          |
| <span data-ttu-id="df800-231">CMF \_ 正常</span><span class="sxs-lookup"><span data-stu-id="df800-231">CMF\_NORMAL</span></span>      | <span data-ttu-id="df800-232">快捷方式功能表將會正常顯示。</span><span class="sxs-lookup"><span data-stu-id="df800-232">The shortcut menu will be displayed normally.</span></span> <span data-ttu-id="df800-233">方法應該將其命令新增至功能表。</span><span class="sxs-lookup"><span data-stu-id="df800-233">The method should add its commands to the menu.</span></span>                                                                                                                            |



 

<span data-ttu-id="df800-234">您可以使用 [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) 或 [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) ，將功能表項目新增至清單。</span><span class="sxs-lookup"><span data-stu-id="df800-234">Use either [**InsertMenu**](/windows/win32/api/winuser/nf-winuser-insertmenua) or [**InsertMenuItem**](/windows/win32/api/winuser/nf-winuser-insertmenuitema) to add menu items to the list.</span></span> <span data-ttu-id="df800-235">然後傳回嚴重性值設定為「**嚴重性 \_ 成功**」的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="df800-235">Then return an **HRESULT** value with the severity set to **SEVERITY\_SUCCESS**.</span></span> <span data-ttu-id="df800-236">將 [程式碼] 值設定為已指派最大命令識別碼的位移，再加上一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="df800-236">Set the code value to the offset of the largest command identifier that was assigned, plus one (1).</span></span> <span data-ttu-id="df800-237">例如，假設 *idCmdFirst* 設為5，而您將三個專案新增至功能表，並將命令識別碼設定為5、7和8。</span><span class="sxs-lookup"><span data-stu-id="df800-237">For example, assume that *idCmdFirst* is set to 5 and you add three items to the menu with command identifiers of 5, 7, and 8.</span></span> <span data-ttu-id="df800-238">傳回值應為 `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)` 。</span><span class="sxs-lookup"><span data-stu-id="df800-238">The return value should be `MAKE_HRESULT(SEVERITY_SUCCESS, 0, 8 - 5 + 1)`.</span></span>

<span data-ttu-id="df800-239">下列範例顯示的是 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 的簡單實作為插入單一命令。</span><span class="sxs-lookup"><span data-stu-id="df800-239">The following example shows a simple implementation of [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) that inserts a single command.</span></span> <span data-ttu-id="df800-240">此命令的識別碼位移是 IDM \_ 顯示，其設定為零。</span><span class="sxs-lookup"><span data-stu-id="df800-240">The identifier offset for the command is IDM\_DISPLAY, which is set to zero.</span></span> <span data-ttu-id="df800-241">**M \_ pszVerb** 和 **m \_ pwszVerb** 變數是私用變數，用來以 ANSI 和 Unicode 格式儲存相關聯的語言獨立動詞字串。</span><span class="sxs-lookup"><span data-stu-id="df800-241">The **m\_pszVerb** and **m\_pwszVerb** variables are private variables used to store the associated language-independent verb string in both ANSI and Unicode formats.</span></span>


```C++
#define IDM_DISPLAY 0

STDMETHODIMP CMenuExtension::QueryContextMenu(HMENU hMenu,
                                              UINT indexMenu,
                                              UINT idCmdFirst,
                                              UINT idCmdLast,
                                              UINT uFlags)
{
    HRESULT hr;
    
    if(!(CMF_DEFAULTONLY & uFlags))
    {
        InsertMenu(hMenu, 
                   indexMenu, 
                   MF_STRING | MF_BYPOSITION, 
                   idCmdFirst + IDM_DISPLAY, 
                   "&Display File Name");

    
        
        hr = StringCbCopyA(m_pszVerb, sizeof(m_pszVerb), "display");
        hr = StringCbCopyW(m_pwszVerb, sizeof(m_pwszVerb), L"display");

        return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(IDM_DISPLAY + 1));
    }

    return MAKE_HRESULT(SEVERITY_SUCCESS, 0, USHORT(0));
}
```



<span data-ttu-id="df800-242">如需其他動詞的執行工作，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="df800-242">For other verb implementation tasks, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="df800-243">相關主題</span><span class="sxs-lookup"><span data-stu-id="df800-243">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df800-244">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="df800-244">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="df800-245">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="df800-245">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="df800-246">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="df800-246">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="df800-247">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="df800-247">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="df800-248">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="df800-248">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="df800-249">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="df800-249">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 

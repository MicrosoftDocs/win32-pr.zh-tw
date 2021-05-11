---
description: 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。 就像所有這類處理常式一樣，它們都是同進程元件物件模型， (COM) 物件實作為 Dll。
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: 建立快捷方式功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e102833453566f42d058ff82061f34ebc65691
ms.sourcegitcommit: 9655f82be96b11258276fdefff14423c30552fbb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/11/2021
ms.locfileid: "109740569"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="b2a1a-104">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="b2a1a-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="b2a1a-105">快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="b2a1a-106">這些處理常式的 impelmented 方式可能會讓它們在自己的進程或在瀏覽器中載入，或其他協力廠商進程中載入。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-106">These handlers may be impelmented in a way that causes them to load in their own process or in the explorer, or other 3rd party processes.</span></span> <span data-ttu-id="b2a1a-107">建立同進程處理常式時請小心，因為它們可能會對載入這些處理常式的進程造成損害。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-107">Take care when creating in-process handlers as they can cause harm to the process that loads them.</span></span>

> [!Note]  
> <span data-ttu-id="b2a1a-108">註冊在32位應用程式內容中運作的處理常式時，會有64位版本之 Windows 的特殊考慮：當在不同位的應用程式內容中叫用時，WOW64 子系統會將檔案系統存取重新導向至某些路徑。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-108">There are special considerations for 64-bit based versions of Windows when registering handlers that work in the context of 32-bit applications: when invoked in the context of an application of different bitness, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="b2a1a-109">如果您的 .exe 處理常式儲存在其中一個路徑中，就無法在此內容中存取。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-109">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="b2a1a-110">因此，若要解決這個問題，請將 .exe 儲存在未重新導向的路徑中，或儲存啟動實際版本之 .exe 的存根版本。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-110">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

<span data-ttu-id="b2a1a-111">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-111">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b2a1a-112">標準動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-112">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="b2a1a-113">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-113">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="b2a1a-114">僅限程式設計存取動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-114">Programmatic Access Only Verbs</span></span>](#programmaticaccessonly-verbs)
-   [<span data-ttu-id="b2a1a-115">使用靜態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-115">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="b2a1a-116">使用 IDropTarget 介面啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="b2a1a-116">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="b2a1a-117">指定靜態動詞命令的位置和順序</span><span class="sxs-lookup"><span data-stu-id="b2a1a-117">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="b2a1a-118">將動詞放置於功能表頂端或底部</span><span class="sxs-lookup"><span data-stu-id="b2a1a-118">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="b2a1a-119">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-119">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="b2a1a-120">使用 Advanced Query 語法取得靜態動詞命令的動態行為</span><span class="sxs-lookup"><span data-stu-id="b2a1a-120">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="b2a1a-121">已淘汰：將動詞與動態資料交換命令建立關聯</span><span class="sxs-lookup"><span data-stu-id="b2a1a-121">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="b2a1a-122">完成動詞執行工作</span><span class="sxs-lookup"><span data-stu-id="b2a1a-122">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="b2a1a-123">自訂預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-123">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="b2a1a-124">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-124">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="b2a1a-125">隱藏動詞和控制可見度</span><span class="sxs-lookup"><span data-stu-id="b2a1a-125">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="b2a1a-126">採用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="b2a1a-126">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="b2a1a-127">使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="b2a1a-127">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="b2a1a-128">透過 Desktop.ini為資料夾執行自訂動詞 </span><span class="sxs-lookup"><span data-stu-id="b2a1a-128">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="b2a1a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2a1a-129">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="b2a1a-130">標準動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-130">Canonical Verbs</span></span>

<span data-ttu-id="b2a1a-131">應用程式通常負責為其定義的動詞提供當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-131">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="b2a1a-132">不過，為了提供某種程度的語言獨立性，系統會定義一組標準的常用動詞，稱為標準動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-132">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="b2a1a-133">標準動詞永遠不會向使用者顯示，而且可以搭配任何 UI 語言使用。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-133">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="b2a1a-134">系統會使用標準名稱自動產生適當當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-134">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="b2a1a-135">例如，開啟動詞的顯示字串會設定為在英文系統上 **開啟** ，以及德文系統上的德文對等專案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-135">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>


| <span data-ttu-id="b2a1a-136">標準動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-136">Canonical verb</span></span> | <span data-ttu-id="b2a1a-137">描述</span><span class="sxs-lookup"><span data-stu-id="b2a1a-137">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="b2a1a-138">開啟</span><span class="sxs-lookup"><span data-stu-id="b2a1a-138">Open</span></span>           | <span data-ttu-id="b2a1a-139">開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-139">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="b2a1a-140">Opennew</span><span class="sxs-lookup"><span data-stu-id="b2a1a-140">Opennew</span></span>        | <span data-ttu-id="b2a1a-141">在新視窗中開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-141">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="b2a1a-142">列印</span><span class="sxs-lookup"><span data-stu-id="b2a1a-142">Print</span></span>          | <span data-ttu-id="b2a1a-143">列印檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-143">Prints the file.</span></span>                                                     |
| <span data-ttu-id="b2a1a-144">Printto</span><span class="sxs-lookup"><span data-stu-id="b2a1a-144">Printto</span></span>        | <span data-ttu-id="b2a1a-145">允許使用者將檔案拖曳至印表機物件來列印該檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-145">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="b2a1a-146">探索</span><span class="sxs-lookup"><span data-stu-id="b2a1a-146">Explore</span></span>        | <span data-ttu-id="b2a1a-147">開啟 Windows 檔案總管，並選取資料夾。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-147">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="b2a1a-148">屬性</span><span class="sxs-lookup"><span data-stu-id="b2a1a-148">Properties</span></span>     | <span data-ttu-id="b2a1a-149">開啟物件的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-149">Opens the object's property sheet.</span></span>                                   |

> [!Note]  
> <span data-ttu-id="b2a1a-150">**Printto** 動詞也是標準的，但永遠不會顯示。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-150">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="b2a1a-151">它包含可讓使用者將檔案拖曳至印表機物件來列印該檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-151">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

<span data-ttu-id="b2a1a-152">快速鍵功能表處理常式可透過 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 搭配 **Gc \_ VERBW** 或 **gc \_ VERBA** 來提供自己的標準動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-152">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="b2a1a-153">系統會使用標準動詞作為第二個參數， (*lpOperation*) 傳遞至 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)，而是 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)。傳遞至 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)方法的 **lpVerb** 成員。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-153">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="b2a1a-154">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-154">Extended Verbs</span></span>

<span data-ttu-id="b2a1a-155">當使用者以滑鼠右鍵按一下物件時，快捷方式功能表會顯示預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-155">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="b2a1a-156">您可能想要在某些快捷方式功能表上新增和支援命令，而這些快捷方式功能表未顯示在每個快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-156">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="b2a1a-157">例如，您可能會有不常使用或適用于有經驗的使用者的命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-157">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="b2a1a-158">基於這個理由，您也可以定義一或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-158">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="b2a1a-159">這些動詞命令類似于一般動詞，但會透過其註冊方式與一般動詞進行區別。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-159">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="b2a1a-160">若要存取擴充的動詞，使用者必須在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-160">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="b2a1a-161">當使用者這樣做時，除了預設動詞以外，還會顯示擴充的動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-161">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="b2a1a-162">您可以使用登錄來定義一個或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-162">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="b2a1a-163">只有當使用者以滑鼠右鍵按一下物件，同步選取 SHIFT 鍵時，才會顯示相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-163">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="b2a1a-164">若要將動詞定義為擴充，請將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-164">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="b2a1a-165">此值不應該有任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-165">The value should not have any data associated with it.</span></span>

## <a name="programmatic-access-only"></a><span data-ttu-id="b2a1a-166">僅限程式設計存取</span><span class="sxs-lookup"><span data-stu-id="b2a1a-166">Programmatic Access Only</span></span>

<span data-ttu-id="b2a1a-167">這些動詞永遠不會顯示在內容功能表中。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-167">These verbs are never displayed in a context menu.</span></span> <span data-ttu-id="b2a1a-168">您可以使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)來存取這些物件，並在 [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa)物件)  (指定 *pExecInfo* 參數的 **lpVerb** 欄位。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-168">These can be accessed by using [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) and specifying the **lpVerb** field of the *pExecInfo* parameter (a [SHELLEXECUTEINFO](/windows/win32/api/shellapi/ns-shellapi-shellexecuteinfoa) object).</span></span> <span data-ttu-id="b2a1a-169">若要將動詞定義為僅限程式設計存取，請將 "ProgrammaticAccessOnly" **REG \_ SZ** 值新增至動詞的子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-169">To define a verb as programmatic access only, add a "ProgrammaticAccessOnly" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="b2a1a-170">此值不應該有任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-170">The value should not have any data associated with it.</span></span>

<span data-ttu-id="b2a1a-171">您可以使用登錄來定義一個或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-171">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="b2a1a-172">只有當使用者以滑鼠右鍵按一下物件，同步選取 SHIFT 鍵時，才會顯示相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-172">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="b2a1a-173">若要將動詞定義為擴充，請將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-173">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="b2a1a-174">此值不應該有任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-174">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="b2a1a-175">使用靜態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-175">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="b2a1a-176">[為快捷方式功能表選擇靜態或動態動詞命令](shortcut-choose-method.md)之後，您可以註冊檔案類型的靜態動詞命令，以擴充檔案類型的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-176">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="b2a1a-177">若要這樣做，請在與檔案類型相關聯的應用程式 ProgID 的子機碼底下，新增 **Shell** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-177">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="b2a1a-178">（選擇性）您可以為檔案類型定義預設動詞，方法是將它設為 **Shell** 子機碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-178">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="b2a1a-179">預設動詞會先顯示在快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-179">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="b2a1a-180">其目的是在呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函式時提供 Shell 所能使用的動詞命令，但不會指定任何動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-180">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="b2a1a-181">以這種方式使用 **ShellExecuteEx** 時，Shell 不一定會選取預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-181">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="b2a1a-182">Shell 會依下列順序使用第一個可用的動詞：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-182">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="b2a1a-183">預設動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-183">The default verb</span></span>
2.  <span data-ttu-id="b2a1a-184">如果指定了動詞順序，則為登錄中的第一個動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-184">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="b2a1a-185">**Open** 動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-185">The **Open** verb</span></span>
4.  <span data-ttu-id="b2a1a-186">**Open With** 動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-186">The **Open With** verb</span></span>

<span data-ttu-id="b2a1a-187">如果未列出任何可用的動詞，作業就會失敗。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-187">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="b2a1a-188">針對您想要在 Shell 子機碼下新增的每個動詞，各建立一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-188">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="b2a1a-189">這些子機碼中的每個子機碼都必須將 **REG \_ SZ** 值設定為動詞的顯示字串， (當地語系化的字串) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-189">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="b2a1a-190">針對每個動詞子機碼，建立命令子機碼，並將預設值設定為啟用專案的命令列。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-190">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="b2a1a-191">針對標準動詞，例如 [ **開啟** ] 和 [ **列印**]，您可以省略顯示字串，因為系統會自動顯示適當的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-191">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="b2a1a-192">針對 noncanonical 動詞，如果您省略顯示字串，則會顯示動詞字串。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-192">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="b2a1a-193">在下列登錄範例中，請注意：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-193">In the following registry example, note that:</span></span>

-   <span data-ttu-id="b2a1a-194">因為 **doit r** 不是標準動詞，所以會將顯示名稱指派給它，您可以按 D 鍵加以選取。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-194">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="b2a1a-195">**Printto** 動詞未出現在快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-195">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="b2a1a-196">不過，它包含在登錄中可讓使用者藉由將檔案放在印表機圖示上來進行列印。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-196">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="b2a1a-197">每個動詞都會顯示一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-197">One subkey is shown for each verb.</span></span> <span data-ttu-id="b2a1a-198">**%1** 代表檔案名和 **%2** 印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-198">**%1** represents the file name and **%2** the printer name.</span></span>

```
HKEY_CLASSES_ROOT
   .myp-ms
      (Default) = MyProgram.1
      MyProgram.1
         (Default) = My Program Application
         Shell
            (Default) = doit
            doit
               (Default) = &Do It
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            open
               command
                  (Default) = c:\MyDir\MyProgram.exe /d "%1"
            print
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1"
            printto
               command
                  (Default) = c:\MyDir\MyProgram.exe /p "%1" "%2"
```

<span data-ttu-id="b2a1a-199">下圖說明以上述登錄專案為依據的快捷方式功能表延伸。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-199">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="b2a1a-200">此快捷方式功能表在其功能表上已 **開啟**、 **完成** 及 **列印** 動詞命令，並將 **其做** 為預設動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-200">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![[做為預設動詞] 快捷方式功能表的螢幕擷取畫面](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="b2a1a-202">使用 IDropTarget 介面啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="b2a1a-202">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="b2a1a-203">動態資料交換 (的 DDE) 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-203">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="b2a1a-204">**IDropTarget** 更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟動。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-204">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="b2a1a-205">如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-205">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="b2a1a-206">此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-206">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="b2a1a-207">這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-207">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="b2a1a-208">如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-208">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="b2a1a-209">指定靜態動詞命令的位置和順序</span><span class="sxs-lookup"><span data-stu-id="b2a1a-209">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="b2a1a-210">通常動詞命令會根據其列舉方式在快捷方式功能表上排序;列舉是根據關聯陣列的順序，接著是關聯陣列中專案的順序，如登錄的排序次序所定義。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-210">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="b2a1a-211">您可以針對關聯專案指定 Shell 子機碼的預設值來排序動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-211">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="b2a1a-212">這個預設值可以包含單一專案，這會顯示在快捷方式功能表的頂端位置，或是以空格或逗號分隔的專案清單。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-212">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="b2a1a-213">在後者的情況下，清單中的第一個專案是預設專案，而其他動詞會依照指定的順序顯示在其下方。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-213">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="b2a1a-214">例如，下列登錄專案會依下列順序產生快捷方式功能表動詞：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-214">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="b2a1a-215">顯示</span><span class="sxs-lookup"><span data-stu-id="b2a1a-215">Display</span></span>
2.  <span data-ttu-id="b2a1a-216">小工具</span><span class="sxs-lookup"><span data-stu-id="b2a1a-216">Gadgets</span></span>
3.  <span data-ttu-id="b2a1a-217">個人化</span><span class="sxs-lookup"><span data-stu-id="b2a1a-217">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="b2a1a-218">同樣地，下列登錄專案會依下列順序產生快捷方式功能表動詞：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-218">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="b2a1a-219">個人化</span><span class="sxs-lookup"><span data-stu-id="b2a1a-219">Personalization</span></span>
2.  <span data-ttu-id="b2a1a-220">小工具</span><span class="sxs-lookup"><span data-stu-id="b2a1a-220">Gadgets</span></span>
3.  <span data-ttu-id="b2a1a-221">顯示</span><span class="sxs-lookup"><span data-stu-id="b2a1a-221">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="b2a1a-222">將動詞放置於功能表頂端或底部</span><span class="sxs-lookup"><span data-stu-id="b2a1a-222">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="b2a1a-223">下列登錄屬性可以用來將動詞放置在功能表的頂端或底部。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-223">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="b2a1a-224">如果有多個動詞指定此屬性，則最後一個會取得優先順序：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-224">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="b2a1a-225">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-225">Creating Static Cascading Menus</span></span>

<span data-ttu-id="b2a1a-226">在 Windows 7 （含）以後版本中，透過登錄設定支援串聯功能表的執行。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-226">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="b2a1a-227">在 Windows 7 之前，只能透過 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面的執行來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-227">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="b2a1a-228">在 Windows 7 （含）以後版本中，您應該只在靜態方法不足時，才需要採用以 COM 程式碼為基礎的解決方案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-228">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="b2a1a-229">下列螢幕擷取畫面提供串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-229">The following screen shot provides an example of a cascading menu.</span></span>

![顯示級聯功能表範例的螢幕擷取畫面](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="b2a1a-231">在 Windows 7 和更新版本中，有三種方式可以建立串聯功能表：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-231">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="b2a1a-232">使用子命令登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-232">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="b2a1a-233">使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-233">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="b2a1a-234">使用 IExplorerCommand 介面建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-234">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="b2a1a-235">使用子命令登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-235">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="b2a1a-236">在 Windows 7 （含）以後版本中，您可以使用下列程式，使用子命令專案來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-236">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="b2a1a-237">**使用子命令專案建立串聯功能表**</span><span class="sxs-lookup"><span data-stu-id="b2a1a-237">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="b2a1a-238">在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-238">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="b2a1a-239">在此範例中，我們會為此子機碼命名為 *CascadeTest*。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-239">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="b2a1a-240">請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-240">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="b2a1a-241">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-241">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="b2a1a-242">在此範例中，我們將它指派為「測試 Cascade 功能表」。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-242">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="b2a1a-243">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的子命令專案，這個專案是由分號所指派的動詞命令（以分號 demlimited），並以外觀順序顯示。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-243">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="b2a1a-244">例如，我們在這裡指派了許多系統提供的動詞：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-244">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="b2a1a-245">在自訂動詞命令的情況下，請使用任何靜態動詞實方法來加以執行，並在 **CommandStore** 子機碼底下列出它們，如下列虛構動詞 *VerbName* 的範例所示：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-245">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      CommandStore
                         Shell
                            VerbName
                            command
                               (Default) = notepad.exe %1
    ```

> [!Note]  
> <span data-ttu-id="b2a1a-246">這個方法的優點是，自訂動詞命令可以註冊一次，並藉由列出子命令專案下的動詞名稱重複使用。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-246">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="b2a1a-247">但是，應用程式需要有許可權才能修改 **HKEY \_ 本機 \_ 電腦** 下的登錄。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-247">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="b2a1a-248">使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-248">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="b2a1a-249">在 Windows 7 和更新版本中，您可以使用 ExtendedSubCommandKey 專案來建立擴充的串聯功能表：串聯功能表中的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-249">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="b2a1a-250">下列螢幕擷取畫面是延伸串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-250">The following screen shot is an example of an extended cascading menu.</span></span>

![顯示裝置的擴充串聯功能表的螢幕擷取畫面](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="b2a1a-252">由於 **HKEY \_ 類別 \_ 根目錄** 是 **HKEY \_ 目前 \_ 使用者** 和 **HKEY \_ 本機 \_ 電腦** 的組合，因此您可以在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼下註冊任何自訂動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-252">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="b2a1a-253">這麼做的主要優點是不需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-253">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="b2a1a-254">此外，其他檔案關聯也可以藉由指定相同的 ExtendedSubCommandsKey 子機碼，重複使用這整組動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-254">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="b2a1a-255">如果您不需要重複使用這組動詞，可以列出父系底下的動詞命令，但是確定父系的預設值是空的。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-255">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="b2a1a-256">**使用 ExtendedSubCommandsKey 專案建立串聯功能表**</span><span class="sxs-lookup"><span data-stu-id="b2a1a-256">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="b2a1a-257">在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-257">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="b2a1a-258">在此範例中，我們會為此子機碼命名為 *CascadeTest2*。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-258">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="b2a1a-259">請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-259">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="b2a1a-260">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-260">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="b2a1a-261">在此範例中，我們將它指派為「測試 Cascade 功能表」。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-261">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="b2a1a-262">在您所建立的 *CascadeTest* 子機碼底下，新增 **ExtendedSubCommandsKey** 子機碼，然後將 (**REG \_ SZ** 類型的檔子命令新增) ; 例如：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-262">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtfile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Layout
                   Properties
                   Select all
    ```

    <span data-ttu-id="b2a1a-263">確定 [ *測試串聯功能表 2* ] 子機碼的預設值是空的，而且顯示為 [ **未設定) 的 (值**]。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-263">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="b2a1a-264">使用下列任何靜態動詞命令來填入 subverbs。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-264">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="b2a1a-265">請注意，CommandFlags 子機碼代表 EXPCMDFLAGS 值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-265">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="b2a1a-266">如果您想要在 cascade 功能表項目之前或之後加入分隔符號，請使用 ECF \_ SEPARATORBEFORE (0x20) 或 ECF \_ SEPARATORAFTER (0x40) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-266">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="b2a1a-267">如需這些 Windows 7 及更新版本旗標的說明，請參閱 [**IExplorerCommand：： GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-267">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="b2a1a-268">ECF \_ SEPARATORBEFORE 僅適用于最上層的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-268">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="b2a1a-269">MUIVerb 的類型為 **reg \_ SZ**，而 CommandFlags 的類型為 **reg \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-269">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       txtile
          Shell
             Test Cascade Menu 2
                (Default)
                ExtendedSubCommandsKey
                   Shell
                      cmd1
                         MUIVerb = Notepad
                         command
                            (Default) = %SystemRoot%\system32\notepad.exe %1
                      cmd2
                         MUIVerb = Wordpad
                         CommandFlags = 0x20
                         command
                            (Default) = "C:\Program Files\Windows NT\Accessories\wordpad.exe" %1
    ```

<span data-ttu-id="b2a1a-270">下列螢幕擷取畫面是先前的登錄機碼專案範例的圖例。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-270">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![顯示顯示 [記事本] 和 [wordpad] 選項之級聯功能表範例的螢幕擷取畫面](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="b2a1a-272">使用 IExplorerCommand 介面建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-272">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="b2a1a-273">將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-273">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="b2a1a-274">這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-274">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="b2a1a-275">在 Windows 7 （含）以後版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 來提供相同的動詞實行，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)一樣。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-275">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="b2a1a-276">以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-276">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/filecascademenu.png)

<span data-ttu-id="b2a1a-278">下列螢幕擷取畫面說明 [ **裝置** ] 資料夾中串聯功能表的另一個執行。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-278">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="b2a1a-280">因為 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 僅支援同進程啟用，所以建議您在需要于命令和快捷方式功能表之間共用執行的 Shell 資料來源使用。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-280">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="b2a1a-281">使用 Advanced Query 語法取得靜態動詞命令的動態行為</span><span class="sxs-lookup"><span data-stu-id="b2a1a-281">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="b2a1a-282">Advanced Query 語法 (AQS) 可以表達要使用為其具現化動詞之專案的屬性進行評估的條件。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-282">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="b2a1a-283">這個系統只適用于快速屬性。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-283">This system works only with fast properties.</span></span> <span data-ttu-id="b2a1a-284">這些是 Shell 資料來源回報的屬性，不會從 [**IShellFolder2：： GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)傳回 [\* \* \* \* SHCOLSTATE \_ 慢 \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* \*。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-284">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="b2a1a-285">Windows 7 和更新版本支援可避免當地語系化組建問題的標準值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-285">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="b2a1a-286">當地語系化的組建需要下列標準語法，才能利用此 Windows 7 增強功能。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-286">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="b2a1a-287">在下列範例登錄專案中：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-287">In the following example registry entry:</span></span>

-   <span data-ttu-id="b2a1a-288">**AppliesTo** 值會控制是否要顯示或隱藏動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-288">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="b2a1a-289">DefaultAppliesTo 值控制預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-289">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="b2a1a-290">HasLUAShield 值會控制是否顯示使用者帳戶控制 (UAC) 盾牌。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-290">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="b2a1a-291">在此範例中， **DefaultAppliesTo** 值會讓這個動詞成為其檔案名中有 "exampleText1" 這個字的任何檔案的預設值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-291">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="b2a1a-292">**AppliesTo** 值會啟用名稱中有 "exampleText1" 之任何檔案的動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-292">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="b2a1a-293">**HasLUAShield** 值會顯示名稱中有 "exampleText2" 的檔案盾牌。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-293">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="b2a1a-294">新增 **命令** 子機碼和值：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-294">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="b2a1a-295">在 Windows 7 登錄中，請參閱 **HKEY \_ 類別 \_ 根** \\ **磁片磁碟機** 作為使用下列方法的 bitlocker 動詞範例：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-295">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="b2a1a-296">AppliesTo = BitlockerProtection： = 2</span><span class="sxs-lookup"><span data-stu-id="b2a1a-296">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="b2a1a-297">BitlockerRequiresAdmin： = StructuredQueryType。布林 \# 值 True</span><span class="sxs-lookup"><span data-stu-id="b2a1a-297">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="b2a1a-298">如需 AQS 的詳細資訊，請參閱 [Advanced Query 語法](../search/-search-3x-advancedquerysyntax.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-298">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="b2a1a-299">已淘汰：將動詞與動態資料交換命令建立關聯</span><span class="sxs-lookup"><span data-stu-id="b2a1a-299">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="b2a1a-300">DDE 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-300">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="b2a1a-301">DDE 已被取代，因為它依賴廣播視窗訊息來探索 DDE 伺服器。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-301">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="b2a1a-302">DDE 伺服器會停止回應廣播視窗訊息，因此會讓其他應用程式的 DDE 交談停止回應。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-302">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="b2a1a-303">單一停滯的應用程式通常會在使用者的體驗中造成後續的停止回應。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-303">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="b2a1a-304">[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)方法更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟用。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-304">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="b2a1a-305">如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-305">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="b2a1a-306">此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-306">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="b2a1a-307">這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-307">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="b2a1a-308">如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-308">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="b2a1a-309">完成動詞執行工作</span><span class="sxs-lookup"><span data-stu-id="b2a1a-309">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="b2a1a-310">下列用來執行動詞命令的工作，與靜態和動態動詞命令都有關。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-310">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="b2a1a-311">如需動態動詞命令的詳細資訊，請參閱 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-311">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="b2a1a-312">自訂預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-312">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="b2a1a-313">許多預先定義的 Shell 物件都具有可自訂的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-313">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="b2a1a-314">註冊命令的方式與註冊一般檔案類型的方式非常類似，但請使用預先定義的物件名稱做為檔案類型名稱。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-314">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="b2a1a-315">預先定義的物件清單位於 [建立 Shell 延伸模組處理常式](handlers.md)的 *預先定義 Shell 物件* 區段中。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-315">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="b2a1a-316">這些預先定義的 Shell 物件，其快捷方式功能表可透過在登錄中新增動詞來自訂，並在包含單字動詞的表格中標示。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-316">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="b2a1a-317">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-317">Extending a New Submenu</span></span>

<span data-ttu-id="b2a1a-318">當使用者在 Windows 檔案總管中開啟 [檔案 **] 功能表時** ，其中一個顯示的命令是 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-318">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="b2a1a-319">選取此命令會顯示子功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-319">Selecting this command displays a submenu.</span></span> <span data-ttu-id="b2a1a-320">依預設，子功能表包含兩個命令： **資料夾** 和 **快捷方式**，可讓使用者建立子資料夾和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-320">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="b2a1a-321">您可以擴充此子功能表，以包含任何檔案類型的檔案建立命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-321">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="b2a1a-322">若要將檔案建立命令新增至 **新** 的子功能表，您的應用程式檔必須有相關聯的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-322">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="b2a1a-323">在檔案名下包含 **ShellNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-323">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="b2a1a-324">選取 [檔案 **] 功能表的** [ **新** 命令] 時，Shell 會將檔案類型加入至 **新** 的子功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-324">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="b2a1a-325">命令的顯示字串是指派給程式 ProgID 的描述性字串。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-325">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="b2a1a-326">若要指定檔案建立方法，請將一或多個資料值指派給 **ShellNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-326">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="b2a1a-327">下表列出可用的值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-327">The available values are listed in the following table.</span></span>



| <span data-ttu-id="b2a1a-328">ShellNew 子機碼值</span><span class="sxs-lookup"><span data-stu-id="b2a1a-328">ShellNew subkey value</span></span> | <span data-ttu-id="b2a1a-329">描述</span><span class="sxs-lookup"><span data-stu-id="b2a1a-329">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a1a-330">命令</span><span class="sxs-lookup"><span data-stu-id="b2a1a-330">Command</span></span>               | <span data-ttu-id="b2a1a-331">執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-331">Executes an application.</span></span> <span data-ttu-id="b2a1a-332">這個 **REG \_ SZ** 值會指定要執行之應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-332">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="b2a1a-333">例如，您可以將它設定為啟動 wizard。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-333">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="b2a1a-334">資料</span><span class="sxs-lookup"><span data-stu-id="b2a1a-334">Data</span></span>                  | <span data-ttu-id="b2a1a-335">建立包含指定資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-335">Creates a file containing specified data.</span></span> <span data-ttu-id="b2a1a-336">這個 **REG \_ 二進位** 值會指定檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-336">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="b2a1a-337">如果指定了 **NullFile** 或 **FileName** ，則會忽略 **資料**。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-337">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="b2a1a-338">FileName</span><span class="sxs-lookup"><span data-stu-id="b2a1a-338">FileName</span></span>              | <span data-ttu-id="b2a1a-339">建立檔案，該檔案為指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-339">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="b2a1a-340">這個 **REG \_ SZ** 值會指定要複製之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-340">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="b2a1a-341">NullFile</span><span class="sxs-lookup"><span data-stu-id="b2a1a-341">NullFile</span></span>              | <span data-ttu-id="b2a1a-342">建立空白檔案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-342">Creates an empty file.</span></span> <span data-ttu-id="b2a1a-343">**NullFile** 尚未指派值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-343">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="b2a1a-344">如果指定 **NullFile** ，則會忽略 **資料** 和 **檔案名** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-344">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="b2a1a-345">下列登錄機碼範例和螢幕擷取畫面說明 myp-ms 檔案類型的 **新** 子功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-345">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="b2a1a-346">它有一個 **Myprogram.exe 應用程式** 命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-346">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="b2a1a-347">螢幕擷取畫面說明 **新** 的子功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-347">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="b2a1a-348">當使用者從 **新** 的子功能表選取 **myprogram.exe 應用程式** 時，Shell 會建立名為 **New myprogram.exe myp 的** 檔案，並將它傳遞至 **MyProgram.exe**。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-348">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![windows explorer 的螢幕擷取畫面，在 [新增] 子功能表上顯示新的 [myprogram.exe 應用程式] 命令](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="b2a1a-350">建立拖放處理常式</span><span class="sxs-lookup"><span data-stu-id="b2a1a-350">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="b2a1a-351">執行拖放處理常式的基本程式與傳統快捷方式功能表處理常式的基本程式相同。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-351">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="b2a1a-352">不過，快捷方式功能表處理常式通常只會使用傳遞給處理常式之 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標，來將物件的名稱解壓縮。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-352">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="b2a1a-353">拖放處理常式可以執行更複雜的資料處理程式來修改拖曳物件的行為。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-353">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="b2a1a-354">當使用者以滑鼠右鍵按一下 Shell 物件來拖曳物件時，會在使用者嘗試卸載物件時顯示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-354">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="b2a1a-355">下列螢幕擷取畫面說明典型的拖放快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-355">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![拖放快捷方式功能表的螢幕擷取畫面](images/context-menu/context-dragdrop.png)

<span data-ttu-id="b2a1a-357">拖放處理常式是快捷方式功能表處理常式，可將專案加入這個快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-357">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="b2a1a-358">拖放處理常式通常會在下列子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-358">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="b2a1a-359">在名為的拖放處理常式的 **DragDropHandlers** 子機碼下新增子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串形式 (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-359">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="b2a1a-360">下列範例會啟用 **MyDD** 拖放處理常式。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-360">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="b2a1a-361">隱藏動詞和控制可見度</span><span class="sxs-lookup"><span data-stu-id="b2a1a-361">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="b2a1a-362">您可以使用 Windows 原則設定來控制動詞可視性。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-362">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="b2a1a-363">藉由將 **SuppressionPolicy** 值或 **SuppressionPolicyEx** GUID 值新增至動詞的登錄子機碼，就可以透過原則設定來隱藏動詞命令。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-363">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="b2a1a-364">將 **SuppressionPolicy** 子機碼的值設定為原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-364">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="b2a1a-365">如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-365">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="b2a1a-366">如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-366">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="b2a1a-367">採用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="b2a1a-367">Employing the Verb Selection Model</span></span>

<span data-ttu-id="b2a1a-368">您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-368">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="b2a1a-369">針對此動詞支援的三種情況，動詞都需要個別的登錄值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-369">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="b2a1a-370">動詞選取模型的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-370">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="b2a1a-371">指定所有動詞的 MultiSelectModel 值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-371">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="b2a1a-372">如果未指定 MultiSelectModel 值，則會從您選擇的動詞執行類型推斷。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-372">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="b2a1a-373">針對以 COM 為基礎的方法 (例如 DropTarget 和 ExecuteCommand) **播放** 程式，並假設為其他方法 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-373">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="b2a1a-374">針對僅支援單一選取專案的動詞指定 **single** 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-374">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="b2a1a-375">針對支援任意數量專案的動詞指定 **播放** 程式。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-375">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="b2a1a-376">針對每個專案建立最上層視窗的動詞命令指定 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-376">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="b2a1a-377">這麼做會限制啟用的專案數目，如果使用者開啟太多視窗，則有助於避免系統資源不足。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-377">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="b2a1a-378">當選取的專案數目不符合動詞選取模型，或大於下表所述的預設限制時，就無法顯示該動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-378">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="b2a1a-379">動詞執行的類型</span><span class="sxs-lookup"><span data-stu-id="b2a1a-379">Type of verb implementation</span></span> | <span data-ttu-id="b2a1a-380">文件</span><span class="sxs-lookup"><span data-stu-id="b2a1a-380">Document</span></span> | <span data-ttu-id="b2a1a-381">播放器</span><span class="sxs-lookup"><span data-stu-id="b2a1a-381">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="b2a1a-382">舊版</span><span class="sxs-lookup"><span data-stu-id="b2a1a-382">Legacy</span></span>                      | <span data-ttu-id="b2a1a-383">15個專案</span><span class="sxs-lookup"><span data-stu-id="b2a1a-383">15 items</span></span> | <span data-ttu-id="b2a1a-384">100專案</span><span class="sxs-lookup"><span data-stu-id="b2a1a-384">100 items</span></span> |
| <span data-ttu-id="b2a1a-385">COM</span><span class="sxs-lookup"><span data-stu-id="b2a1a-385">COM</span></span>                         | <span data-ttu-id="b2a1a-386">15個專案</span><span class="sxs-lookup"><span data-stu-id="b2a1a-386">15 items</span></span> | <span data-ttu-id="b2a1a-387">沒有限制</span><span class="sxs-lookup"><span data-stu-id="b2a1a-387">No limit</span></span>  |



 

<span data-ttu-id="b2a1a-388">以下是使用 MultiSelectModel 值的範例登錄專案。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-388">The following are example registry entries using the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

### <a name="using-item-attributes"></a><span data-ttu-id="b2a1a-389">使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="b2a1a-389">Using Item Attributes</span></span>

<span data-ttu-id="b2a1a-390">您可以測試專案之 Shell 屬性的 [**SFGAO**](sfgao.md) 旗標值，以判斷是否應啟用或停用動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-390">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="b2a1a-391">若要使用此屬性功能，請在下列動詞命令底下新增下列 **REG \_ DWORD** 值：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-391">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="b2a1a-392">AttributeMask 值會指定要測試之遮罩的位值 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-392">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="b2a1a-393">AttributeValue 值會指定所測試之位的 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-393">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="b2a1a-394">ImpliedSelectionModel 為專案動詞指定零，或在背景快捷方式功能表上指定非零的動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-394">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="b2a1a-395">在下列範例登錄專案中，AttributeMask 會設定為 [**SFGAO \_ READONLY**](sfgao.md) (0x40000) 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-395">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         test.verb2
            AttributeMask = 0x40000
            AttributeValue = 0x0
            ImpliedSelectionModel = 0x0
            command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="b2a1a-396">透過 Desktop.ini 為資料夾執行自訂動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-396">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="b2a1a-397">在 Windows 7 和更新版本中，您可以透過 Desktop.ini 將動詞新增至資料夾。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-397">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="b2a1a-398">如需 Desktop.ini 檔案的詳細資訊，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-398">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="b2a1a-399">Desktop.ini 的檔案應該一律標示為  +  **隱藏** 系統，使其不會顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-399">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="b2a1a-400">**若要透過 Desktop.ini 檔案新增資料夾的自訂動詞命令，請執行下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="b2a1a-400">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="b2a1a-401">建立標示為 **唯讀** 或 **系統** 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-401">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="b2a1a-402">建立包含的 Desktop.ini 檔案 \[ 。ShellClassInfo \] DirectoryClass = Folder ProgID。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-402">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="b2a1a-403">在登錄中，建立具有值 CanUseForDirectory 的 **HKEY \_ 類別 \_ 根** \\ **資料夾 ProgID** 。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-403">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="b2a1a-404">CanUseForDirectory 值可避免誤用未設定為透過 Desktop.ini 為資料夾執行自訂動詞命令的 Progid。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-404">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="b2a1a-405">在 **資料夾** ProgID 子機碼底下新增動詞，例如：</span><span class="sxs-lookup"><span data-stu-id="b2a1a-405">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="b2a1a-406">這些動詞命令可以是預設動詞，在此情況下，按兩下資料夾會啟動動詞。</span><span class="sxs-lookup"><span data-stu-id="b2a1a-406">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b2a1a-407">相關主題</span><span class="sxs-lookup"><span data-stu-id="b2a1a-407">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2a1a-408">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="b2a1a-408">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="b2a1a-409">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="b2a1a-409">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="b2a1a-410">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b2a1a-410">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="b2a1a-411">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="b2a1a-411">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="b2a1a-412">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="b2a1a-412">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="b2a1a-413">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="b2a1a-413">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 

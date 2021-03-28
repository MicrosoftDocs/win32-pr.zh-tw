---
description: 快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。 就像所有這類處理常式一樣，它們都是同進程元件物件模型， (COM) 物件實作為 Dll。
ms.assetid: cff79cdc-8a01-4575-9af7-2a485c6a8e46
title: 建立快捷方式功能表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b7091483726c322a8ae18bace883af126d404
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "103853192"
---
# <a name="creating-shortcut-menu-handlers"></a><span data-ttu-id="fbc09-104">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="fbc09-104">Creating Shortcut Menu Handlers</span></span>

<span data-ttu-id="fbc09-105">快速鍵功能表處理常式（也稱為內容功能表處理常式或動詞處理常式）是檔案類型處理常式的類型。</span><span class="sxs-lookup"><span data-stu-id="fbc09-105">Shortcut menu handlers, also known as context menu handlers or verb handlers, are a type of file type handler.</span></span> <span data-ttu-id="fbc09-106">就像所有這類處理常式一樣，它們都是同進程元件物件模型， (COM) 物件實作為 Dll。</span><span class="sxs-lookup"><span data-stu-id="fbc09-106">Like all such handlers, they are in-process Component Object Model (COM) objects implemented as DLLs.</span></span>

> [!Note]  
> <span data-ttu-id="fbc09-107">註冊在32位應用程式內容中運作的處理常式時，會有64位 Windows 的特殊考慮：當 Shell 動詞命令在32位應用程式的內容中叫用時，WOW64 子系統會將檔案系統存取重新導向至某些路徑。</span><span class="sxs-lookup"><span data-stu-id="fbc09-107">There are special considerations for 64-bit Windows when registering handlers that work in the context of 32-bit applications: when Shell verbs are invoked in the context of a 32-bit application, the WOW64 subsystem redirects file system access to some paths.</span></span> <span data-ttu-id="fbc09-108">如果您的 .exe 處理常式儲存在其中一個路徑中，就無法在此內容中存取。</span><span class="sxs-lookup"><span data-stu-id="fbc09-108">If your .exe handler is stored in one of those paths, it is not accessible in this context.</span></span> <span data-ttu-id="fbc09-109">因此，若要解決這個問題，請將 .exe 儲存在未重新導向的路徑中，或儲存啟動實際版本之 .exe 的存根版本。</span><span class="sxs-lookup"><span data-stu-id="fbc09-109">Therefore, as a work around, either store your .exe in a path that does not get redirected, or store a stub version of your .exe that launches the real version.</span></span>

 

<span data-ttu-id="fbc09-110">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="fbc09-110">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="fbc09-111">標準動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-111">Canonical Verbs</span></span>](#canonical-verbs)
-   [<span data-ttu-id="fbc09-112">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="fbc09-113">使用靜態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-113">Customizing a Shortcut Menu Using Static Verbs</span></span>](#customizing-a-shortcut-menu-using-static-verbs)
    -   [<span data-ttu-id="fbc09-114">使用 IDropTarget 介面啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="fbc09-114">Activating Your Handler Using the IDropTarget Interface</span></span>](#activating-your-handler-using-the-idroptarget-interface)
    -   [<span data-ttu-id="fbc09-115">指定靜態動詞命令的位置和順序</span><span class="sxs-lookup"><span data-stu-id="fbc09-115">Specifying the Position and Order of Static Verbs</span></span>](#specifying-the-position-and-order-of-static-verbs)
    -   [<span data-ttu-id="fbc09-116">將動詞放置於功能表頂端或底部</span><span class="sxs-lookup"><span data-stu-id="fbc09-116">Positioning Verbs at the Top or Bottom of the Menu</span></span>](#positioning-verbs-at-the-top-or-bottom-of-the-menu)
    -   [<span data-ttu-id="fbc09-117">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-117">Creating Static Cascading Menus</span></span>](#creating-static-cascading-menus)
    -   [<span data-ttu-id="fbc09-118">使用 Advanced Query 語法取得靜態動詞命令的動態行為</span><span class="sxs-lookup"><span data-stu-id="fbc09-118">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>](#getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax)
    -   [<span data-ttu-id="fbc09-119">已淘汰：將動詞與動態資料交換命令建立關聯</span><span class="sxs-lookup"><span data-stu-id="fbc09-119">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>](#deprecated-associating-verbs-with-dynamic-data-exchange-commands)
-   [<span data-ttu-id="fbc09-120">完成動詞執行工作</span><span class="sxs-lookup"><span data-stu-id="fbc09-120">Completing Verb Implementation Tasks</span></span>](#completing-verb-implementation-tasks)
    -   [<span data-ttu-id="fbc09-121">自訂預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-121">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>](#customizing-the-shortcut-menu-for-predefined-shell-objects)
    -   [<span data-ttu-id="fbc09-122">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-122">Extending a New Submenu</span></span>](#extending-a-new-submenu)
    -   [<span data-ttu-id="fbc09-123">隱藏動詞和控制可見度</span><span class="sxs-lookup"><span data-stu-id="fbc09-123">Suppressing Verbs and Controlling Visibility</span></span>](#suppressing-verbs-and-controlling-visibility)
    -   [<span data-ttu-id="fbc09-124">採用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="fbc09-124">Employing the Verb Selection Model</span></span>](#employing-the-verb-selection-model)
    -   [<span data-ttu-id="fbc09-125">使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="fbc09-125">Using Item Attributes</span></span>](#using-item-attributes)
    -   [<span data-ttu-id="fbc09-126">透過 Desktop.ini為資料夾執行自訂動詞 </span><span class="sxs-lookup"><span data-stu-id="fbc09-126">Implementing Custom Verbs for Folders through Desktop.ini</span></span>](#implementing-custom-verbs-for-folders-through-desktopini)
-   [<span data-ttu-id="fbc09-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbc09-127">Related topics</span></span>](#related-topics)

## <a name="canonical-verbs"></a><span data-ttu-id="fbc09-128">標準動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-128">Canonical Verbs</span></span>

<span data-ttu-id="fbc09-129">應用程式通常負責為其定義的動詞提供當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="fbc09-129">Applications are generally responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="fbc09-130">不過，為了提供某種程度的語言獨立性，系統會定義一組標準的常用動詞，稱為標準動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-130">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called canonical verbs.</span></span> <span data-ttu-id="fbc09-131">標準動詞永遠不會向使用者顯示，而且可以搭配任何 UI 語言使用。</span><span class="sxs-lookup"><span data-stu-id="fbc09-131">A canonical verb is never displayed to the user, and can be used with any UI language.</span></span> <span data-ttu-id="fbc09-132">系統會使用標準名稱自動產生適當當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="fbc09-132">The system uses the canonical name to automatically generate a properly localized display string.</span></span> <span data-ttu-id="fbc09-133">例如，開啟動詞的顯示字串會設定為在英文系統上 **開啟** ，以及德文系統上的德文對等專案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-133">For instance, the open verb's display string is set to **Open** on an English system, and to the German equivalent on a German system.</span></span>



| <span data-ttu-id="fbc09-134">標準動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-134">Canonical verb</span></span> | <span data-ttu-id="fbc09-135">Description</span><span class="sxs-lookup"><span data-stu-id="fbc09-135">Description</span></span>                                                          |
|----------------|----------------------------------------------------------------------|
| <span data-ttu-id="fbc09-136">開啟</span><span class="sxs-lookup"><span data-stu-id="fbc09-136">Open</span></span>           | <span data-ttu-id="fbc09-137">開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="fbc09-137">Opens the file or folder.</span></span>                                            |
| <span data-ttu-id="fbc09-138">Opennew</span><span class="sxs-lookup"><span data-stu-id="fbc09-138">Opennew</span></span>        | <span data-ttu-id="fbc09-139">在新視窗中開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="fbc09-139">Opens the file or folder in a new window.</span></span>                            |
| <span data-ttu-id="fbc09-140">列印</span><span class="sxs-lookup"><span data-stu-id="fbc09-140">Print</span></span>          | <span data-ttu-id="fbc09-141">列印檔案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-141">Prints the file.</span></span>                                                     |
| <span data-ttu-id="fbc09-142">Printto</span><span class="sxs-lookup"><span data-stu-id="fbc09-142">Printto</span></span>        | <span data-ttu-id="fbc09-143">允許使用者將檔案拖曳至印表機物件來列印該檔案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-143">Permits the user to print a file by dragging it to a printer object.</span></span> |
| <span data-ttu-id="fbc09-144">探索</span><span class="sxs-lookup"><span data-stu-id="fbc09-144">Explore</span></span>        | <span data-ttu-id="fbc09-145">開啟 Windows 檔案總管，並選取資料夾。</span><span class="sxs-lookup"><span data-stu-id="fbc09-145">Opens Windows Explorer with the folder selected.</span></span>                     |
| <span data-ttu-id="fbc09-146">屬性</span><span class="sxs-lookup"><span data-stu-id="fbc09-146">Properties</span></span>     | <span data-ttu-id="fbc09-147">開啟物件的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-147">Opens the object's property sheet.</span></span>                                   |



 

> [!Note]  
> <span data-ttu-id="fbc09-148">**Printto** 動詞也是標準的，但永遠不會顯示。</span><span class="sxs-lookup"><span data-stu-id="fbc09-148">The **Printto** verb is also canonical, but it is never displayed.</span></span> <span data-ttu-id="fbc09-149">它包含可讓使用者將檔案拖曳至印表機物件來列印該檔案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-149">Its inclusion enables the user to print a file by dragging it to a printer object.</span></span>

 

<span data-ttu-id="fbc09-150">快速鍵功能表處理常式可透過 [**ICoNtextMenu：： GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) 搭配 **Gc \_ VERBW** 或 **gc \_ VERBA** 來提供自己的標準動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-150">Shortcut menu handlers can provide their own canonical verbs through [**IContextMenu::GetCommandString**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-getcommandstring) with **GCS\_VERBW**, or **GCS\_VERBA**.</span></span> <span data-ttu-id="fbc09-151">系統會使用標準動詞作為第二個參數， (*lpOperation*) 傳遞至 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)，而是 [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo)。傳遞至 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)方法的 **lpVerb** 成員。</span><span class="sxs-lookup"><span data-stu-id="fbc09-151">The system will use the canonical verbs as the second parameter (*lpOperation*) passed to [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), and is the [**CMINVOKECOMMANDINFO**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo).**lpVerb** member passed to the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method.</span></span>

## <a name="extended-verbs"></a><span data-ttu-id="fbc09-152">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-152">Extended Verbs</span></span>

<span data-ttu-id="fbc09-153">當使用者以滑鼠右鍵按一下物件時，快捷方式功能表會顯示預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-153">When the user right-clicks an object, the shortcut menu displays the default verbs.</span></span> <span data-ttu-id="fbc09-154">您可能想要在某些快捷方式功能表上新增和支援命令，而這些快捷方式功能表未顯示在每個快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="fbc09-154">You might want to add and support commands on some shortcut menus that are not displayed on every shortcut menu.</span></span> <span data-ttu-id="fbc09-155">例如，您可能會有不常使用或適用于有經驗的使用者的命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-155">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="fbc09-156">基於這個理由，您也可以定義一或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-156">For this reason, you can also define one or more extended verbs.</span></span> <span data-ttu-id="fbc09-157">這些動詞命令類似于一般動詞，但會透過其註冊方式與一般動詞進行區別。</span><span class="sxs-lookup"><span data-stu-id="fbc09-157">These verbs are similar to normal verbs, but are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="fbc09-158">若要存取擴充的動詞，使用者必須在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件。</span><span class="sxs-lookup"><span data-stu-id="fbc09-158">To have access to extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="fbc09-159">當使用者這樣做時，除了預設動詞以外，還會顯示擴充的動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-159">When the user does so, the extended verbs are displayed in addition to the default verbs.</span></span>

<span data-ttu-id="fbc09-160">您可以使用登錄來定義一個或多個擴充動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-160">You can use the registry to define one or more extended verbs.</span></span> <span data-ttu-id="fbc09-161">只有當使用者以滑鼠右鍵按一下物件，同步選取 SHIFT 鍵時，才會顯示相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-161">The associated commands will be displayed only when the user right-clicks an object while also pressing the SHIFT key.</span></span> <span data-ttu-id="fbc09-162">若要將動詞定義為擴充，請將 "extended" **REG \_ SZ** 值新增至動詞的子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-162">To define a verb as extended, add an "extended" **REG\_SZ** value to the verb's subkey.</span></span> <span data-ttu-id="fbc09-163">此值不應該有任何與其相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="fbc09-163">The value should not have any data associated with it.</span></span>

## <a name="customizing-a-shortcut-menu-using-static-verbs"></a><span data-ttu-id="fbc09-164">使用靜態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-164">Customizing a Shortcut Menu Using Static Verbs</span></span>

<span data-ttu-id="fbc09-165">[為快捷方式功能表選擇靜態或動態動詞命令](shortcut-choose-method.md)之後，您可以註冊檔案類型的靜態動詞命令，以擴充檔案類型的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-165">After [Choosing a Static or Dynamic Verb for your Shortcut Menu](shortcut-choose-method.md) you can extend the shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="fbc09-166">若要這樣做，請在與檔案類型相關聯的應用程式 ProgID 的子機碼底下，新增 **Shell** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-166">To do so, add a **Shell** subkey below the subkey for the ProgID of the application associated with the file type.</span></span> <span data-ttu-id="fbc09-167">（選擇性）您可以為檔案類型定義預設動詞，方法是將它設為 **Shell** 子機碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-167">Optionally, you can define a default verb for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="fbc09-168">預設動詞會先顯示在快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="fbc09-168">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="fbc09-169">其目的是在呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 函式時提供 Shell 所能使用的動詞命令，但不會指定任何動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-169">Its purpose is to provide the Shell with a verb it can use when the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) function is called, but no verb is specified.</span></span> <span data-ttu-id="fbc09-170">以這種方式使用 **ShellExecuteEx** 時，Shell 不一定會選取預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-170">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span>

<span data-ttu-id="fbc09-171">Shell 會依下列順序使用第一個可用的動詞：</span><span class="sxs-lookup"><span data-stu-id="fbc09-171">The Shell uses the first available verb in the following order:</span></span>

1.  <span data-ttu-id="fbc09-172">預設動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-172">The default verb</span></span>
2.  <span data-ttu-id="fbc09-173">如果指定了動詞順序，則為登錄中的第一個動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-173">The first verb in the registry, if the verb order is specified</span></span>
3.  <span data-ttu-id="fbc09-174">**Open** 動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-174">The **Open** verb</span></span>
4.  <span data-ttu-id="fbc09-175">**Open With** 動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-175">The **Open With** verb</span></span>

<span data-ttu-id="fbc09-176">如果未列出任何可用的動詞，作業就會失敗。</span><span class="sxs-lookup"><span data-stu-id="fbc09-176">If none of the verbs listed is available, the operation fails.</span></span>

<span data-ttu-id="fbc09-177">針對您想要在 Shell 子機碼下新增的每個動詞，各建立一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-177">Create one subkey for each verb you want to add under the Shell subkey.</span></span> <span data-ttu-id="fbc09-178">這些子機碼中的每個子機碼都必須將 **REG \_ SZ** 值設定為動詞的顯示字串， (當地語系化的字串) 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-178">Each of these subkeys must have a **REG\_SZ** value set to the verb's display string (localized string).</span></span> <span data-ttu-id="fbc09-179">針對每個動詞子機碼，建立命令子機碼，並將預設值設定為啟用專案的命令列。</span><span class="sxs-lookup"><span data-stu-id="fbc09-179">For each verb subkey, create a command subkey with the default value set to the command line for activating the items.</span></span> <span data-ttu-id="fbc09-180">針對標準動詞，例如 [ **開啟** ] 和 [ **列印**]，您可以省略顯示字串，因為系統會自動顯示適當的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="fbc09-180">For canonical verbs, such as **Open** and **Print**, you can omit the display string because the system automatically displays a properly localized string.</span></span> <span data-ttu-id="fbc09-181">針對 noncanonical 動詞，如果您省略顯示字串，則會顯示動詞字串。</span><span class="sxs-lookup"><span data-stu-id="fbc09-181">For noncanonical verbs, if you omit the display string, the verb string is displayed.</span></span>

<span data-ttu-id="fbc09-182">在下列登錄範例中，請注意：</span><span class="sxs-lookup"><span data-stu-id="fbc09-182">In the following registry example, note that:</span></span>

-   <span data-ttu-id="fbc09-183">因為 **doit r** 不是標準動詞，所以會將顯示名稱指派給它，您可以按 D 鍵加以選取。</span><span class="sxs-lookup"><span data-stu-id="fbc09-183">Because **Doit** is not a canonical verb, it is assigned a display name, which can be selected by pressing the D key.</span></span>
-   <span data-ttu-id="fbc09-184">**Printto** 動詞未出現在快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="fbc09-184">The **Printto** verb does not appear on the shortcut menu.</span></span> <span data-ttu-id="fbc09-185">不過，它包含在登錄中可讓使用者藉由將檔案放在印表機圖示上來進行列印。</span><span class="sxs-lookup"><span data-stu-id="fbc09-185">However, its inclusion in the registry enables the user to print files by dropping them on a printer icon.</span></span>
-   <span data-ttu-id="fbc09-186">每個動詞都會顯示一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-186">One subkey is shown for each verb.</span></span> <span data-ttu-id="fbc09-187">**%1** 代表檔案名和 **%2** 印表機的名稱。</span><span class="sxs-lookup"><span data-stu-id="fbc09-187">**%1** represents the file name and **%2** the printer name.</span></span>

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

<span data-ttu-id="fbc09-188">下圖說明以上述登錄專案為依據的快捷方式功能表延伸。</span><span class="sxs-lookup"><span data-stu-id="fbc09-188">The following diagram illustrates the extension of the shortcut menu in accordance with the registry entries above.</span></span> <span data-ttu-id="fbc09-189">此快捷方式功能表在其功能表上已 **開啟**、 **完成** 及 **列印** 動詞命令，並將 **其做** 為預設動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-189">This shortcut menu has **Open**, **Do It**, and **Print** verbs on its menu, with **Do It** as the default verb.</span></span>

![[做為預設動詞] 快捷方式功能表的螢幕擷取畫面](images/context-menu/context-doitdefaultverb.png)

### <a name="activating-your-handler-using-the-idroptarget-interface"></a><span data-ttu-id="fbc09-191">使用 IDropTarget 介面啟用處理常式</span><span class="sxs-lookup"><span data-stu-id="fbc09-191">Activating Your Handler Using the IDropTarget Interface</span></span>

<span data-ttu-id="fbc09-192">動態資料交換 (的 DDE) 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-192">Dynamic Data Exchange (DDE) is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="fbc09-193">**IDropTarget** 更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟動。</span><span class="sxs-lookup"><span data-stu-id="fbc09-193">**IDropTarget** is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="fbc09-194">如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。</span><span class="sxs-lookup"><span data-stu-id="fbc09-194">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="fbc09-195">此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。</span><span class="sxs-lookup"><span data-stu-id="fbc09-195">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="fbc09-196">這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。</span><span class="sxs-lookup"><span data-stu-id="fbc09-196">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="fbc09-197">如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-197">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="specifying-the-position-and-order-of-static-verbs"></a><span data-ttu-id="fbc09-198">指定靜態動詞命令的位置和順序</span><span class="sxs-lookup"><span data-stu-id="fbc09-198">Specifying the Position and Order of Static Verbs</span></span>

<span data-ttu-id="fbc09-199">通常動詞命令會根據其列舉方式在快捷方式功能表上排序;列舉是根據關聯陣列的順序，接著是關聯陣列中專案的順序，如登錄的排序次序所定義。</span><span class="sxs-lookup"><span data-stu-id="fbc09-199">Normally verbs are ordered on a shortcut menu based on how they are enumerated; enumeration is based first on the order of the association array, and then on the order of the items in the association array, as defined by the sort order of the registry.</span></span>

<span data-ttu-id="fbc09-200">您可以針對關聯專案指定 Shell 子機碼的預設值來排序動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-200">Verbs can be ordered by specifying the default value of the Shell subkey for the association entry.</span></span> <span data-ttu-id="fbc09-201">這個預設值可以包含單一專案，這會顯示在快捷方式功能表的頂端位置，或是以空格或逗號分隔的專案清單。</span><span class="sxs-lookup"><span data-stu-id="fbc09-201">This default value can include a single item, which will be displayed at the top position of the shortcut menu, or a list of items separated by spaces or commas.</span></span> <span data-ttu-id="fbc09-202">在後者的情況下，清單中的第一個專案是預設專案，而其他動詞會依照指定的順序顯示在其下方。</span><span class="sxs-lookup"><span data-stu-id="fbc09-202">In the latter case, the first item in the list is the default item, and the other verbs are displayed immediately below it in the order specified.</span></span>

<span data-ttu-id="fbc09-203">例如，下列登錄專案會依下列順序產生快捷方式功能表動詞：</span><span class="sxs-lookup"><span data-stu-id="fbc09-203">For example, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="fbc09-204">顯示</span><span class="sxs-lookup"><span data-stu-id="fbc09-204">Display</span></span>
2.  <span data-ttu-id="fbc09-205">小工具</span><span class="sxs-lookup"><span data-stu-id="fbc09-205">Gadgets</span></span>
3.  <span data-ttu-id="fbc09-206">個人化</span><span class="sxs-lookup"><span data-stu-id="fbc09-206">Personalization</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell
         Display
         Gadgets
         Personalization
```

<span data-ttu-id="fbc09-207">同樣地，下列登錄專案會依下列順序產生快捷方式功能表動詞：</span><span class="sxs-lookup"><span data-stu-id="fbc09-207">Similarly, the following registry entry produces shortcut menu verbs in the following order:</span></span>

1.  <span data-ttu-id="fbc09-208">個人化</span><span class="sxs-lookup"><span data-stu-id="fbc09-208">Personalization</span></span>
2.  <span data-ttu-id="fbc09-209">小工具</span><span class="sxs-lookup"><span data-stu-id="fbc09-209">Gadgets</span></span>
3.  <span data-ttu-id="fbc09-210">顯示</span><span class="sxs-lookup"><span data-stu-id="fbc09-210">Display</span></span>

```
HKEY_CLASSES_ROOT
   DesktopBackground
      Shell = "Personalization,Gadgets"
      Display
```

### <a name="positioning-verbs-at-the-top-or-bottom-of-the-menu"></a><span data-ttu-id="fbc09-211">將動詞放置於功能表頂端或底部</span><span class="sxs-lookup"><span data-stu-id="fbc09-211">Positioning Verbs at the Top or Bottom of the Menu</span></span>

<span data-ttu-id="fbc09-212">下列登錄屬性可以用來將動詞放置在功能表的頂端或底部。</span><span class="sxs-lookup"><span data-stu-id="fbc09-212">The following registry attribute can be used to place a verb at the top or bottom of the menu.</span></span> <span data-ttu-id="fbc09-213">如果有多個動詞指定此屬性，則最後一個會取得優先順序：</span><span class="sxs-lookup"><span data-stu-id="fbc09-213">If there are multiple verbs that specify this attribute then the last one to do so gets priority:</span></span>

``` syntax
Position=Top | Bottom 
```

### <a name="creating-static-cascading-menus"></a><span data-ttu-id="fbc09-214">建立靜態串聯功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-214">Creating Static Cascading Menus</span></span>

<span data-ttu-id="fbc09-215">在 Windows 7 （含）以後版本中，透過登錄設定支援串聯功能表的執行。</span><span class="sxs-lookup"><span data-stu-id="fbc09-215">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="fbc09-216">在 Windows 7 之前，只能透過 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) 介面的執行來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-216">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="fbc09-217">在 Windows 7 （含）以後版本中，您應該只在靜態方法不足時，才需要採用以 COM 程式碼為基礎的解決方案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-217">In Windows 7 and later, you should resort to COM code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="fbc09-218">下列螢幕擷取畫面提供串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="fbc09-218">The following screen shot provides an example of a cascading menu.</span></span>

![顯示級聯功能表範例的螢幕擷取畫面](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="fbc09-220">在 Windows 7 和更新版本中，有三種方式可以建立串聯功能表：</span><span class="sxs-lookup"><span data-stu-id="fbc09-220">In Windows 7 and later, there are three ways to create cascading menus:</span></span>

-   [<span data-ttu-id="fbc09-221">使用子命令登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-221">Creating Cascading Menus with the SubCommands Registry Entry</span></span>](#creating-cascading-menus-with-the-subcommands-registry-entry)
-   [<span data-ttu-id="fbc09-222">使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-222">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](#creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry)
-   [<span data-ttu-id="fbc09-223">使用 IExplorerCommand 介面建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-223">Creating Cascading Menus with the IExplorerCommand Interface</span></span>](#creating-cascading-menus-with-the-iexplorercommand-interface)

### <a name="creating-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="fbc09-224">使用子命令登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-224">Creating Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="fbc09-225">在 Windows 7 （含）以後版本中，您可以使用下列程式，使用子命令專案來建立串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-225">In Windows 7 and later, you can use the SubCommands entry to create cascading menus by using the following procedure.</span></span>

<span data-ttu-id="fbc09-226">**使用子命令專案建立串聯功能表**</span><span class="sxs-lookup"><span data-stu-id="fbc09-226">**To create a cascading menu by using the SubCommands entry**</span></span>

1.  <span data-ttu-id="fbc09-227">在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-227">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="fbc09-228">在此範例中，我們會為此子機碼命名為 *CascadeTest*。</span><span class="sxs-lookup"><span data-stu-id="fbc09-228">In this example, we give this subkey the name *CascadeTest*.</span></span> <span data-ttu-id="fbc09-229">請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。</span><span class="sxs-lookup"><span data-stu-id="fbc09-229">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
    ```

2.  <span data-ttu-id="fbc09-230">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。</span><span class="sxs-lookup"><span data-stu-id="fbc09-230">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="fbc09-231">在此範例中，我們將它指派為「測試 Cascade 功能表」。</span><span class="sxs-lookup"><span data-stu-id="fbc09-231">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu
    ```

3.  <span data-ttu-id="fbc09-232">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的子命令專案，這個專案是由分號所指派的動詞命令（以分號 demlimited），並以外觀順序顯示。</span><span class="sxs-lookup"><span data-stu-id="fbc09-232">To your *CascadeTest* subkey, add a SubCommands entry of type **REG\_SZ** that is assigned list, demlimited by semi-colons, of the verbs that should appear on the menu, in the order of appearance.</span></span> <span data-ttu-id="fbc09-233">例如，我們在這裡指派了許多系統提供的動詞：</span><span class="sxs-lookup"><span data-stu-id="fbc09-233">For example, here we assign a number of system-provided verbs:</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          Shell
             CascadeTest
                SubCommands
                Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
    ```

4.  <span data-ttu-id="fbc09-234">在自訂動詞命令的情況下，請使用任何靜態動詞實方法來加以執行，並在 **CommandStore** 子機碼底下列出它們，如下列虛構動詞 *VerbName* 的範例所示：</span><span class="sxs-lookup"><span data-stu-id="fbc09-234">In the case of custom verbs, implement them using any of the static verb implementation methods and list them under the **CommandStore** subkey as shown in this example for a fictional verb *VerbName*:</span></span>

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
> <span data-ttu-id="fbc09-235">這個方法的優點是，自訂動詞命令可以註冊一次，並藉由列出子命令專案下的動詞名稱重複使用。</span><span class="sxs-lookup"><span data-stu-id="fbc09-235">This method has the advantage that the custom verbs can be registered once and reused by listing the verb name under the SubCommands entry.</span></span> <span data-ttu-id="fbc09-236">但是，應用程式需要有許可權才能修改 **HKEY \_ 本機 \_ 電腦** 下的登錄。</span><span class="sxs-lookup"><span data-stu-id="fbc09-236">However, it requires the application to have permission to modify the registry under **HKEY\_LOCAL\_MACHINE**.</span></span>

 

### <a name="creating-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="fbc09-237">使用 ExtendedSubCommandsKey 登錄專案建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-237">Creating Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="fbc09-238">在 Windows 7 和更新版本中，您可以使用 ExtendedSubCommandKey 專案來建立擴充的串聯功能表：串聯功能表中的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-238">In Windows 7 and later, you can use the ExtendedSubCommandKey entry to create extended cascading menus: cascading menus within cascading menus.</span></span>

<span data-ttu-id="fbc09-239">下列螢幕擷取畫面是延伸串聯功能表的範例。</span><span class="sxs-lookup"><span data-stu-id="fbc09-239">The following screen shot is an example of an extended cascading menu.</span></span>

![顯示裝置的擴充串聯功能表的螢幕擷取畫面](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="fbc09-241">由於 **HKEY \_ 類別 \_ 根目錄** 是 **HKEY \_ 目前 \_ 使用者** 和 **HKEY \_ 本機 \_ 電腦** 的組合，因此您可以在 [ **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別**] 子機碼下註冊任何自訂動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-241">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register any custom verbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="fbc09-242">這麼做的主要優點是不需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="fbc09-242">The main advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="fbc09-243">此外，其他檔案關聯也可以藉由指定相同的 ExtendedSubCommandsKey 子機碼，重複使用這整組動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-243">Also, other file associations can reuse this entire set of verbs by specifying the same ExtendedSubCommandsKey subkey.</span></span> <span data-ttu-id="fbc09-244">如果您不需要重複使用這組動詞，可以列出父系底下的動詞命令，但是確定父系的預設值是空的。</span><span class="sxs-lookup"><span data-stu-id="fbc09-244">If you do not need to reuse this set of verbs, you can list the verbs under the parent, but ensure that the Default value of the parent is empty.</span></span>

<span data-ttu-id="fbc09-245">**使用 ExtendedSubCommandsKey 專案建立串聯功能表**</span><span class="sxs-lookup"><span data-stu-id="fbc09-245">**To create a cascading menu by using an ExtendedSubCommandsKey entry**</span></span>

1.  <span data-ttu-id="fbc09-246">在 **HKEY \_ 類別的 \_ 根目錄** ProgID shell 下建立子機碼 \\  \\  ，以代表您的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-246">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell** to represent your cascading menu.</span></span> <span data-ttu-id="fbc09-247">在此範例中，我們會為此子機碼命名為 *CascadeTest2*。</span><span class="sxs-lookup"><span data-stu-id="fbc09-247">In this example, we give this subkey the name *CascadeTest2*.</span></span> <span data-ttu-id="fbc09-248">請確定 *CascadeTest* 子機碼的預設值是空的，並顯示為 **未) 設定 (值**。</span><span class="sxs-lookup"><span data-stu-id="fbc09-248">Ensure that the default value of the *CascadeTest* subkey is empty, and shown as **(value not set)**.</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest2
                (Default)
    ```

2.  <span data-ttu-id="fbc09-249">在您的 *CascadeTest* 子機碼中，新增類型為 **REG \_ SZ** 的 MUIVerb 專案，並將在快捷方式功能表上顯示為其名稱的文字指派給它。</span><span class="sxs-lookup"><span data-stu-id="fbc09-249">To your *CascadeTest* subkey, add a MUIVerb entry of type **REG\_SZ** and assign it the text that will appear as its name on the shortcut menu.</span></span> <span data-ttu-id="fbc09-250">在此範例中，我們將它指派為「測試 Cascade 功能表」。</span><span class="sxs-lookup"><span data-stu-id="fbc09-250">In this example, we assign it "Test Cascade Menu".</span></span>

    ```
    HKEY_CLASSES_ROOT
       *
          shell
             CascadeTest
                (Default)
                MUIVerb = Test Cascade Menu 2
    ```

3.  <span data-ttu-id="fbc09-251">在您所建立的 *CascadeTest* 子機碼底下，新增 **ExtendedSubCommandsKey** 子機碼，然後將 (**REG \_ SZ** 類型的檔子命令新增) ; 例如：</span><span class="sxs-lookup"><span data-stu-id="fbc09-251">Under the *CascadeTest* subkey you have created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of **REG\_SZ** type); for example:</span></span>

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

    <span data-ttu-id="fbc09-252">確定 [ *測試串聯功能表 2* ] 子機碼的預設值是空的，而且顯示為 [ **未設定) 的 (值**]。</span><span class="sxs-lookup"><span data-stu-id="fbc09-252">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

4.  <span data-ttu-id="fbc09-253">使用下列任何靜態動詞命令來填入 subverbs。</span><span class="sxs-lookup"><span data-stu-id="fbc09-253">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="fbc09-254">請注意，CommandFlags 子機碼代表 EXPCMDFLAGS 值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-254">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="fbc09-255">如果您想要在 cascade 功能表項目之前或之後加入分隔符號，請使用 ECF \_ SEPARATORBEFORE (0x20) 或 ECF \_ SEPARATORAFTER (0x40) 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-255">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="fbc09-256">如需這些 Windows 7 及更新版本旗標的說明，請參閱 [**IExplorerCommand：： GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-256">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="fbc09-257">ECF \_ SEPARATORBEFORE 僅適用于最上層的功能表項目。</span><span class="sxs-lookup"><span data-stu-id="fbc09-257">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="fbc09-258">MUIVerb 的類型為 **reg \_ SZ**，而 CommandFlags 的類型為 **reg \_ DWORD**。</span><span class="sxs-lookup"><span data-stu-id="fbc09-258">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

<span data-ttu-id="fbc09-259">下列螢幕擷取畫面是先前的登錄機碼專案範例的圖例。</span><span class="sxs-lookup"><span data-stu-id="fbc09-259">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![顯示顯示 [記事本] 和 [wordpad] 選項之級聯功能表範例的螢幕擷取畫面](images/file-assoc/testcascademenu2.png)

### <a name="creating-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="fbc09-261">使用 IExplorerCommand 介面建立串聯式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-261">Creating Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="fbc09-262">將動詞新增至串聯功能表的另一個選項是透過 [**IExplorerCommand：： EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-262">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="fbc09-263">這個方法會啟用透過 [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) 提供命令模組命令的資料來源，以使用這些命令做為快捷方式功能表上的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-263">This method enables data sources that provide their command module commands through [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="fbc09-264">在 Windows 7 （含）以後版本中，您可以使用 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 來提供相同的動詞實行，就像使用 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)一樣。</span><span class="sxs-lookup"><span data-stu-id="fbc09-264">In Windows 7 and later, you can provide the same verb implementation using [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) as you can with [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span>

<span data-ttu-id="fbc09-265">以下兩個螢幕擷取畫面說明如何使用 [ **裝置** ] 資料夾中的串聯功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-265">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面。](images/file-assoc/filecascademenu.png)

<span data-ttu-id="fbc09-267">下列螢幕擷取畫面說明 [ **裝置** ] 資料夾中串聯功能表的另一個執行。</span><span class="sxs-lookup"><span data-stu-id="fbc09-267">The following screen shot illustrates another implementation of a cascading menu in the **Devices** folder.</span></span>

![顯示 [裝置] 資料夾中串聯功能表範例的螢幕擷取畫面](images/file-assoc/cascadedevices2.png)

> [!Note]  
> <span data-ttu-id="fbc09-269">因為 [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) 僅支援同進程啟用，所以建議您在需要于命令和快捷方式功能表之間共用執行的 Shell 資料來源使用。</span><span class="sxs-lookup"><span data-stu-id="fbc09-269">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

### <a name="getting-dynamic-behavior-for-static-verbs-by-using-advanced-query-syntax"></a><span data-ttu-id="fbc09-270">使用 Advanced Query 語法取得靜態動詞命令的動態行為</span><span class="sxs-lookup"><span data-stu-id="fbc09-270">Getting Dynamic Behavior for Static Verbs by Using Advanced Query Syntax</span></span>

<span data-ttu-id="fbc09-271">Advanced Query 語法 (AQS) 可以表達要使用為其具現化動詞之專案的屬性進行評估的條件。</span><span class="sxs-lookup"><span data-stu-id="fbc09-271">Advanced Query Syntax (AQS) can express a condition that will be evaluated using properties from the item that the verb is being instantiated for.</span></span> <span data-ttu-id="fbc09-272">這個系統只適用于快速屬性。</span><span class="sxs-lookup"><span data-stu-id="fbc09-272">This system works only with fast properties.</span></span> <span data-ttu-id="fbc09-273">這些是 Shell 資料來源回報的屬性，不會從 [**IShellFolder2：： GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate)傳回 [\* \* \* \* SHCOLSTATE \_ 慢 \*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) \* \* \*。</span><span class="sxs-lookup"><span data-stu-id="fbc09-273">These are properties that the Shell data source reports as fast by not returning [\*\*\*\*SHCOLSTATE\_SLOW\*\*\*\*](/windows/win32/api/shtypes/ne-shtypes-shcolstate) from [**IShellFolder2::GetDefaultColumnState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdefaultcolumnstate).</span></span>

<span data-ttu-id="fbc09-274">Windows 7 和更新版本支援可避免當地語系化組建問題的標準值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-274">Windows 7 and later support canonical values that avoid problems on localized builds.</span></span> <span data-ttu-id="fbc09-275">當地語系化的組建需要下列標準語法，才能利用此 Windows 7 增強功能。</span><span class="sxs-lookup"><span data-stu-id="fbc09-275">The following canonical syntax is required on localized builds to take advantage of this Windows 7 enhancement.</span></span>

``` syntax
System.StructuredQueryType.Boolean#True
```

<span data-ttu-id="fbc09-276">在下列範例登錄專案中：</span><span class="sxs-lookup"><span data-stu-id="fbc09-276">In the following example registry entry:</span></span>

-   <span data-ttu-id="fbc09-277">**AppliesTo** 值會控制是否要顯示或隱藏動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-277">The **AppliesTo** value controls whether the verb is displayed or hidden.</span></span>
-   <span data-ttu-id="fbc09-278">DefaultAppliesTo 值控制預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-278">The DefaultAppliesTo value controls which verb is the default.</span></span>
-   <span data-ttu-id="fbc09-279">HasLUAShield 值會控制是否顯示使用者帳戶控制 (UAC) 盾牌。</span><span class="sxs-lookup"><span data-stu-id="fbc09-279">The HasLUAShield value controls whether a User Account Control (UAC) shield is displayed.</span></span>

<span data-ttu-id="fbc09-280">在此範例中， **DefaultAppliesTo** 值會讓這個動詞成為其檔案名中有 "exampleText1" 這個字的任何檔案的預設值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-280">In this example the **DefaultAppliesTo** value makes this verb the default for any file with the word "exampleText1" in its file name.</span></span> <span data-ttu-id="fbc09-281">**AppliesTo** 值會啟用名稱中有 "exampleText1" 之任何檔案的動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-281">The **AppliesTo** value enables the verb for any file with "exampleText1" in the name.</span></span> <span data-ttu-id="fbc09-282">**HasLUAShield** 值會顯示名稱中有 "exampleText2" 的檔案盾牌。</span><span class="sxs-lookup"><span data-stu-id="fbc09-282">The **HasLUAShield** value displays the shield for files with "exampleText2" in the name.</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            DefaultAppliesTo = System.ItemName:"exampleText1"
            HasLUAShield = System.ItemName:"exampleText2"
            AppliesTo = System.ItemName:"exampleText1"
```

<span data-ttu-id="fbc09-283">新增 **命令** 子機碼和值：</span><span class="sxs-lookup"><span data-stu-id="fbc09-283">Add the **Command** subkey, and a value:</span></span>

```
HKEY_CLASSES_ROOT
   txtile
      shell
         test.verb
            Command
               (Default) = %SystemRoot%\system32\notepad.exe %1
```

<span data-ttu-id="fbc09-284">在 Windows 7 登錄中，請參閱 **HKEY \_ 類別 \_ 根** \\ **磁片磁碟機** 作為使用下列方法的 bitlocker 動詞範例：</span><span class="sxs-lookup"><span data-stu-id="fbc09-284">In the Windows 7 registry, see **HKEY\_CLASSES\_ROOT**\\**drive** as an example of bitlocker verbs that employ the following approach:</span></span>

-   <span data-ttu-id="fbc09-285">AppliesTo = BitlockerProtection： = 2</span><span class="sxs-lookup"><span data-stu-id="fbc09-285">AppliesTo = System.Volume.BitlockerProtection:=2</span></span>
-   <span data-ttu-id="fbc09-286">BitlockerRequiresAdmin： = StructuredQueryType。布林 \# 值 True</span><span class="sxs-lookup"><span data-stu-id="fbc09-286">System.Volume.BitlockerRequiresAdmin:=System.StructuredQueryType.Boolean\#True</span></span>

<span data-ttu-id="fbc09-287">如需 AQS 的詳細資訊，請參閱 [Advanced Query 語法](../search/-search-3x-advancedquerysyntax.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-287">For more information about AQS, see [Advanced Query Syntax](../search/-search-3x-advancedquerysyntax.md).</span></span>

### <a name="deprecated-associating-verbs-with-dynamic-data-exchange-commands"></a><span data-ttu-id="fbc09-288">已淘汰：將動詞與動態資料交換命令建立關聯</span><span class="sxs-lookup"><span data-stu-id="fbc09-288">Deprecated: Associating Verbs with Dynamic Data Exchange Commands</span></span>

<span data-ttu-id="fbc09-289">DDE 已被取代;請改用 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-289">DDE is deprecated; use [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) instead.</span></span> <span data-ttu-id="fbc09-290">DDE 已被取代，因為它依賴廣播視窗訊息來探索 DDE 伺服器。</span><span class="sxs-lookup"><span data-stu-id="fbc09-290">DDE is deprecated because it relies on a broadcast window message to discover the DDE server.</span></span> <span data-ttu-id="fbc09-291">DDE 伺服器會停止回應廣播視窗訊息，因此會讓其他應用程式的 DDE 交談停止回應。</span><span class="sxs-lookup"><span data-stu-id="fbc09-291">A DDE server hang stalls the broadcast window message and thus hangs DDE conversations for other applications.</span></span> <span data-ttu-id="fbc09-292">單一停滯的應用程式通常會在使用者的體驗中造成後續的停止回應。</span><span class="sxs-lookup"><span data-stu-id="fbc09-292">It is common for a single stuck application to cause subsequent hangs all across the user's experience.</span></span>

<span data-ttu-id="fbc09-293">[**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)方法更健全，而且有更好的啟用支援，因為它會使用處理程式的 COM 啟用。</span><span class="sxs-lookup"><span data-stu-id="fbc09-293">The [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) method is more robust and has better activation support because it uses COM activation of the handler.</span></span> <span data-ttu-id="fbc09-294">如果選取多個專案， **IDropTarget** 就不會受限於在 DDE 和 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)中找到的緩衝區大小限制。</span><span class="sxs-lookup"><span data-stu-id="fbc09-294">In the case of multiple item selection, **IDropTarget** is not subject to the buffer size restrictions found in both DDE and the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span> <span data-ttu-id="fbc09-295">此外，專案會以資料物件的形式傳遞至應用程式，您可以使用 [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) 函數來轉換成專案陣列。</span><span class="sxs-lookup"><span data-stu-id="fbc09-295">Also, items are passed to the application as a data object that can be converted to an item array by using the [**SHCreateShellItemArrayFromDataObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject) function.</span></span> <span data-ttu-id="fbc09-296">這麼做會比較簡單，而且不會遺失將專案轉換成命令列或 DDE 通訊協定的路徑時所發生的命名空間資訊。</span><span class="sxs-lookup"><span data-stu-id="fbc09-296">Doing so is simpler, and does not lose namespace information as occurs when the item is converted to a path for command-line or DDE protocols.</span></span>

<span data-ttu-id="fbc09-297">如需檔案關聯屬性之 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 和 Shell 查詢的詳細資訊，請參閱 [認知類型和應用程式註冊](fa-perceivedtypes.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-297">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="completing-verb-implementation-tasks"></a><span data-ttu-id="fbc09-298">完成動詞執行工作</span><span class="sxs-lookup"><span data-stu-id="fbc09-298">Completing Verb Implementation Tasks</span></span>

<span data-ttu-id="fbc09-299">下列用來執行動詞命令的工作，與靜態和動態動詞命令都有關。</span><span class="sxs-lookup"><span data-stu-id="fbc09-299">The following tasks for implementing verbs are relevant to both static and dynamic verb implementations.</span></span> <span data-ttu-id="fbc09-300">如需動態動詞命令的詳細資訊，請參閱 [使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-300">For more information on dynamic verbs, see [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

### <a name="customizing-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="fbc09-301">自訂預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-301">Customizing the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="fbc09-302">許多預先定義的 Shell 物件都具有可自訂的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-302">Many predefined Shell objects have shortcut menus that can be customized.</span></span> <span data-ttu-id="fbc09-303">註冊命令的方式與註冊一般檔案類型的方式非常類似，但請使用預先定義的物件名稱做為檔案類型名稱。</span><span class="sxs-lookup"><span data-stu-id="fbc09-303">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="fbc09-304">預先定義的物件清單位於 [建立 Shell 延伸模組處理常式](handlers.md)的 *預先定義 Shell 物件* 區段中。</span><span class="sxs-lookup"><span data-stu-id="fbc09-304">A list of predefined objects is in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="fbc09-305">這些預先定義的 Shell 物件，其快捷方式功能表可透過在登錄中新增動詞來自訂，並在包含單字動詞的表格中標示。</span><span class="sxs-lookup"><span data-stu-id="fbc09-305">Those predefined Shell objects whose shortcut menus can be customized by adding verbs in the registry are marked in the table with the word Verb.</span></span>

### <a name="extending-a-new-submenu"></a><span data-ttu-id="fbc09-306">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-306">Extending a New Submenu</span></span>

<span data-ttu-id="fbc09-307">當使用者在 Windows 檔案總管中開啟 [檔案 **] 功能表時** ，其中一個顯示的命令是 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="fbc09-307">When a user opens the **File** menu in Windows Explorer, one of the commands displayed is **New**.</span></span> <span data-ttu-id="fbc09-308">選取此命令會顯示子功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-308">Selecting this command displays a submenu.</span></span> <span data-ttu-id="fbc09-309">依預設，子功能表包含兩個命令： **資料夾** 和 **快捷方式**，可讓使用者建立子資料夾和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fbc09-309">By default, the submenu contains two commands, **Folder** and **Shortcut**, that enable users to create subfolders and shortcuts.</span></span> <span data-ttu-id="fbc09-310">您可以擴充此子功能表，以包含任何檔案類型的檔案建立命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-310">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="fbc09-311">若要將檔案建立命令新增至 **新** 的子功能表，您的應用程式檔必須有相關聯的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="fbc09-311">To add a file-creation command to the **New** submenu, your application's files must have an associated file type.</span></span> <span data-ttu-id="fbc09-312">在檔案名下包含 **ShellNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-312">Include a **ShellNew** subkey under the file name.</span></span> <span data-ttu-id="fbc09-313">選取 [檔案 **] 功能表的** [ **新** 命令] 時，Shell 會將檔案類型加入至 **新** 的子功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-313">When the **File** menu's **New** command is selected, the Shell adds the file type to the **New** submenu.</span></span> <span data-ttu-id="fbc09-314">命令的顯示字串是指派給程式 ProgID 的描述性字串。</span><span class="sxs-lookup"><span data-stu-id="fbc09-314">The command's display string is the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="fbc09-315">若要指定檔案建立方法，請將一或多個資料值指派給 **ShellNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-315">To specify the file creation method, assign one or more data values to the **ShellNew** subkey.</span></span> <span data-ttu-id="fbc09-316">下表列出可用的值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-316">The available values are listed in the following table.</span></span>



| <span data-ttu-id="fbc09-317">ShellNew 子機碼值</span><span class="sxs-lookup"><span data-stu-id="fbc09-317">ShellNew subkey value</span></span> | <span data-ttu-id="fbc09-318">Description</span><span class="sxs-lookup"><span data-stu-id="fbc09-318">Description</span></span>                                                                                                                                                              |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbc09-319">命令</span><span class="sxs-lookup"><span data-stu-id="fbc09-319">Command</span></span>               | <span data-ttu-id="fbc09-320">執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="fbc09-320">Executes an application.</span></span> <span data-ttu-id="fbc09-321">這個 **REG \_ SZ** 值會指定要執行之應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="fbc09-321">This **REG\_SZ** value specifies the path of the application to be executed.</span></span> <span data-ttu-id="fbc09-322">例如，您可以將它設定為啟動 wizard。</span><span class="sxs-lookup"><span data-stu-id="fbc09-322">For example, you could set it to launch a wizard.</span></span>                  |
| <span data-ttu-id="fbc09-323">資料</span><span class="sxs-lookup"><span data-stu-id="fbc09-323">Data</span></span>                  | <span data-ttu-id="fbc09-324">建立包含指定資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-324">Creates a file containing specified data.</span></span> <span data-ttu-id="fbc09-325">這個 **REG \_ 二進位** 值會指定檔案的資料。</span><span class="sxs-lookup"><span data-stu-id="fbc09-325">This **REG\_BINARY** value specifies the file's data.</span></span> <span data-ttu-id="fbc09-326">如果指定了 **NullFile** 或 **FileName** ，則會忽略 **資料**。</span><span class="sxs-lookup"><span data-stu-id="fbc09-326">**Data** is ignored if either **NullFile** or **FileName** is specified.</span></span> |
| <span data-ttu-id="fbc09-327">FileName</span><span class="sxs-lookup"><span data-stu-id="fbc09-327">FileName</span></span>              | <span data-ttu-id="fbc09-328">建立檔案，該檔案為指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="fbc09-328">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="fbc09-329">這個 **REG \_ SZ** 值會指定要複製之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="fbc09-329">This **REG\_SZ** value specifies the fully qualified path of the file to be copied.</span></span>                                   |
| <span data-ttu-id="fbc09-330">NullFile</span><span class="sxs-lookup"><span data-stu-id="fbc09-330">NullFile</span></span>              | <span data-ttu-id="fbc09-331">建立空白檔案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-331">Creates an empty file.</span></span> <span data-ttu-id="fbc09-332">**NullFile** 尚未指派值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-332">**NullFile** has no assigned a value.</span></span> <span data-ttu-id="fbc09-333">如果指定 **NullFile** ，則會忽略 **資料** 和 **檔案名** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-333">If **NullFile** is specified, the **Data** and **FileName** registry values are ignored.</span></span>                    |



 

<span data-ttu-id="fbc09-334">下列登錄機碼範例和螢幕擷取畫面說明 myp-ms 檔案類型的 **新** 子功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-334">The following registry key example and screen shot illustrate the **New** submenu for the .myp-ms file type.</span></span> <span data-ttu-id="fbc09-335">它有一個 **Myprogram.exe 應用程式** 命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-335">It has a command, **MyProgram Application**.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
         NullFile
```

<span data-ttu-id="fbc09-336">螢幕擷取畫面說明 **新** 的子功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-336">The screen shot illustrates the **New** submenu.</span></span> <span data-ttu-id="fbc09-337">當使用者從 **新** 的子功能表選取 **myprogram.exe 應用程式** 時，Shell 會建立名為 **New myprogram.exe myp 的** 檔案，並將它傳遞至 **MyProgram.exe**。</span><span class="sxs-lookup"><span data-stu-id="fbc09-337">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named **New MyProgram Application.myp-ms** and passes it to **MyProgram.exe**.</span></span>

![windows explorer 的螢幕擷取畫面，在 [新增] 子功能表上顯示新的 [myprogram.exe 應用程式] 命令](images/context-menu/context-myprogramexe.png)

### <a name="creating-drag-and-drop-handlers"></a><span data-ttu-id="fbc09-339">建立拖放處理常式</span><span class="sxs-lookup"><span data-stu-id="fbc09-339">Creating Drag-and-Drop Handlers</span></span>

<span data-ttu-id="fbc09-340">執行拖放處理常式的基本程式與傳統快捷方式功能表處理常式的基本程式相同。</span><span class="sxs-lookup"><span data-stu-id="fbc09-340">The basic procedure for implementing a drag-and-drop handler is the same as for conventional shortcut menu handlers.</span></span> <span data-ttu-id="fbc09-341">不過，快捷方式功能表處理常式通常只會使用傳遞給處理常式之 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)方法的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)指標，來將物件的名稱解壓縮。</span><span class="sxs-lookup"><span data-stu-id="fbc09-341">However, shortcut menu handlers normally use only the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to the handler's [**IShellExtInit::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method to extract the object's name.</span></span> <span data-ttu-id="fbc09-342">拖放處理常式可以執行更複雜的資料處理程式來修改拖曳物件的行為。</span><span class="sxs-lookup"><span data-stu-id="fbc09-342">A drag-and-drop handler could implement a more sophisticated data handler to modify the behavior of the dragged object.</span></span>

<span data-ttu-id="fbc09-343">當使用者以滑鼠右鍵按一下 Shell 物件來拖曳物件時，會在使用者嘗試卸載物件時顯示快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-343">When a user right-clicks a Shell object to drag an object, a shortcut menu is displayed when the user attempts to drop the object.</span></span> <span data-ttu-id="fbc09-344">下列螢幕擷取畫面說明典型的拖放快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-344">The following screen shot illustrates a typical drag-and-drop shortcut menu.</span></span>

![拖放快捷方式功能表的螢幕擷取畫面](images/context-menu/context-dragdrop.png)

<span data-ttu-id="fbc09-346">拖放處理常式是快捷方式功能表處理常式，可將專案加入這個快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="fbc09-346">A drag-and-drop handler is a shortcut menu handler that can add items to this shortcut menu.</span></span> <span data-ttu-id="fbc09-347">拖放處理常式通常會在下列子機碼下註冊。</span><span class="sxs-lookup"><span data-stu-id="fbc09-347">Drag-and-drop handlers are typically registered under the following subkey.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
```

<span data-ttu-id="fbc09-348">在名為的拖放處理常式的 **DragDropHandlers** 子機碼下新增子機碼，並將子機碼的預設值設定為處理常式之類別識別碼的字串形式 (CLSID) GUID。</span><span class="sxs-lookup"><span data-stu-id="fbc09-348">Add a subkey under the **DragDropHandlers** subkey named for the drag-and-drop handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span> <span data-ttu-id="fbc09-349">下列範例會啟用 **MyDD** 拖放處理常式。</span><span class="sxs-lookup"><span data-stu-id="fbc09-349">The following example enables the **MyDD** drag-and-drop handler.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         DragDropHandlers
            MyDD
               (Default) = {MyDD CLSID GUID}
```

### <a name="suppressing-verbs-and-controlling-visibility"></a><span data-ttu-id="fbc09-350">隱藏動詞和控制可見度</span><span class="sxs-lookup"><span data-stu-id="fbc09-350">Suppressing Verbs and Controlling Visibility</span></span>

<span data-ttu-id="fbc09-351">您可以使用 Windows 原則設定來控制動詞可視性。</span><span class="sxs-lookup"><span data-stu-id="fbc09-351">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="fbc09-352">藉由將 **SuppressionPolicy** 值或 **SuppressionPolicyEx** GUID 值新增至動詞的登錄子機碼，就可以透過原則設定來隱藏動詞命令。</span><span class="sxs-lookup"><span data-stu-id="fbc09-352">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** value, or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="fbc09-353">將 **SuppressionPolicy** 子機碼的值設定為原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="fbc09-353">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="fbc09-354">如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="fbc09-354">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="fbc09-355">如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。</span><span class="sxs-lookup"><span data-stu-id="fbc09-355">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

### <a name="employing-the-verb-selection-model"></a><span data-ttu-id="fbc09-356">採用動詞選取模型</span><span class="sxs-lookup"><span data-stu-id="fbc09-356">Employing the Verb Selection Model</span></span>

<span data-ttu-id="fbc09-357">您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。</span><span class="sxs-lookup"><span data-stu-id="fbc09-357">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="fbc09-358">針對此動詞支援的三種情況，動詞都需要個別的登錄值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-358">A verb requires separate registry values for each of these three situations that the verb supports.</span></span> <span data-ttu-id="fbc09-359">動詞選取模型的可能值如下：</span><span class="sxs-lookup"><span data-stu-id="fbc09-359">The possible values for the verb selection model are as follows:</span></span>

-   <span data-ttu-id="fbc09-360">指定所有動詞的 MultiSelectModel 值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-360">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="fbc09-361">如果未指定 MultiSelectModel 值，則會從您選擇的動詞執行類型推斷。</span><span class="sxs-lookup"><span data-stu-id="fbc09-361">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="fbc09-362">針對以 COM 為基礎的方法 (例如 DropTarget 和 ExecuteCommand) **播放** 程式，並假設為其他方法 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-362">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>
-   <span data-ttu-id="fbc09-363">針對僅支援單一選取專案的動詞指定 **single** 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-363">Specify **Single** for verbs that support only a single selection.</span></span>
-   <span data-ttu-id="fbc09-364">針對支援任意數量專案的動詞指定 **播放** 程式。</span><span class="sxs-lookup"><span data-stu-id="fbc09-364">Specify **Player** for verbs that support any number of items.</span></span>
-   <span data-ttu-id="fbc09-365">針對每個專案建立最上層視窗的動詞命令指定 **檔** 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-365">Specify **Document** for verbs that create a top level window for each item.</span></span> <span data-ttu-id="fbc09-366">這麼做會限制啟用的專案數目，如果使用者開啟太多視窗，則有助於避免系統資源不足。</span><span class="sxs-lookup"><span data-stu-id="fbc09-366">Doing so limits the number of items activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

<span data-ttu-id="fbc09-367">當選取的專案數目不符合動詞選取模型，或大於下表所述的預設限制時，就無法顯示該動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-367">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="fbc09-368">動詞執行的類型</span><span class="sxs-lookup"><span data-stu-id="fbc09-368">Type of verb implementation</span></span> | <span data-ttu-id="fbc09-369">文件</span><span class="sxs-lookup"><span data-stu-id="fbc09-369">Document</span></span> | <span data-ttu-id="fbc09-370">播放器</span><span class="sxs-lookup"><span data-stu-id="fbc09-370">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="fbc09-371">舊版</span><span class="sxs-lookup"><span data-stu-id="fbc09-371">Legacy</span></span>                      | <span data-ttu-id="fbc09-372">15個專案</span><span class="sxs-lookup"><span data-stu-id="fbc09-372">15 items</span></span> | <span data-ttu-id="fbc09-373">100專案</span><span class="sxs-lookup"><span data-stu-id="fbc09-373">100 items</span></span> |
| <span data-ttu-id="fbc09-374">COM</span><span class="sxs-lookup"><span data-stu-id="fbc09-374">COM</span></span>                         | <span data-ttu-id="fbc09-375">15個專案</span><span class="sxs-lookup"><span data-stu-id="fbc09-375">15 items</span></span> | <span data-ttu-id="fbc09-376">沒有限制</span><span class="sxs-lookup"><span data-stu-id="fbc09-376">No limit</span></span>  |



 

<span data-ttu-id="fbc09-377">以下是使用 MultiSelectModel 值的範例登錄專案。</span><span class="sxs-lookup"><span data-stu-id="fbc09-377">The following are example registry entries using the MultiSelectModel value.</span></span>

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

### <a name="using-item-attributes"></a><span data-ttu-id="fbc09-378">使用專案屬性</span><span class="sxs-lookup"><span data-stu-id="fbc09-378">Using Item Attributes</span></span>

<span data-ttu-id="fbc09-379">您可以測試專案之 Shell 屬性的 [**SFGAO**](sfgao.md) 旗標值，以判斷是否應啟用或停用動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-379">The [**SFGAO**](sfgao.md) flag values of the Shell attributes for an item can be tested to determine whether the verb should be enabled or disabled.</span></span>

<span data-ttu-id="fbc09-380">若要使用此屬性功能，請在下列動詞命令底下新增下列 **REG \_ DWORD** 值：</span><span class="sxs-lookup"><span data-stu-id="fbc09-380">To use this attribute feature, add the following the **REG\_DWORD** values under the verb:</span></span>

-   <span data-ttu-id="fbc09-381">AttributeMask 值會指定要測試之遮罩的位值 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-381">The AttributeMask value specifies the [**SFGAO**](sfgao.md) value of the bit values of the mask to test with.</span></span>
-   <span data-ttu-id="fbc09-382">AttributeValue 值會指定所測試之位的 [**SFGAO**](sfgao.md) 值。</span><span class="sxs-lookup"><span data-stu-id="fbc09-382">The AttributeValue value specifies the [**SFGAO**](sfgao.md) value of the bits that are tested.</span></span>
-   <span data-ttu-id="fbc09-383">ImpliedSelectionModel 為專案動詞指定零，或在背景快捷方式功能表上指定非零的動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-383">The ImpliedSelectionModel specifies zero for item verbs, or nonzero for verbs on the background shortcut menu.</span></span>

<span data-ttu-id="fbc09-384">在下列範例登錄專案中，AttributeMask 會設定為 [**SFGAO \_ READONLY**](sfgao.md) (0x40000) 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-384">In the following example registry entry, the AttributeMask is set to [**SFGAO\_READONLY**](sfgao.md) (0x40000).</span></span>

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

### <a name="implementing-custom-verbs-for-folders-through-desktopini"></a><span data-ttu-id="fbc09-385">透過 Desktop.ini 為資料夾執行自訂動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-385">Implementing Custom Verbs for Folders through Desktop.ini</span></span>

<span data-ttu-id="fbc09-386">在 Windows 7 和更新版本中，您可以透過 Desktop.ini 將動詞新增至資料夾。</span><span class="sxs-lookup"><span data-stu-id="fbc09-386">In Windows 7 and later, you can add verbs to a folder through Desktop.ini.</span></span> <span data-ttu-id="fbc09-387">如需 Desktop.ini 檔案的詳細資訊，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。</span><span class="sxs-lookup"><span data-stu-id="fbc09-387">For more information about Desktop.ini files, see [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md).</span></span>

> [!Note]  
> <span data-ttu-id="fbc09-388">Desktop.ini 的檔案應該一律標示為  +  **隱藏** 系統，使其不會顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="fbc09-388">Desktop.ini files should always be marked **System** + **Hidden** so they won't be displayed to users.</span></span>

 

<span data-ttu-id="fbc09-389">**若要透過 Desktop.ini 檔案新增資料夾的自訂動詞命令，請執行下列步驟：**</span><span class="sxs-lookup"><span data-stu-id="fbc09-389">**To add custom verbs for folders through a Desktop.ini file, perform the following steps:**</span></span>

1.  <span data-ttu-id="fbc09-390">建立標示為 **唯讀** 或 **系統** 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="fbc09-390">Create a folder that is marked **Read-only** or **System**.</span></span>
2.  <span data-ttu-id="fbc09-391">建立包含的 Desktop.ini 檔案 \[ 。ShellClassInfo \] DirectoryClass = Folder ProgID。</span><span class="sxs-lookup"><span data-stu-id="fbc09-391">Create a Desktop.ini file that includes a \[.ShellClassInfo\] DirectoryClass=Folder ProgID.</span></span>
3.  <span data-ttu-id="fbc09-392">在登錄中，建立具有值 CanUseForDirectory 的 **HKEY \_ 類別 \_ 根** \\ **資料夾 ProgID** 。</span><span class="sxs-lookup"><span data-stu-id="fbc09-392">In the registry create **HKEY\_CLASSES\_ROOT**\\**Folder ProgID** with a value of CanUseForDirectory.</span></span> <span data-ttu-id="fbc09-393">CanUseForDirectory 值可避免誤用未設定為透過 Desktop.ini 為資料夾執行自訂動詞命令的 Progid。</span><span class="sxs-lookup"><span data-stu-id="fbc09-393">The CanUseForDirectory value avoids the misuse of ProgIDs that are set not to participate in implementing custom verbs for folders through Desktop.ini.</span></span>
4.  <span data-ttu-id="fbc09-394">在 **資料夾** ProgID 子機碼底下新增動詞，例如：</span><span class="sxs-lookup"><span data-stu-id="fbc09-394">Add verbs under the **Folder** ProgID subkey, for example:</span></span>

    ```
    HKEY_CLASSES_ROOT
       CustomFolderType
          Shell
             MyVerb
                command
                   (Default) = %SystemRoot%\system32\notepad.exe %1\desktop.ini
    ```

> [!Note]  
> <span data-ttu-id="fbc09-395">這些動詞命令可以是預設動詞，在此情況下，按兩下資料夾會啟動動詞。</span><span class="sxs-lookup"><span data-stu-id="fbc09-395">These verbs can be the default verb, in which case double-clicking the folder activates the verb.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fbc09-396">相關主題</span><span class="sxs-lookup"><span data-stu-id="fbc09-396">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbc09-397">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="fbc09-397">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="fbc09-398">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="fbc09-398">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="fbc09-399">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="fbc09-399">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="fbc09-400">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="fbc09-400">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="fbc09-401">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="fbc09-401">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> <dt>

[<span data-ttu-id="fbc09-402">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="fbc09-402">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 

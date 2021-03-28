---
description: 以滑鼠右鍵按一下物件，通常會顯示快捷方式功能表。 此功能表包含使用者可選取的命令清單，可在物件上執行各種動作。 本節是檔案系統物件的快捷方式功能表簡介。
ms.assetid: d951d1e8-0f88-49c4-8373-e6db0e18cd72
title: 擴充快速鍵功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895550ff050d559b3523676ddaa2a58099398a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553698"
---
# <a name="extending-shortcut-menus"></a><span data-ttu-id="8dbca-105">擴充快速鍵功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-105">Extending Shortcut Menus</span></span>

<span data-ttu-id="8dbca-106">以滑鼠右鍵按一下物件，通常會顯示 *快捷方式功能表*。</span><span class="sxs-lookup"><span data-stu-id="8dbca-106">Right-clicking an object normally causes the display of a *shortcut menu*.</span></span> <span data-ttu-id="8dbca-107">此功能表包含使用者可選取的命令清單，可在物件上執行各種動作。</span><span class="sxs-lookup"><span data-stu-id="8dbca-107">This menu contains a list of commands that the user can select to perform various actions on the object.</span></span> <span data-ttu-id="8dbca-108">本節是檔案系統物件的快捷方式功能表簡介。</span><span class="sxs-lookup"><span data-stu-id="8dbca-108">This section is an introduction to shortcut menus for file system objects.</span></span>

-   [<span data-ttu-id="8dbca-109">檔案系統物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-109">Shortcut Menus for File System Objects</span></span>](#shortcut-menus-for-file-system-objects)
-   [<span data-ttu-id="8dbca-110">快速鍵功能表動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-110">Shortcut Menu Verbs</span></span>](#shortcut-menu-verbs)
    -   [<span data-ttu-id="8dbca-111">標準動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-111">Canonical Verbs</span></span>](#canonical-verbs)
    -   [<span data-ttu-id="8dbca-112">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-112">Extended Verbs</span></span>](#extended-verbs)
-   [<span data-ttu-id="8dbca-113">擴充檔案類型的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-113">Extending the Shortcut Menu for a File Type</span></span>](#extending-the-shortcut-menu-for-a-file-type)
-   [<span data-ttu-id="8dbca-114">擴充預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-114">Extending the Shortcut Menu for Predefined Shell Objects</span></span>](#extending-the-shortcut-menu-for-predefined-shell-objects)
-   [<span data-ttu-id="8dbca-115">註冊應用程式以處理任意檔案類型</span><span class="sxs-lookup"><span data-stu-id="8dbca-115">Registering an Application to Handle Arbitrary File Types</span></span>](#registering-an-application-to-handle-arbitrary-file-types)
-   [<span data-ttu-id="8dbca-116">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-116">Extending the New Submenu</span></span>](#extending-the-new-submenu)

<span data-ttu-id="8dbca-117">其他資訊可在這裡取得：</span><span class="sxs-lookup"><span data-stu-id="8dbca-117">Additional information is available here:</span></span>

-   [<span data-ttu-id="8dbca-118">如何定義擴充動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-118">How To Define Extended Verbs</span></span>](how-to-define-extended-verbs.md)
-   [<span data-ttu-id="8dbca-119">如何建立動詞與 DDE 命令的關聯</span><span class="sxs-lookup"><span data-stu-id="8dbca-119">How To Associate Verbs with DDE Commands</span></span>](how-to-associate-verbs-with-dde-commands.md)

## <a name="shortcut-menus-for-file-system-objects"></a><span data-ttu-id="8dbca-120">檔案系統物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-120">Shortcut Menus for File System Objects</span></span>

<span data-ttu-id="8dbca-121">當使用者以滑鼠右鍵按一下顯示在 Windows 檔案總管或桌面上的物件（例如檔案）時，會出現快捷方式功能表，其中包含命令清單。</span><span class="sxs-lookup"><span data-stu-id="8dbca-121">When a user right-clicks an object, such as a file, that is displayed in Windows Explorer or on the desktop, a shortcut menu appears with a list of commands.</span></span> <span data-ttu-id="8dbca-122">然後，使用者可以藉由選取適當的命令，在檔案上執行動作，例如開啟或刪除檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-122">The user can then perform an action on the file, such as opening or deleting it, by selecting the appropriate command.</span></span>

<span data-ttu-id="8dbca-123">因為快捷方式功能表通常用於檔案管理，所以 Shell 會提供一組預設的命令，例如剪下和複製，並顯示在任何檔案的快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="8dbca-123">Because shortcut menus are often used for file management, the Shell provides a set of default commands, such as Cut and Copy, that appear on the shortcut menu for any file.</span></span> <span data-ttu-id="8dbca-124">請注意，雖然 [開啟檔案] 是預設的命令，但是不會針對某些標準檔案類型（例如 .wav）顯示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-124">Note that although Open With is a default command, it is not displayed for some standard file types, such as .wav.</span></span> <span data-ttu-id="8dbca-125">下列範例我的檔目錄的圖例，也用來作為 [自訂圖示](icon.md)的範例，會顯示以滑鼠右鍵按一下 MyDocs4.xyz 所顯示的預設快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-125">The following illustration of the sample My Documents directory, which was also used as an example in [Customizing Icons](icon.md), shows a default shortcut menu that was displayed by right-clicking MyDocs4.xyz.</span></span>

![檔案系統物件的預設快捷方式功能表的螢幕擷取畫面](images/context1.jpg)

<span data-ttu-id="8dbca-127">MyDocs4.xyz 顯示預設快捷方式功能表的原因是它不是已註冊 [檔案類型](fa-file-types.md)的成員。</span><span class="sxs-lookup"><span data-stu-id="8dbca-127">The reason that MyDocs4.xyz shows a default shortcut menu is that it is not a member of a registered [file type](fa-file-types.md).</span></span> <span data-ttu-id="8dbca-128">另一方面，.txt 是已註冊的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8dbca-128">On the other hand, .txt is a registered file type.</span></span> <span data-ttu-id="8dbca-129">如果您以滑鼠右鍵按一下其中一個 .txt 檔案，您將會看到一個快捷方式功能表，其中有兩個額外的命令在上方區段中： **開啟** 和 **列印**。</span><span class="sxs-lookup"><span data-stu-id="8dbca-129">If you right-click one of the .txt files, you will instead see a shortcut menu with two additional commands in its upper section: **Open** and **Print**.</span></span>

![檔案系統物件的自訂快捷方式功能表的螢幕擷取畫面](images/context2.jpg)

<span data-ttu-id="8dbca-131">註冊檔案類型之後，您可以使用其他命令來擴充其快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-131">Once a file type is registered, you can extend its shortcut menu with additional commands.</span></span> <span data-ttu-id="8dbca-132">當以滑鼠右鍵按一下該類型的任何檔案時，它們會顯示在預設的命令上方。</span><span class="sxs-lookup"><span data-stu-id="8dbca-132">They are displayed above the default commands when any file of that type is right-clicked.</span></span> <span data-ttu-id="8dbca-133">雖然以這種方式新增的大部分命令都是常見的命令（例如 [ **列印** ] 或 [ **開啟**]），但您可以隨意新增任何使用者可能覺得有用的命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-133">Although most of the commands added in this way are common ones, such as **Print** or **Open**, you are free to add any command that a user might find helpful.</span></span>

<span data-ttu-id="8dbca-134">擴充檔案類型的快捷方式功能表所需的所有專案，都是為每個命令建立一個登錄專案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-134">All that is required to extend the shortcut menu for a file type is to create a registry entry for each command.</span></span> <span data-ttu-id="8dbca-135">更複雜的方法是執行 *快捷方式功能表處理常式*，它可讓您依檔案逐一擴充檔案類型的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-135">A more sophisticated approach is to implement a *shortcut menu handler*, which allows you to extend the shortcut menu for a file type on a file-by-file basis.</span></span> <span data-ttu-id="8dbca-136">如需詳細資訊，請參閱 [建立快顯功能表處理常式](context-menu-handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbca-136">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="shortcut-menu-verbs"></a><span data-ttu-id="8dbca-137">快速鍵功能表動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-137">Shortcut Menu Verbs</span></span>

<span data-ttu-id="8dbca-138">快速鍵功能表上的每個命令都是由其 *動詞* 命令在登錄中識別。</span><span class="sxs-lookup"><span data-stu-id="8dbca-138">Each command on the shortcut menu is identified in the registry by its *verb*.</span></span> <span data-ttu-id="8dbca-139">這些動詞與 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 在以程式設計方式啟動應用程式時所使用的相同。</span><span class="sxs-lookup"><span data-stu-id="8dbca-139">These verbs are the same as those used by [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) when launching applications programmatically.</span></span> <span data-ttu-id="8dbca-140">如需有關使用 **ShellExecuteEx** 的詳細資訊，請參閱 [啟動應用程式](launch.md)的討論。</span><span class="sxs-lookup"><span data-stu-id="8dbca-140">For further information about the use of **ShellExecuteEx**, see the discussion in [Launching Applications](launch.md).</span></span>

<span data-ttu-id="8dbca-141">動詞是簡單的文字字串，可供 Shell 用來識別相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-141">A verb is a simple text string that is used by the Shell to identify the associated command.</span></span> <span data-ttu-id="8dbca-142">每個動詞命令都對應至用來在主控台視窗或 batch ( .bat) 檔中啟動命令的 *命令字串* 。</span><span class="sxs-lookup"><span data-stu-id="8dbca-142">Each verb corresponds to the *command string* used to launch the command in a console window or batch (.bat) file.</span></span> <span data-ttu-id="8dbca-143">例如， **open** 動詞通常會啟動程式來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-143">For example, the **open** verb normally launches a program to open a file.</span></span> <span data-ttu-id="8dbca-144">它的命令字串通常看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="8dbca-144">Its command string typically looks something like this:</span></span>

``` syntax
"My Program.exe" "%1"
```

<span data-ttu-id="8dbca-145">"%1" 是檔案名所提供之命令列參數的標準預留位置。</span><span class="sxs-lookup"><span data-stu-id="8dbca-145">"%1" is the standard placeholder for a command line parameter provided with the filename.</span></span> <span data-ttu-id="8dbca-146">例如，它可以指定要顯示在索引標籤式視圖中的特定頁面。</span><span class="sxs-lookup"><span data-stu-id="8dbca-146">For instance, it can specify a particular page to display in a tabbed view.</span></span>

> [!Note]  
> <span data-ttu-id="8dbca-147">如果命令字串的任何元素包含或可能包含空格，則必須以引號括住。</span><span class="sxs-lookup"><span data-stu-id="8dbca-147">If any element of the command string contains or might contain spaces, it must be enclosed in quotation marks.</span></span> <span data-ttu-id="8dbca-148">否則，如果元素包含空格，將無法正確剖析。</span><span class="sxs-lookup"><span data-stu-id="8dbca-148">Otherwise, if the element contains a space, it will not parse correctly.</span></span> <span data-ttu-id="8dbca-149">比方說，「我的 Program.exe」會正確啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="8dbca-149">For instance, "My Program.exe" will launch the application properly.</span></span> <span data-ttu-id="8dbca-150">如果您使用我的 Program.exe，系統會嘗試以 "Program.exe" 作為第一個命令列引數來啟動 "My"。</span><span class="sxs-lookup"><span data-stu-id="8dbca-150">If you use My Program.exe, the system will attempt to launch "My" with "Program.exe" as its first command line argument.</span></span> <span data-ttu-id="8dbca-151">您應該一律使用引號，其中包含引數（例如 "%1"），並由 Shell 擴充為字串，因為您無法確定字串不會包含空格。</span><span class="sxs-lookup"><span data-stu-id="8dbca-151">You should always use quotation marks with arguments such as "%1" that are expanded to strings by the Shell, because you cannot be certain that the string will not contain a space.</span></span>

 

<span data-ttu-id="8dbca-152">動詞也可以有相關聯的 *顯示字串* ，這會顯示在快捷方式功能表上，而不是動詞字串本身。</span><span class="sxs-lookup"><span data-stu-id="8dbca-152">Verbs can also have a *display string* associated with them, which is displayed on the shortcut menu instead of the verb string itself.</span></span> <span data-ttu-id="8dbca-153">例如， **openas** 的顯示字串會以開啟。</span><span class="sxs-lookup"><span data-stu-id="8dbca-153">For example, the display string for **openas** is Open With.</span></span> <span data-ttu-id="8dbca-154">如同一般的功能表字串，在顯示字串中包含 & 符號 (&) ，可讓您選擇鍵盤的命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-154">Like normal menu strings, including an ampersand (&) in the display string allows keyboard selection of the command.</span></span>

### <a name="canonical-verbs"></a><span data-ttu-id="8dbca-155">標準動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-155">Canonical Verbs</span></span>

<span data-ttu-id="8dbca-156">一般情況下，應用程式會負責為其定義的動詞提供當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-156">In general, applications are responsible for providing localized display strings for the verbs they define.</span></span> <span data-ttu-id="8dbca-157">不過，為了提供某種程度的語言獨立性，系統會定義一組標準的常用動詞，稱為標準 *動詞*。</span><span class="sxs-lookup"><span data-stu-id="8dbca-157">However, to provide a degree of language independence, the system defines a standard set of commonly used verbs called *canonical verbs*.</span></span> <span data-ttu-id="8dbca-158">標準動詞可以搭配任何語言使用，系統會自動產生適當當地語系化的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-158">A canonical verb can be used with any language, and the system automatically generates a properly localized display string.</span></span> <span data-ttu-id="8dbca-159">比方說， **開啟** 動詞的顯示字串將設定為在英文系統上開啟，並且在德文系統上Öffnen。</span><span class="sxs-lookup"><span data-stu-id="8dbca-159">For instance, the **open** verb's display string will be set to Open on an English system, and to Öffnen on a German system.</span></span>

<span data-ttu-id="8dbca-160">標準動詞包括：</span><span class="sxs-lookup"><span data-stu-id="8dbca-160">The canonical verbs include:</span></span>



| <span data-ttu-id="8dbca-161">值</span><span class="sxs-lookup"><span data-stu-id="8dbca-161">Value</span></span>      | <span data-ttu-id="8dbca-162">描述</span><span class="sxs-lookup"><span data-stu-id="8dbca-162">Description</span></span>                                                                                 |
|------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbca-163">開啟</span><span class="sxs-lookup"><span data-stu-id="8dbca-163">open</span></span>       | <span data-ttu-id="8dbca-164">開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="8dbca-164">Opens the file or folder.</span></span>                                                                   |
| <span data-ttu-id="8dbca-165">opennew</span><span class="sxs-lookup"><span data-stu-id="8dbca-165">opennew</span></span>    | <span data-ttu-id="8dbca-166">在新視窗中開啟檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="8dbca-166">Opens the file or folder in a new window.</span></span>                                                   |
| <span data-ttu-id="8dbca-167">print</span><span class="sxs-lookup"><span data-stu-id="8dbca-167">print</span></span>      | <span data-ttu-id="8dbca-168">列印檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-168">Prints the file.</span></span>                                                                            |
| <span data-ttu-id="8dbca-169">探索</span><span class="sxs-lookup"><span data-stu-id="8dbca-169">explore</span></span>    | <span data-ttu-id="8dbca-170">開啟 Windows 檔案總管，並選取資料夾。</span><span class="sxs-lookup"><span data-stu-id="8dbca-170">Opens Windows Explorer with the folder selected.</span></span>                                            |
| <span data-ttu-id="8dbca-171">尋找</span><span class="sxs-lookup"><span data-stu-id="8dbca-171">find</span></span>       | <span data-ttu-id="8dbca-172">開啟 [ **Windows Search** ] 對話方塊，並將資料夾設定為預設搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="8dbca-172">Opens the **Windows Search** dialog box with the folder set as the default search location.</span></span> |
| <span data-ttu-id="8dbca-173">openas</span><span class="sxs-lookup"><span data-stu-id="8dbca-173">openas</span></span>     | <span data-ttu-id="8dbca-174">開啟 [ **開啟方式** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="8dbca-174">Opens the **Open With** dialog box.</span></span>                                                         |
| <span data-ttu-id="8dbca-175">properties</span><span class="sxs-lookup"><span data-stu-id="8dbca-175">properties</span></span> | <span data-ttu-id="8dbca-176">開啟物件的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-176">Opens the object's property sheet.</span></span>                                                          |



 

<span data-ttu-id="8dbca-177">Printto 動詞也是標準的，但永遠不會顯示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-177">The printto verb is also canonical but is never displayed.</span></span> <span data-ttu-id="8dbca-178">它可讓使用者將檔案拖曳至印表機物件來列印該檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-178">It allows the user to print a file by dragging it to a printer object.</span></span>

### <a name="extended-verbs"></a><span data-ttu-id="8dbca-179">擴充的動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-179">Extended Verbs</span></span>

<span data-ttu-id="8dbca-180">當使用者以滑鼠右鍵按一下物件時，快捷方式功能表會包含所有一般動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-180">When the user right-clicks an object, the shortcut menu contains all the normal verbs.</span></span> <span data-ttu-id="8dbca-181">不過，可能會有您想要支援但未顯示在每個快捷方式功能表上的命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-181">However, there could be commands that you want to support but not have displayed on every shortcut menu.</span></span> <span data-ttu-id="8dbca-182">例如，您可能會有不常使用或適用于有經驗的使用者的命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-182">For example, you could have commands that are not commonly used or that are intended for experienced users.</span></span> <span data-ttu-id="8dbca-183">基於這個理由，您也可以定義一或多個 *擴充動詞*。</span><span class="sxs-lookup"><span data-stu-id="8dbca-183">For this reason, you can also define one or more *extended verbs*.</span></span> <span data-ttu-id="8dbca-184">這些動詞也是字元字串，類似于一般動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-184">These verbs are also character strings and are similar to normal verbs.</span></span> <span data-ttu-id="8dbca-185">它們是以其註冊方式與一般動詞的區別。</span><span class="sxs-lookup"><span data-stu-id="8dbca-185">They are distinguished from normal verbs by the way they are registered.</span></span> <span data-ttu-id="8dbca-186">若要存取與擴充動詞相關聯的命令，使用者必須在按下 SHIFT 鍵時，以滑鼠右鍵按一下物件。</span><span class="sxs-lookup"><span data-stu-id="8dbca-186">To have access to the commands associated with extended verbs, the user must right-click an object while pressing the SHIFT key.</span></span> <span data-ttu-id="8dbca-187">擴充的動詞將會連同一般動詞一起顯示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-187">The extended verbs will then be displayed along with the normal verbs.</span></span>

## <a name="extending-the-shortcut-menu-for-a-file-type"></a><span data-ttu-id="8dbca-188">擴充檔案類型的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-188">Extending the Shortcut Menu for a File Type</span></span>

<span data-ttu-id="8dbca-189">擴充檔案類型之快捷方式功能表最簡單的方式就是使用登錄。</span><span class="sxs-lookup"><span data-stu-id="8dbca-189">The simplest way to extend the shortcut menu for a file type is with the registry.</span></span> <span data-ttu-id="8dbca-190">若要這樣做，請在與 [檔案類型](fa-file-types.md)相關聯的應用程式 ProgID 的索引鍵下方新增 **Shell** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="8dbca-190">To do this, add a **Shell** subkey below the key for the ProgID of the application associated with the [file type](fa-file-types.md).</span></span> <span data-ttu-id="8dbca-191">（選擇性）您可以為檔案類型定義 *預設動詞* ，方法是將它設為 **Shell** 子機碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="8dbca-191">Optionally, you can define a *default verb* for the file type by making it the default value of the **Shell** subkey.</span></span>

<span data-ttu-id="8dbca-192">預設動詞會先顯示在快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="8dbca-192">The default verb is displayed first on the shortcut menu.</span></span> <span data-ttu-id="8dbca-193">其目的是在呼叫 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 時，提供 Shell 所能使用的動詞，但未指定任何動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-193">Its purpose is to provide the Shell with a verb it can use when [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) is called but no verb is specified.</span></span> <span data-ttu-id="8dbca-194">以這種方式使用 **ShellExecuteEx** 時，Shell 不一定會選取預設的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-194">The Shell does not necessarily select the default verb when **ShellExecuteEx** is used in this fashion.</span></span> <span data-ttu-id="8dbca-195">針對 Shell [版本 5.0](versions.md) 和更新版本，在 Windows 2000 和更新版本的系統上，shell 會使用下列清單中第一個可用的動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-195">For Shell [versions 5.0](versions.md) and later, found on Windows 2000 and later systems, the Shell uses the first available verb from the following list.</span></span> <span data-ttu-id="8dbca-196">如果沒有可用的，則作業會失敗。</span><span class="sxs-lookup"><span data-stu-id="8dbca-196">If none are available, the operation fails.</span></span>

-   <span data-ttu-id="8dbca-197">Open 動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-197">The open verb</span></span>
-   <span data-ttu-id="8dbca-198">預設動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-198">The default verb</span></span>
-   <span data-ttu-id="8dbca-199">登錄中的第一個動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-199">The first verb in the registry</span></span>
-   <span data-ttu-id="8dbca-200">Openwith 動詞</span><span class="sxs-lookup"><span data-stu-id="8dbca-200">The openwith verb</span></span>

<span data-ttu-id="8dbca-201">若為 [5.0 版](versions.md)之前的 Shell 版本，請省略第三個專案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-201">For Shell versions prior to [version 5.0](versions.md), omit the third item.</span></span>

<span data-ttu-id="8dbca-202">在 **Shell** 子機碼底下，為您要新增的每個動詞建立一個子機碼。</span><span class="sxs-lookup"><span data-stu-id="8dbca-202">Below the **Shell** subkey, create one subkey for each verb you want to add.</span></span> <span data-ttu-id="8dbca-203">這些子機碼的每一個都會將 **REG \_ SZ** 值設定為動詞的顯示字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-203">Each of these subkeys will have a **REG\_SZ** value set to the verb's display string.</span></span> <span data-ttu-id="8dbca-204">您可以省略標準動詞的顯示字串，因為系統會自動顯示適當的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-204">You can omit the display string for canonical verbs because the system will automatically display a properly localized string.</span></span> <span data-ttu-id="8dbca-205">如果您省略 noncanonical 動詞的顯示字串，將會顯示動詞字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-205">If you omit the display string for noncanonical verbs, the verb string will be displayed.</span></span> <span data-ttu-id="8dbca-206">針對每個動詞子機碼，建立 **命令** 子機碼，並將預設值設定為命令字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-206">For each verb subkey, create a **command** subkey with the default value set to the command string.</span></span>

<span data-ttu-id="8dbca-207">下圖顯示在 [檔案類型](fa-file-types.md) 中使用之 myp 檔案類型與 [自訂圖示](icon.md)的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-207">The following illustration shows a shortcut menu for the .myp file type used in [File Types](fa-file-types.md) and [Customizing Icons](icon.md).</span></span> <span data-ttu-id="8dbca-208">它現在會在其快捷方式功能表上提供開啟、doit r、列印和 printto 動詞，並以 doit r 作為預設動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-208">It now has open, doit, print, and printto verbs on its shortcut menu, with doit as the default verb.</span></span> <span data-ttu-id="8dbca-209">快捷方式功能表如下所示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-209">The shortcut menu looks like this.</span></span>

![自訂快捷方式功能表的螢幕擷取畫面](images/context3.jpg)

<span data-ttu-id="8dbca-211">用來擴充上圖所示之快捷方式功能表的登錄專案如下：</span><span class="sxs-lookup"><span data-stu-id="8dbca-211">The registry entries used to extend the shortcut menu shown in the preceding illustration are:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

<span data-ttu-id="8dbca-212">雖然 **Open With** 命令高於第一個分隔符號，但它會由系統自動建立，且不需要登錄專案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-212">Although the **Open With** command is above the first separator, it is automatically created by the system and does not require a registry entry.</span></span> <span data-ttu-id="8dbca-213">系統會自動建立標準動詞開啟和列印的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8dbca-213">The system automatically creates display names for the canonical verbs open and print.</span></span> <span data-ttu-id="8dbca-214">因為 doit r 不是標準的動詞命令，所以會將顯示名稱指派為「&這麼做」，只要按 D 鍵就可以選取它。</span><span class="sxs-lookup"><span data-stu-id="8dbca-214">Because doit is not a canonical verb, it is assigned a display name, "&Do It", which can be selected by pressing the D key.</span></span> <span data-ttu-id="8dbca-215">Printto 動詞命令不會出現在快捷方式功能表上，但包含它可讓使用者藉由將檔案放在印表機圖示上來列印檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-215">The printto verb does not appear on the shortcut menu, but including it allows the user to print files by dropping them on a printer icon.</span></span> <span data-ttu-id="8dbca-216">在此範例中，%1 代表檔案名和 %2 印表機名稱。</span><span class="sxs-lookup"><span data-stu-id="8dbca-216">In this example, %1 represents the file name and %2 the printer name.</span></span>

<span data-ttu-id="8dbca-217">藉由將 SuppressionPolicy 值新增至動詞鍵，即可透過原則設定來隱藏動詞。</span><span class="sxs-lookup"><span data-stu-id="8dbca-217">Verbs can be suppressed through policy settings by adding a SuppressionPolicy value to the verb's key.</span></span> <span data-ttu-id="8dbca-218">將 SuppressionPolicy 的值設定為原則識別碼。</span><span class="sxs-lookup"><span data-stu-id="8dbca-218">Set the value of SuppressionPolicy to the policy ID.</span></span> <span data-ttu-id="8dbca-219">如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="8dbca-219">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="8dbca-220">如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。</span><span class="sxs-lookup"><span data-stu-id="8dbca-220">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

## <a name="extending-the-shortcut-menu-for-predefined-shell-objects"></a><span data-ttu-id="8dbca-221">擴充預先定義之 Shell 物件的快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-221">Extending the Shortcut Menu for Predefined Shell Objects</span></span>

<span data-ttu-id="8dbca-222">許多預先定義的 Shell 物件都有可延伸的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-222">Many predefined Shell objects have shortcut menus that can be extended.</span></span> <span data-ttu-id="8dbca-223">註冊命令的方式與註冊一般檔案類型的方式非常類似，但請使用預先定義的物件名稱做為檔案類型名稱。</span><span class="sxs-lookup"><span data-stu-id="8dbca-223">Register the command in much the same way that you register typical file types, but use the name of the predefined object as the file type name.</span></span>

<span data-ttu-id="8dbca-224">預先定義的物件清單可以在 [建立 Shell 延伸模組處理常式](handlers.md)的 *預先定義 shell 物件* 區段中找到。</span><span class="sxs-lookup"><span data-stu-id="8dbca-224">A list of predefined objects can be found in the *Predefined Shell Objects* section of [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="8dbca-225">這些預先定義的 Shell 物件，其快捷方式功能表可透過在登錄中新增動詞來加以擴充，並以 "Verb" 這個字標示在資料表中。</span><span class="sxs-lookup"><span data-stu-id="8dbca-225">Those predefined Shell objects whose shortcut menus can be extended by adding verbs in the registry are marked in the table with the word "Verb."</span></span>

## <a name="registering-an-application-to-handle-arbitrary-file-types"></a><span data-ttu-id="8dbca-226">註冊應用程式以處理任意檔案類型</span><span class="sxs-lookup"><span data-stu-id="8dbca-226">Registering an Application to Handle Arbitrary File Types</span></span>

<span data-ttu-id="8dbca-227">本檔的前面幾節已經討論過如何定義特定檔案類型的快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="8dbca-227">The preceding sections of this document have discussed how to define shortcut menu items for a particular file type.</span></span> <span data-ttu-id="8dbca-228">此外，定義快捷方式功能表可讓您指定相關聯的應用程式如何開啟檔案類型的成員。</span><span class="sxs-lookup"><span data-stu-id="8dbca-228">Among other things, defining the shortcut menu allows you to specify how the associated application opens a member of the file type.</span></span> <span data-ttu-id="8dbca-229">不過，如 [檔案類型](fa-file-types.md)中所述，當使用者嘗試使用您的應用程式開啟您未與應用程式建立關聯的檔案類型時，應用程式也可以註冊個別的預設程式。</span><span class="sxs-lookup"><span data-stu-id="8dbca-229">However, as discussed in [File Types](fa-file-types.md), applications can also register a separate default procedure to be used when a user attempts to use your application to open a file type that you have not associated with the application.</span></span> <span data-ttu-id="8dbca-230">本主題會在此討論，因為您註冊的預設程式與註冊快捷方式功能表項目的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="8dbca-230">This topic is discussed here because you register the default procedure in much the same way you register shortcut menu items.</span></span>

<span data-ttu-id="8dbca-231">預設程式有兩個基本用途。</span><span class="sxs-lookup"><span data-stu-id="8dbca-231">The default procedure serves two basic purposes.</span></span> <span data-ttu-id="8dbca-232">其中一個方法是指定應該如何叫用應用程式，以開啟任意檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8dbca-232">One is to specify how your application should be invoked to open an arbitrary file type.</span></span> <span data-ttu-id="8dbca-233">比方說，您可以使用命令列旗標來指出正在開啟未知的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8dbca-233">You could, for instance, use a command-line flag to indicate that an unknown file type is being opened.</span></span> <span data-ttu-id="8dbca-234">另一個用途是定義檔案類型的各種特性，例如快捷方式功能表項目和圖示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-234">The other purpose is to define the various characteristics of a file type, such as the shortcut menu items and the icon.</span></span> <span data-ttu-id="8dbca-235">如果使用者將您的應用程式與其他檔案類型產生關聯，則該類型會具有這些特性。</span><span class="sxs-lookup"><span data-stu-id="8dbca-235">If a user associates your application with an additional file type, that type will have these characteristics.</span></span> <span data-ttu-id="8dbca-236">如果其他檔案類型先前與另一個應用程式相關聯，這些特性將會取代原始的。</span><span class="sxs-lookup"><span data-stu-id="8dbca-236">If the additional file type was previously associated with another application, these characteristics will replace the originals.</span></span>

<span data-ttu-id="8dbca-237">若要註冊預設程式，請將您為應用程式 ProgID 建立的登錄機碼放在 **HKEY \_ 類別 \_ 根** 應用程式的應用程式子機碼下 \\ \*\*\*\*。</span><span class="sxs-lookup"><span data-stu-id="8dbca-237">To register the default procedure, place the same registry keys you created for your application's ProgID under the application's subkey of **HKEY\_CLASSES\_ROOT**\\**Applications**.</span></span> <span data-ttu-id="8dbca-238">您也可以包含 FriendlyAppName 值，為系統提供易記的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="8dbca-238">You can also include a FriendlyAppName value to provide the system with a friendly name for your application.</span></span> <span data-ttu-id="8dbca-239">應用程式的易記名稱也可以從它的可執行檔中解壓縮，但只有在 FriendlyAppName 值不存在時。</span><span class="sxs-lookup"><span data-stu-id="8dbca-239">The application's friendly name may also be extracted from its executable file, but only if the FriendlyAppName value is absent.</span></span> <span data-ttu-id="8dbca-240">下列登錄片段顯示 MyProgram.exe 的範例預設程式，可定義易記名稱和數個快捷方式功能表項目。</span><span class="sxs-lookup"><span data-stu-id="8dbca-240">The following registry fragment shows a sample default procedure for MyProgram.exe that defines a friendly name and several shortcut menu items.</span></span> <span data-ttu-id="8dbca-241">命令字串包含/a 旗標，以通知應用程式它正在開啟任意檔案類型。</span><span class="sxs-lookup"><span data-stu-id="8dbca-241">The command strings include the /a flag to notify the application that it is opening an arbitrary file type.</span></span> <span data-ttu-id="8dbca-242">如果您包含 **DefaultIcon** 子機碼，您應該使用一般圖示。</span><span class="sxs-lookup"><span data-stu-id="8dbca-242">If you include a **DefaultIcon** subkey, you should use a generic icon.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         FriendlyAppName = Friendly Name
         shell
            open
               command
                  (Default) = C:\MyDir\MyProgram.exe /a "%1"
            print
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
            printto
               command
                  (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2" %3 %4
```

## <a name="extending-the-new-submenu"></a><span data-ttu-id="8dbca-243">擴充新的子功能表</span><span class="sxs-lookup"><span data-stu-id="8dbca-243">Extending the New Submenu</span></span>

<span data-ttu-id="8dbca-244">當使用者在 Windows 檔案總管中開啟 [檔案 **] 功能表時** ，第一個命令是 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="8dbca-244">When a user opens the **File** menu in Windows Explorer, the first command is **New**.</span></span> <span data-ttu-id="8dbca-245">選取此命令會顯示子功能表。</span><span class="sxs-lookup"><span data-stu-id="8dbca-245">Selecting this command displays a submenu.</span></span> <span data-ttu-id="8dbca-246">依預設，它包含兩個命令、 **資料夾** 和 **快捷方式**，可讓使用者建立子資料夾和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="8dbca-246">By default, it contains two commands, **Folder** and **Shortcut**, that allow users to create subfolders and shortcuts.</span></span> <span data-ttu-id="8dbca-247">您可以擴充此子功能表，以包含任何檔案類型的檔案建立命令。</span><span class="sxs-lookup"><span data-stu-id="8dbca-247">This submenu can be extended to include file creation commands for any file type.</span></span>

<span data-ttu-id="8dbca-248">若要將檔案建立命令新增至 **新** 的子功能表，您的應用程式檔必須有相關聯的 [檔案類型](fa-file-types.md) 。</span><span class="sxs-lookup"><span data-stu-id="8dbca-248">To add a file-creation command to the **New** submenu, your application's files must have a [file type](fa-file-types.md) associated with them.</span></span> <span data-ttu-id="8dbca-249">在副檔名的機碼底下包含 **ShellNew** 子機碼。</span><span class="sxs-lookup"><span data-stu-id="8dbca-249">Include a **ShellNew** subkey under the key for the file name extension.</span></span> <span data-ttu-id="8dbca-250">選取 [檔案] 功能表的 [**新** 命令] 時，Shell 會將它新增至 **新** 的 **子功能表。**</span><span class="sxs-lookup"><span data-stu-id="8dbca-250">When the **File** menu's **New** command is selected, the Shell will add it to the **New** submenu.</span></span> <span data-ttu-id="8dbca-251">命令的顯示字串將會是指派給程式 ProgID 的描述性字串。</span><span class="sxs-lookup"><span data-stu-id="8dbca-251">The command's display string will be the descriptive string that is assigned to the program's ProgID.</span></span>

<span data-ttu-id="8dbca-252">將一或多個資料值指派給 **ShellNew** 子機碼，以指定檔案建立方法。</span><span class="sxs-lookup"><span data-stu-id="8dbca-252">Assign one or more data values to the **ShellNew** subkey to specify the file creation method.</span></span> <span data-ttu-id="8dbca-253">可用的值如下。</span><span class="sxs-lookup"><span data-stu-id="8dbca-253">The available values follow.</span></span>



| <span data-ttu-id="8dbca-254">值</span><span class="sxs-lookup"><span data-stu-id="8dbca-254">Value</span></span>    | <span data-ttu-id="8dbca-255">描述</span><span class="sxs-lookup"><span data-stu-id="8dbca-255">Description</span></span>                                                                                                                                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8dbca-256">命令</span><span class="sxs-lookup"><span data-stu-id="8dbca-256">Command</span></span>  | <span data-ttu-id="8dbca-257">執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="8dbca-257">Executes an application.</span></span> <span data-ttu-id="8dbca-258">這是 **REG \_ SZ** 值，可指定要執行之應用程式的路徑。</span><span class="sxs-lookup"><span data-stu-id="8dbca-258">This is a **REG\_SZ** value specifying the path of the application to be executed.</span></span> <span data-ttu-id="8dbca-259">例如，您可以將它設定為啟動 wizard。</span><span class="sxs-lookup"><span data-stu-id="8dbca-259">For example, you could set it to launch a wizard.</span></span> |
| <span data-ttu-id="8dbca-260">資料</span><span class="sxs-lookup"><span data-stu-id="8dbca-260">Data</span></span>     | <span data-ttu-id="8dbca-261">建立包含指定資料的檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-261">Creates a file containing specified data.</span></span> <span data-ttu-id="8dbca-262">資料是具有檔案資料的 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="8dbca-262">Data is a **REG\_BINARY** value with the file's data.</span></span> <span data-ttu-id="8dbca-263">如果指定了 NullFile 或 FileName，則會忽略資料。</span><span class="sxs-lookup"><span data-stu-id="8dbca-263">Data is ignored if either NullFile or FileName is specified.</span></span>  |
| <span data-ttu-id="8dbca-264">FileName</span><span class="sxs-lookup"><span data-stu-id="8dbca-264">FileName</span></span> | <span data-ttu-id="8dbca-265">建立檔案，該檔案為指定檔案的複本。</span><span class="sxs-lookup"><span data-stu-id="8dbca-265">Creates a file that is a copy of a specified file.</span></span> <span data-ttu-id="8dbca-266">FileName 是 **REG \_ SZ** 值，設定為要複製之檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="8dbca-266">FileName is a **REG\_SZ** value, set to the fully qualified path of the file to be copied.</span></span>                 |
| <span data-ttu-id="8dbca-267">NullFile</span><span class="sxs-lookup"><span data-stu-id="8dbca-267">NullFile</span></span> | <span data-ttu-id="8dbca-268">建立空白檔案。</span><span class="sxs-lookup"><span data-stu-id="8dbca-268">Creates an empty file.</span></span> <span data-ttu-id="8dbca-269">未將值指派給 NullFile。</span><span class="sxs-lookup"><span data-stu-id="8dbca-269">NullFile is not assigned a value.</span></span> <span data-ttu-id="8dbca-270">如果指定 NullFile，則會忽略資料和檔案名的值。</span><span class="sxs-lookup"><span data-stu-id="8dbca-270">If NullFile is specified, the Data and FileName values are ignored.</span></span>                                  |



 

<span data-ttu-id="8dbca-271">下圖顯示在 [檔案類型](fa-file-types.md)中用來做為範例的 myp 檔案類型的 **新** 子功能表，以及 [自訂圖示](icon.md)。</span><span class="sxs-lookup"><span data-stu-id="8dbca-271">The following illustration shows the **New** submenu for the .myp file type used as an example in [File Types](fa-file-types.md) and [Customizing Icons](icon.md).</span></span> <span data-ttu-id="8dbca-272">它現在有一個命令 **Myprogram.exe 應用程式**。</span><span class="sxs-lookup"><span data-stu-id="8dbca-272">It now has a command, **MyProgram Application**.</span></span> <span data-ttu-id="8dbca-273">當使用者從 **新** 的子功能表選取 **myprogram.exe 應用程式** 時，Shell 會建立名為 "New myprogram.exe Application. myp" 的檔案，並將它傳遞給 MyProgram.exe。</span><span class="sxs-lookup"><span data-stu-id="8dbca-273">When a user selects **MyProgram Application** from the **New** submenu, the Shell creates a file named "New MyProgram Application.myp" and passes it to MyProgram.exe.</span></span>

![自訂 [新增] 功能表的螢幕擷取畫面](images/context5.png)

<span data-ttu-id="8dbca-275">登錄專案現在如下所示：</span><span class="sxs-lookup"><span data-stu-id="8dbca-275">The registry entry is now as follows:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
      MyProgram.1
         ShellNew
            NullFile
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = C:\MyDir\MyProgram.exe,2
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
         doit
            (Default) = &Do It
            command
               (Default) = C:\MyDir\MyProgram.exe /d "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /p "%1" "%2" %3 %4
```

 

 




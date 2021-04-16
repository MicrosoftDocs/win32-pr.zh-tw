---
description: 當使用者以滑鼠右鍵按一下 Shell 物件（例如檔案）時，Shell 會顯示快捷方式 (內容) 功能表。
ms.assetid: 4f46b8c3-1e12-447c-87f4-bbe2c305f77a
title: 動詞和檔案關聯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b398b168afe66c3ddd1abe4c78863fbf67ffcbd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550995"
---
# <a name="verbs-and-file-associations"></a><span data-ttu-id="b5412-103">動詞和檔案關聯</span><span class="sxs-lookup"><span data-stu-id="b5412-103">Verbs and File Associations</span></span>

<span data-ttu-id="b5412-104">當使用者以滑鼠右鍵按一下 Shell 物件（例如檔案）時，Shell 會顯示快捷方式 (內容) 功能表。</span><span class="sxs-lookup"><span data-stu-id="b5412-104">When a user right-clicks a Shell object such as a file, the Shell displays a shortcut (context) menu.</span></span> <span data-ttu-id="b5412-105">此功能表包含使用者可以選取的命令清單，以對專案執行各種動作。</span><span class="sxs-lookup"><span data-stu-id="b5412-105">This menu contains a list of commands that the user can select to perform various actions on the item.</span></span> <span data-ttu-id="b5412-106">這些命令也稱為快捷方式功能表項目或動詞。</span><span class="sxs-lookup"><span data-stu-id="b5412-106">These commands are also known as shortcut menu items or verbs.</span></span> <span data-ttu-id="b5412-107">您可以自訂快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b5412-107">Shortcut menus can be customized.</span></span>

<span data-ttu-id="b5412-108">本主題的組織方式如下：</span><span class="sxs-lookup"><span data-stu-id="b5412-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="b5412-109">檔案系統物件的快捷方式功能表簡介</span><span class="sxs-lookup"><span data-stu-id="b5412-109">Introduction to Shortcut Menus for File System Objects</span></span>](#introduction-to-shortcut-menus-for-file-system-objects)
    -   [<span data-ttu-id="b5412-110">將命令新增至快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b5412-110">Add Commands to a Shortcut Menu</span></span>](#add-commands-to-a-shortcut-menu)
-   [<span data-ttu-id="b5412-111">快速鍵功能表動詞</span><span class="sxs-lookup"><span data-stu-id="b5412-111">Shortcut Menu Verbs</span></span>](#shortcut-menu-verbs)
-   [<span data-ttu-id="b5412-112">串流非檔案系統專案和 OpenSearch 結果。</span><span class="sxs-lookup"><span data-stu-id="b5412-112">Stream Non-File System Items and OpenSearch Results.</span></span>](#stream-non-file-system-items-and-opensearch-results)
-   [<span data-ttu-id="b5412-113">註冊應用程式以處理任意檔案類型</span><span class="sxs-lookup"><span data-stu-id="b5412-113">Register an Application to Handle Arbitrary File Types</span></span>](#register-an-application-to-handle-arbitrary-file-types)
-   [<span data-ttu-id="b5412-114">其他資源</span><span class="sxs-lookup"><span data-stu-id="b5412-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="b5412-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5412-115">Related topics</span></span>](#related-topics)

## <a name="introduction-to-shortcut-menus-for-file-system-objects"></a><span data-ttu-id="b5412-116">檔案系統物件的快捷方式功能表簡介</span><span class="sxs-lookup"><span data-stu-id="b5412-116">Introduction to Shortcut Menus for File System Objects</span></span>

<span data-ttu-id="b5412-117">因為快捷方式功能表通常用於檔案管理，所以 Shell 會提供一組預設的命令（例如 **剪** 下和 **複製**），這些命令會出現在任何檔案系統物件（例如檔案或資料夾）的快捷方式功能表上。</span><span class="sxs-lookup"><span data-stu-id="b5412-117">Because shortcut menus are often used for file management, the Shell provides a set of default commands, such as **Cut** and **Copy**, that appear on the shortcut menu for any file system object such as a file or a folder.</span></span>

<span data-ttu-id="b5412-118">下列範例說明以滑鼠右鍵按一下 **MyFile.xyz-ms** 所顯示的預設快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b5412-118">The following example illustrates a default shortcut menu that displayed by right-clicking **MyFile.xyz-ms**.</span></span>

![預設快捷方式功能表的螢幕擷取畫面](images/context-menu/context-filesystemobjects.png)

<span data-ttu-id="b5412-120">預設快捷方式功能表出現 **MyFile.xyz 毫秒** 的原因是因為 **xyz-ms** 不是已註冊檔案類型的成員。</span><span class="sxs-lookup"><span data-stu-id="b5412-120">The reason that a default shortcut menu appears for **MyFile.xyz-ms** is due to the fact that **.xyz-ms** is not a member of a registered file type.</span></span> <span data-ttu-id="b5412-121">相反地， **.txt** 是已註冊的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b5412-121">In contrast, **.txt** is a registered file type.</span></span> <span data-ttu-id="b5412-122">如果您以滑鼠右鍵按一下 **.txt** 檔案，就會在上方區段中看到包含三個額外命令的快捷方式功能表： [ **列印**]、[ **編輯** ] 和 [ **開啟檔案**]。</span><span class="sxs-lookup"><span data-stu-id="b5412-122">If you right-click a **.txt** file, then you see a shortcut menu with three additional commands in its upper section: **Print**, **Edit** and **Open with**.</span></span>

![具有已註冊之檔案類型之檔案的快捷方式功能表的螢幕擷取畫面](images/context-menu/context-registeredfiletype.png)

<span data-ttu-id="b5412-124">若要擴充檔案類型的快捷方式功能表，您必須為每個命令建立一個登錄專案。</span><span class="sxs-lookup"><span data-stu-id="b5412-124">To extend the shortcut menu for a file type, you must create a registry entry for each command.</span></span> <span data-ttu-id="b5412-125">更複雜的方法是執行 (動詞) 處理常式的快捷方式功能表，可讓您以檔案為基礎，擴充檔案類型的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b5412-125">A more sophisticated approach is to implement a shortcut menu (verb) handler, which allows you to extend the shortcut menu for a file type on a file-by-file basis.</span></span> <span data-ttu-id="b5412-126">如需詳細資訊，請參閱 [建立內容功能表處理常式](context-menu-handlers.md)和 [內容功能表參考](context-menu-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b5412-126">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md), and [Context Menu Reference](context-menu-reference.md).</span></span>

### <a name="add-commands-to-a-shortcut-menu"></a><span data-ttu-id="b5412-127">將命令新增至快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b5412-127">Add Commands to a Shortcut Menu</span></span>

<span data-ttu-id="b5412-128">快捷方式功能表處理常式是一種檔案類型處理常式，會將命令新增至現有的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="b5412-128">A shortcut menu handler is a file type handler that adds commands to an existing shortcut menu.</span></span> <span data-ttu-id="b5412-129">快速鍵功能表處理常式會與檔案類型相關聯，並且在每次顯示類別成員的快捷方式功能表時呼叫。</span><span class="sxs-lookup"><span data-stu-id="b5412-129">Shortcut menu handlers are associated with a file type, and are called whenever a shortcut menu is displayed for a member of the class.</span></span> <span data-ttu-id="b5412-130">Shell 會檢查登錄，以查看檔案類型是否與任何快捷方式功能表處理常式相關聯。</span><span class="sxs-lookup"><span data-stu-id="b5412-130">The Shell checks the registry to see if the file type is associated with any shortcut menu handlers.</span></span> <span data-ttu-id="b5412-131">如果是，Shell 會查詢其他快捷方式功能表項目的處理常式。</span><span class="sxs-lookup"><span data-stu-id="b5412-131">If it is, the Shell queries the handlers for additional shortcut menu items.</span></span>

## <a name="shortcut-menu-verbs"></a><span data-ttu-id="b5412-132">快速鍵功能表動詞</span><span class="sxs-lookup"><span data-stu-id="b5412-132">Shortcut Menu Verbs</span></span>

<span data-ttu-id="b5412-133">快速鍵功能表上的每個命令都是由其動詞命令在登錄中識別。</span><span class="sxs-lookup"><span data-stu-id="b5412-133">Each command on the shortcut menu is identified in the registry by its verb.</span></span> <span data-ttu-id="b5412-134">這些動詞與 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 在以程式設計方式啟動應用程式時所使用的相同。</span><span class="sxs-lookup"><span data-stu-id="b5412-134">These verbs are the same as those used by [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) when launching applications programmatically.</span></span>

<span data-ttu-id="b5412-135">動詞是簡單的文字字串，可供 Shell 用來識別相關聯的命令。</span><span class="sxs-lookup"><span data-stu-id="b5412-135">A verb is a simple text string that is used by the Shell to identify the associated command.</span></span> <span data-ttu-id="b5412-136">每個動詞命令都對應至用來在主控台視窗或 batch ( .bat) 檔中啟動命令的命令字串。</span><span class="sxs-lookup"><span data-stu-id="b5412-136">Each verb corresponds to the command string used to launch the command in a console window or batch (.bat) file.</span></span>

<span data-ttu-id="b5412-137">例如，open 動詞通常會啟動程式來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="b5412-137">For example, the open verb normally launches a program to open a file.</span></span> <span data-ttu-id="b5412-138">命令字串通常如下所示：</span><span class="sxs-lookup"><span data-stu-id="b5412-138">The command string typically looks as follows:</span></span>


```
"My Program.exe" "%1"
```



<span data-ttu-id="b5412-139">如果命令字串的任何元素包含或可能包含空格，則必須以引號括住。</span><span class="sxs-lookup"><span data-stu-id="b5412-139">If any element of the command string contains or might contain spaces, it must be enclosed in quotation marks.</span></span> <span data-ttu-id="b5412-140">否則，如果元素包含空格，將無法正確剖析。</span><span class="sxs-lookup"><span data-stu-id="b5412-140">Otherwise, if the element contains a space, it will not parse correctly.</span></span> <span data-ttu-id="b5412-141">比方說，「 **我的 Program.exe** 」會正確啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="b5412-141">For instance, **"My Program.exe"** starts the application properly.</span></span> <span data-ttu-id="b5412-142">如果您使用 **我的 Program.exe** 沒有引號，系統就會嘗試以 **Program.exe** 作為第一個命令列引數來啟動 **my** 。</span><span class="sxs-lookup"><span data-stu-id="b5412-142">If you use **My Program.exe** without quotation marks, then the system attempts to launch **My** with **Program.exe** as its first command line argument.</span></span> <span data-ttu-id="b5412-143">您應該一律使用引號，其中包含引數（例如 **"%1**"），並由 Shell 擴充為字串，因為您無法確定字串不會包含空格。</span><span class="sxs-lookup"><span data-stu-id="b5412-143">You should always use quotation marks with arguments such as **"%1**" that are expanded to strings by the Shell, because you cannot be certain that the string will not contain a space.</span></span>

<span data-ttu-id="b5412-144">動詞也可以有相關聯的顯示名稱，這會顯示在快捷方式功能表上，而不是動詞字串本身。</span><span class="sxs-lookup"><span data-stu-id="b5412-144">Verbs can also have a display name associated with them, which is displayed on the shortcut menu instead of the verb string itself.</span></span> <span data-ttu-id="b5412-145">例如，openas 的顯示字串會 **以開啟**。</span><span class="sxs-lookup"><span data-stu-id="b5412-145">For example, the display string for openas is **Open With**.</span></span> <span data-ttu-id="b5412-146">就像一般的功能表字串一樣，在顯示字串中包含連字號字元，也可以選擇使用鍵盤來選取命令。</span><span class="sxs-lookup"><span data-stu-id="b5412-146">Like normal menu strings, including an ampersand character in the display string allows keyboard selection of the command.</span></span>

## <a name="stream-non-file-system-items-and-opensearch-results"></a><span data-ttu-id="b5412-147">串流非檔案系統專案和 OpenSearch 結果。</span><span class="sxs-lookup"><span data-stu-id="b5412-147">Stream Non-File System Items and OpenSearch Results.</span></span>

<span data-ttu-id="b5412-148">在 Windows 7 （含）以後版本中，支援透過 [ [OpenSearch](http://www.opensearch.org/) ] 通訊協定，將外部來源連接到 Windows 用戶端。</span><span class="sxs-lookup"><span data-stu-id="b5412-148">In Windows 7 and later, there is support of the connection of external sources to the Windows Client via by the [OpenSearch](http://www.opensearch.org/) protocol.</span></span> <span data-ttu-id="b5412-149">這可讓使用者搜尋遠端資料存放區，並從 Windows 檔案總管內查看結果。</span><span class="sxs-lookup"><span data-stu-id="b5412-149">This allows users to search a remote data store and view results from within Windows Explorer.</span></span> <span data-ttu-id="b5412-150">OpenSearch v1.1 標準定義了簡單的檔案格式，可用來描述用戶端應該如何查詢資料存放區的 web 服務，以及服務應該如何傳回結果以供用戶端轉譯。</span><span class="sxs-lookup"><span data-stu-id="b5412-150">The OpenSearch v1.1 standard defines simple file formats that can be used to describe how a client should query the web service for the data store and how the service should return results to be rendered by the client.</span></span>

<span data-ttu-id="b5412-151">您可能需要串流處理非檔案系統專案，以避免在 [OpenSearch](http://www.opensearch.org/) 結果時下載專案。</span><span class="sxs-lookup"><span data-stu-id="b5412-151">You may need to streaming non-file system items to avoid the need to download items in the case of [OpenSearch](http://www.opensearch.org/) results.</span></span> <span data-ttu-id="b5412-152">同盟搜尋功能可讓您從支援 OpenSearch 的非檔案系統位置（例如 SharePoint 和其他 web 服務支援的網站）搜尋專案。</span><span class="sxs-lookup"><span data-stu-id="b5412-152">Federated search feature enables searching items from non-file system locations which support OpenSearch, such as SharePoint and other web services-backed sites, for example.</span></span> <span data-ttu-id="b5412-153">在這些專案上叫用動詞時，系統會下載專案的暫存版本，並將其傳遞至動詞執行。</span><span class="sxs-lookup"><span data-stu-id="b5412-153">When invoking verbs on these items the system downloads a temporary version of the item and passes it to the verb implementation.</span></span> <span data-ttu-id="b5412-154">建議使用動詞實作者，藉由註冊動詞支援的 URL 架構集合來串流專案，以避免下載檔案。</span><span class="sxs-lookup"><span data-stu-id="b5412-154">Verb implementers are encouraged to avoid the need to download the file by registering the set of URL schemas that the verb supports to stream the items.</span></span> <span data-ttu-id="b5412-155">動詞命令是使用 **SupportedProtocols** 登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="b5412-155">Verbs do so by using the **SupportedProtocols** registry key.</span></span>

## <a name="register-an-application-to-handle-arbitrary-file-types"></a><span data-ttu-id="b5412-156">註冊應用程式以處理任意檔案類型</span><span class="sxs-lookup"><span data-stu-id="b5412-156">Register an Application to Handle Arbitrary File Types</span></span>

<span data-ttu-id="b5412-157">定義特定檔案類型的快捷方式功能表項目，可讓您指定相關聯的應用程式如何開啟檔案類型的成員。</span><span class="sxs-lookup"><span data-stu-id="b5412-157">Defining shortcut menu items for a particular file type allows you to specify how the associated application opens a member of the file type.</span></span> <span data-ttu-id="b5412-158">不過，當使用者嘗試使用應用程式開啟與應用程式沒有關聯的檔案類型時，應用程式也可以註冊個別的預設程式。</span><span class="sxs-lookup"><span data-stu-id="b5412-158">However, applications can also register a separate default procedure to be used when a user attempts to use the application to open a file type that is not associated with the application.</span></span> <span data-ttu-id="b5412-159">您註冊預設程式的方式，與註冊快捷方式功能表項目的方式大致相同。</span><span class="sxs-lookup"><span data-stu-id="b5412-159">You register the default procedure in much the same way you register shortcut menu items.</span></span> <span data-ttu-id="b5412-160">如需定義快捷方式功能表項目的詳細資訊，請參閱 [建立內容功能表處理常式](context-menu.md)。</span><span class="sxs-lookup"><span data-stu-id="b5412-160">For more detailed information about defining shortcut menu items, see [Creating Context Menu Handlers](context-menu.md).</span></span>

<span data-ttu-id="b5412-161">預設程式有兩個基本用途。</span><span class="sxs-lookup"><span data-stu-id="b5412-161">The default procedure serves two basic purposes.</span></span> <span data-ttu-id="b5412-162">其中一個方法是指定應該如何叫用應用程式，以開啟任意檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b5412-162">One is to specify how your application should be invoked to open an arbitrary file type.</span></span> <span data-ttu-id="b5412-163">比方說，您可以使用命令列旗標來指出正在開啟未知的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b5412-163">You could, for instance, use a command-line flag to indicate that an unknown file type is being opened.</span></span> <span data-ttu-id="b5412-164">另一個用途是定義檔案類型的各種特性，例如快捷方式功能表項目和圖示。</span><span class="sxs-lookup"><span data-stu-id="b5412-164">The other purpose is to define the various characteristics of a file type, such as the shortcut menu items and the icon.</span></span> <span data-ttu-id="b5412-165">如果使用者將您的應用程式與其他檔案類型產生關聯，該類別將具有這些特性。</span><span class="sxs-lookup"><span data-stu-id="b5412-165">If a user associates your application with an additional file type, that class will have these characteristics.</span></span> <span data-ttu-id="b5412-166">如果其他檔案類型先前與另一個應用程式相關聯，這些特性將會取代原始的。</span><span class="sxs-lookup"><span data-stu-id="b5412-166">If the additional file type was previously associated with another application, these characteristics will replace the originals.</span></span>

<span data-ttu-id="b5412-167">若要註冊預設程式，請將您為應用程式 ProgID 建立的登錄機碼放在 **HKEY \_ 類別 \_ 根 \\ 應用** 程式的應用程式子機碼下。</span><span class="sxs-lookup"><span data-stu-id="b5412-167">To register the default procedure, place the same registry keys you created for your application's ProgID under the application's subkey of **HKEY\_CLASSES\_ROOT\\Applications**.</span></span> <span data-ttu-id="b5412-168">您也可以包含 **FriendlyAppName** 值，為系統提供易記的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="b5412-168">You can also include a **FriendlyAppName** value to provide the system with a friendly name for your application.</span></span> <span data-ttu-id="b5412-169">應用程式的易記名稱也可以從它的可執行檔中解壓縮，但只有在 FriendlyAppName 值不存在時。</span><span class="sxs-lookup"><span data-stu-id="b5412-169">The application's friendly name may also be extracted from its executable file, but only if the FriendlyAppName value is absent.</span></span>

<span data-ttu-id="b5412-170">下列範例登錄專案說明定義易記名稱和數個快捷方式功能表項目的 **MyProgram.exe** 預設程式。</span><span class="sxs-lookup"><span data-stu-id="b5412-170">The following sample registry entry illustrates a default procedure for **MyProgram.exe** that defines a friendly name and several shortcut menu items.</span></span> <span data-ttu-id="b5412-171">命令字串包含 **/a** 旗標，以通知應用程式它正在開啟任意檔案類型。</span><span class="sxs-lookup"><span data-stu-id="b5412-171">The command strings include the **/a** flag to notify the application that it is opening an arbitrary file type.</span></span> <span data-ttu-id="b5412-172">如果您包含 **DefaultIcon** 子機碼，則應該使用一般圖示。</span><span class="sxs-lookup"><span data-stu-id="b5412-172">If you include a **DefaultIcon** subkey, then you should use a generic icon.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.exe
      shell
         open
            command
               (Default) = C:\MyDir\MyProgram.exe /a "%1"
         print
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1"
         printto
            command
               (Default) = C:\MyDir\MyProgram.exe /a /p "%1" "%2"
```

## <a name="additional-resources"></a><span data-ttu-id="b5412-173">其他資源</span><span class="sxs-lookup"><span data-stu-id="b5412-173">Additional Resources</span></span>

-   <span data-ttu-id="b5412-174">如需其他背景，請參閱檔案 [關聯簡介](fa-intro.md)。</span><span class="sxs-lookup"><span data-stu-id="b5412-174">For additional background, see [Introduction to File Associations](fa-intro.md).</span></span>
-   <span data-ttu-id="b5412-175">如需有關使用檔案類型處理常式來擴充 Shell 的概念資訊，請參閱 [建立 Shell 擴充處理常式](handlers.md)。</span><span class="sxs-lookup"><span data-stu-id="b5412-175">For conceptual information about extending the Shell with file type handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5412-176">相關主題</span><span class="sxs-lookup"><span data-stu-id="b5412-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5412-177">快速鍵功能表處理常式和多重選取動詞的最佳作法</span><span class="sxs-lookup"><span data-stu-id="b5412-177">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="b5412-178">為快捷方式功能表選擇靜態或動態動詞</span><span class="sxs-lookup"><span data-stu-id="b5412-178">Choosing a Static or Dynamic Verb for your Shortcut Menu</span></span>](shortcut-choose-method.md)
</dt> <dt>

[<span data-ttu-id="b5412-179">建立快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="b5412-179">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="b5412-180">使用動態動詞自訂快捷方式功能表</span><span class="sxs-lookup"><span data-stu-id="b5412-180">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="b5412-181">快捷方式 (內容) 功能表和快捷方式功能表處理常式</span><span class="sxs-lookup"><span data-stu-id="b5412-181">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="b5412-182">快速鍵功能表參考</span><span class="sxs-lookup"><span data-stu-id="b5412-182">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> </dl>

 

 




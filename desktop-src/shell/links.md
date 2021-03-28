---
description: Shell 連結是資料物件，其中包含用來存取 Shell 命名空間中另一個物件&\# 郵件的資訊，也就是透過 Windows 檔案總管可見的任何物件。
ms.assetid: 32ad306d-54bd-4130-ad30-08db50ef106e
title: Shell 連結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327bcb425f998bcc2a4c0714118d4461ded253ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193354"
---
# <a name="shell-links"></a><span data-ttu-id="ede9a-103">Shell 連結</span><span class="sxs-lookup"><span data-stu-id="ede9a-103">Shell Links</span></span>

<span data-ttu-id="ede9a-104">*Shell 連結* 是資料物件，其中包含用來存取 Shell 命名空間中另一個物件的資訊，也就是透過 Windows 檔案總管可見的任何物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-104">A *Shell link* is a data object that contains information used to access another object in the Shell's namespace—that is, any object visible through Windows Explorer.</span></span> <span data-ttu-id="ede9a-105">可以透過 Shell 連結存取的物件類型包括檔案、資料夾、磁片磁碟機和印表機。</span><span class="sxs-lookup"><span data-stu-id="ede9a-105">The types of objects that can be accessed through Shell links include files, folders, disk drives, and printers.</span></span> <span data-ttu-id="ede9a-106">Shell 連結可讓使用者或應用程式從命名空間中的任何位置存取物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-106">A Shell link allows a user or an application to access an object from anywhere in the namespace.</span></span> <span data-ttu-id="ede9a-107">使用者或應用程式不需要知道物件目前的名稱和位置。</span><span class="sxs-lookup"><span data-stu-id="ede9a-107">The user or application does not need to know the current name and location of the object.</span></span>

-   [<span data-ttu-id="ede9a-108">關於 Shell 連結</span><span class="sxs-lookup"><span data-stu-id="ede9a-108">About Shell Links</span></span>](#about-shell-links)
    -   [<span data-ttu-id="ede9a-109">連結解析</span><span class="sxs-lookup"><span data-stu-id="ede9a-109">Link Resolution</span></span>](#link-resolution)
    -   [<span data-ttu-id="ede9a-110">連結檔案</span><span class="sxs-lookup"><span data-stu-id="ede9a-110">Link Files</span></span>](#link-files)
    -   [<span data-ttu-id="ede9a-111">專案識別碼和識別碼清單</span><span class="sxs-lookup"><span data-stu-id="ede9a-111">Item Identifiers and Identifier Lists</span></span>](#item-identifiers-and-identifier-lists)
-   [<span data-ttu-id="ede9a-112">使用 Shell 連結</span><span class="sxs-lookup"><span data-stu-id="ede9a-112">Using Shell Links</span></span>](#using-shell-links)
    -   [<span data-ttu-id="ede9a-113">建立檔案的快捷方式和資料夾快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-113">Creating a Shortcut and a Folder Shortcut to a File</span></span>](#creating-a-shortcut-and-a-folder-shortcut-to-a-file)
    -   [<span data-ttu-id="ede9a-114">解析快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-114">Resolving a Shortcut</span></span>](#resolving-a-shortcut)
    -   [<span data-ttu-id="ede9a-115">建立非物件的快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-115">Creating a Shortcut to a Nonfile Object</span></span>](#creating-a-shortcut-to-a-nonfile-object)

## <a name="about-shell-links"></a><span data-ttu-id="ede9a-116">關於 Shell 連結</span><span class="sxs-lookup"><span data-stu-id="ede9a-116">About Shell Links</span></span>

<span data-ttu-id="ede9a-117">使用者可從物件的快捷方式功能表選擇 [ **建立快捷方式** ] 命令，以建立 Shell 連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-117">The user creates a Shell link by choosing the **Create Shortcut** command from an object's shortcut menu.</span></span> <span data-ttu-id="ede9a-118">系統會自動建立 Shell 連結的圖示，方法是將物件的圖示與一個小箭號結合 (也就是顯示在圖示左下角的系統定義連結重迭圖示) 。</span><span class="sxs-lookup"><span data-stu-id="ede9a-118">The system automatically creates an icon for the Shell link by combining the object's icon with a small arrow (known as the system-defined link overlay icon) that appears in the lower left corner of the icon.</span></span> <span data-ttu-id="ede9a-119">具有圖示的 Shell 連結稱為快捷方式;不過，詞彙 Shell 連結和快速鍵通常會交替使用。</span><span class="sxs-lookup"><span data-stu-id="ede9a-119">A Shell link that has an icon is called a shortcut; however, the terms Shell link and shortcut are often used interchangeably.</span></span> <span data-ttu-id="ede9a-120">一般而言，使用者會建立快捷方式，以快速存取儲存在子資料夾或其他電腦之共用資料夾中的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-120">Typically, the user creates shortcuts to gain quick access to objects stored in subfolders or in shared folders on other computers.</span></span> <span data-ttu-id="ede9a-121">例如，使用者可以建立子資料夾中的 Microsoft Word 檔的快捷方式，並將快捷方式圖示放置在桌面上。</span><span class="sxs-lookup"><span data-stu-id="ede9a-121">For example, a user can create a shortcut to a Microsoft Word document that is located in a subfolder and place the shortcut icon on the desktop.</span></span> <span data-ttu-id="ede9a-122">然後，使用者就可以按兩下快捷方式圖示來開啟檔。</span><span class="sxs-lookup"><span data-stu-id="ede9a-122">The user can then open the document by double-clicking the shortcut icon.</span></span> <span data-ttu-id="ede9a-123">如果在建立快捷方式之後移動或重新命名檔，系統將會嘗試在使用者下次選取時，更新快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-123">If the document is moved or renamed after the shortcut is created, the system will attempt to update the shortcut the next time the user selects it.</span></span>

<span data-ttu-id="ede9a-124">應用程式也可以建立和使用 Shell 連結和快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-124">Applications can also create and use Shell links and shortcuts.</span></span> <span data-ttu-id="ede9a-125">例如，文字處理應用程式可能會建立 Shell 連結，以執行最近使用的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="ede9a-125">For example, a word processing application might create a Shell link to implement a list of the most recently used documents.</span></span> <span data-ttu-id="ede9a-126">應用程式會使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面來建立 shell 連結化物件，以建立 shell 連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-126">An application creates a Shell link by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to create a Shell link object.</span></span> <span data-ttu-id="ede9a-127">應用程式會使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 或 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面將物件儲存在檔案或資料流程中。</span><span class="sxs-lookup"><span data-stu-id="ede9a-127">The application uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) or [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to store the object in a file or stream.</span></span>

> [!Note]  
> <span data-ttu-id="ede9a-128">您無法使用 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 來建立 URL 的連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-128">You cannot use [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) to create a link to a URL.</span></span>

 

<span data-ttu-id="ede9a-129">本總覽描述 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面，並說明如何使用它從 Microsoft Win32 應用程式內建立和解析 Shell 連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-129">This overview describes the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface and explains how to use it to create and resolve Shell links from within a Microsoft Win32-based application.</span></span> <span data-ttu-id="ede9a-130">由於 Shell 連結的設計是以 OLE 元件物件模型 (COM) 為基礎，因此您應該先熟悉 COM 和 OLE 程式設計的基本概念，再閱讀此總覽。</span><span class="sxs-lookup"><span data-stu-id="ede9a-130">Because the design of Shell links is based on the OLE Component Object Model (COM), you should be familiar with the basic concepts of COM and OLE programming before reading this overview.</span></span>

### <a name="link-resolution"></a><span data-ttu-id="ede9a-131">連結解析</span><span class="sxs-lookup"><span data-stu-id="ede9a-131">Link Resolution</span></span>

<span data-ttu-id="ede9a-132">如果使用者建立物件的快捷方式，並在稍後變更物件的名稱或位置，系統會自動採取步驟來更新或解決在下次使用者選取時的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-132">If a user creates a shortcut to an object and the name or location of the object is later changed, the system automatically takes steps to update, or resolve, the shortcut the next time the user selects it.</span></span> <span data-ttu-id="ede9a-133">但是，如果應用程式建立 Shell 連結並將它儲存在資料流程中，系統就不會自動嘗試解析連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-133">However, if an application creates a Shell link and stores it in a stream, the system does not automatically attempt to resolve the link.</span></span> <span data-ttu-id="ede9a-134">應用程式必須藉由呼叫 [**IShellLink：： resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 方法來解析連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-134">The application must resolve the link by calling the [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) method.</span></span>

<span data-ttu-id="ede9a-135">建立 Shell 連結時，系統會儲存連結的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-135">When a Shell link is created, the system saves information about the link.</span></span> <span data-ttu-id="ede9a-136">解析連結時（自動或透過 [**IShellLink：： Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) 呼叫），系統會先使用 shell 連結之識別碼清單的指標，來抓取與 shell 連結相關聯的路徑。</span><span class="sxs-lookup"><span data-stu-id="ede9a-136">When resolving a link—either automatically or with an [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve) call—the system first retrieves the path associated with the Shell link by using a pointer to the Shell link's identifier list.</span></span> <span data-ttu-id="ede9a-137">如需識別碼清單的詳細資訊，請參閱 [專案識別碼和識別碼清單](#item-identifiers-and-identifier-lists)。</span><span class="sxs-lookup"><span data-stu-id="ede9a-137">For more information about the identifier list, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span> <span data-ttu-id="ede9a-138">系統會在該路徑中搜尋相關聯的物件，如果找到該物件，則會解析該連結。</span><span class="sxs-lookup"><span data-stu-id="ede9a-138">The system searches for the associated object in that path and, if it finds the object, resolves the link.</span></span> <span data-ttu-id="ede9a-139">如果系統找不到物件，它會呼叫 [分散式連結追蹤和物件識別碼](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) 服務（如果有的話），以找出物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-139">If the system cannot find the object, it calls on the [Distributed Link Tracking and Object Identifiers](../fileio/distributed-link-tracking-and-object-identifiers.md) (DLT) service, if available, to locate the object.</span></span> <span data-ttu-id="ede9a-140">如果 DLT 服務無法使用或找不到物件，系統會在相同的目錄中尋找具有相同檔案建立時間和屬性的物件，但名稱不同。</span><span class="sxs-lookup"><span data-stu-id="ede9a-140">If the DLT service is not available or cannot find the object, the system looks in the same directory for an object with the same file creation time and attributes but with a different name.</span></span> <span data-ttu-id="ede9a-141">這種類型的搜尋會將連結解析為已重新命名的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-141">This type of search resolves a link to an object that has been renamed.</span></span>

<span data-ttu-id="ede9a-142">如果系統仍找不到物件，它會搜尋目錄、桌面和本機磁片區，以遞迴方式查看具有相同名稱或建立時間之物件的目錄樹狀結構。</span><span class="sxs-lookup"><span data-stu-id="ede9a-142">If the system still cannot find the object, it searches the directories, the desktop, and local volumes, looking recursively though the directory tree for an object with either the same name or creation time.</span></span> <span data-ttu-id="ede9a-143">如果系統仍找不到相符項，則會顯示一個對話方塊，提示使用者輸入位置。</span><span class="sxs-lookup"><span data-stu-id="ede9a-143">If the system still does not find a match, it displays a dialog box prompting the user for a location.</span></span> <span data-ttu-id="ede9a-144">應用程式可以藉由在 [**IShellLink：： Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve)的呼叫中指定 **SLR \_ NO \_ UI** 值來抑制對話方塊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-144">An application can suppress the dialog box by specifying the **SLR\_NO\_UI** value in a call to [**IShellLink::Resolve**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve).</span></span>

### <a name="initialization-of-the-component-object-library"></a><span data-ttu-id="ede9a-145">元件物件程式庫的初始化</span><span class="sxs-lookup"><span data-stu-id="ede9a-145">Initialization of the Component Object Library</span></span>

<span data-ttu-id="ede9a-146">應用程式必須先藉由呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式來初始化元件物件程式庫，應用程式才能建立及解析快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-146">Before an application can create and resolve shortcuts, it must initialize the component object library by calling the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function.</span></span> <span data-ttu-id="ede9a-147">每次呼叫 **CoInitialize** 都需要對應呼叫 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) 函式，而應用程式會在終止時呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-147">Each call to **CoInitialize** requires a corresponding call to the [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) function, which an application should call when it terminates.</span></span> <span data-ttu-id="ede9a-148">對 **CoUninitialize** 的呼叫可確保應用程式在收到所有擱置中的訊息之前都不會終止。</span><span class="sxs-lookup"><span data-stu-id="ede9a-148">The call to **CoUninitialize** ensures that the application does not terminate until it has received all of its pending messages.</span></span>

### <a name="location-independent-names"></a><span data-ttu-id="ede9a-149">Location-Independent 名稱</span><span class="sxs-lookup"><span data-stu-id="ede9a-149">Location-Independent Names</span></span>

<span data-ttu-id="ede9a-150">系統會為儲存在共用資料夾中的物件，提供與位置無關的 Shell 連結名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9a-150">The system provides location-independent names for Shell links to objects stored in shared folders.</span></span> <span data-ttu-id="ede9a-151">如果物件儲存在本機，系統會提供物件的本機路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="ede9a-151">If the object is stored locally, the system provides the local path and file name for the object.</span></span> <span data-ttu-id="ede9a-152">如果物件儲存在遠端，則系統會為物件提供通用命名慣例 (UNC) 網路資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9a-152">If the object is stored remotely, the system provides a Universal Naming Convention (UNC) network resource name for the object.</span></span> <span data-ttu-id="ede9a-153">由於系統會提供與位置無關的名稱，因此 Shell 連結可以作為檔案的通用名稱，以傳送至其他電腦。</span><span class="sxs-lookup"><span data-stu-id="ede9a-153">Because the system provides location-independent names, a Shell link can serve as a universal name for a file that can be transferred to other computers.</span></span>

### <a name="link-files"></a><span data-ttu-id="ede9a-154">連結檔案</span><span class="sxs-lookup"><span data-stu-id="ede9a-154">Link Files</span></span>

<span data-ttu-id="ede9a-155">當使用者從物件的快捷方式功能表中選擇 [ **建立快捷方式** ] 命令來建立物件的快捷方式時，Windows 會將存取該物件所需的資訊儲存在連結檔案中，此二進位檔案的副檔名為 .lnk。</span><span class="sxs-lookup"><span data-stu-id="ede9a-155">When the user creates a shortcut to an object by choosing the **Create Shortcut** command from the object's shortcut menu, Windows stores the information it needs to access the object in a link file—a binary file that has the .lnk file name extension.</span></span> <span data-ttu-id="ede9a-156">連結檔案包含下列資訊：</span><span class="sxs-lookup"><span data-stu-id="ede9a-156">A link file contains the following information:</span></span>

-   <span data-ttu-id="ede9a-157">快速鍵 (所參考之物件的位置 (路徑) ，稱為對應的物件) 。</span><span class="sxs-lookup"><span data-stu-id="ede9a-157">The location (path) of the object referenced by the shortcut (called the corresponding object).</span></span>
-   <span data-ttu-id="ede9a-158">對應物件的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="ede9a-158">The working directory of the corresponding object.</span></span>
-   <span data-ttu-id="ede9a-159">當快捷方式啟用 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 方法時，系統傳遞給對應物件的引數清單。</span><span class="sxs-lookup"><span data-stu-id="ede9a-159">The list of arguments that the system passes to the corresponding object when the [**IContextMenu::InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) method is activated for the shortcut.</span></span>
-   <span data-ttu-id="ede9a-160">顯示命令，用來設定對應物件的初始顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="ede9a-160">The show command used to set the initial show state of the corresponding object.</span></span> <span data-ttu-id="ede9a-161">這是 \_ [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)中所述的其中一個軟體值。</span><span class="sxs-lookup"><span data-stu-id="ede9a-161">This is one of the SW\_ values described in [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).</span></span>
-   <span data-ttu-id="ede9a-162">快捷方式圖示的位置 (路徑和索引) 。</span><span class="sxs-lookup"><span data-stu-id="ede9a-162">The location (path and index) of the shortcut's icon.</span></span>
-   <span data-ttu-id="ede9a-163">快速鍵的描述字串。</span><span class="sxs-lookup"><span data-stu-id="ede9a-163">The shortcut's description string.</span></span>
-   <span data-ttu-id="ede9a-164">快速鍵的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="ede9a-164">The keyboard shortcut for the shortcut.</span></span>

<span data-ttu-id="ede9a-165">刪除連結檔案時，不會影響對應的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-165">When a link file is deleted, the corresponding object is not affected.</span></span>

<span data-ttu-id="ede9a-166">如果您建立另一個快捷方式的快捷方式，系統只會複製連結檔案，而不是建立新的連結檔案。</span><span class="sxs-lookup"><span data-stu-id="ede9a-166">If you create a shortcut to another shortcut, the system simply copies the link file rather than creating a new link file.</span></span> <span data-ttu-id="ede9a-167">在此情況下，快捷方式將不會彼此獨立。</span><span class="sxs-lookup"><span data-stu-id="ede9a-167">In this case, the shortcuts will not be independent of each other.</span></span>

<span data-ttu-id="ede9a-168">應用程式可以註冊副檔名為快捷方式檔案類型。</span><span class="sxs-lookup"><span data-stu-id="ede9a-168">An application can register a file name extension as a shortcut file type.</span></span> <span data-ttu-id="ede9a-169">如果檔案的副檔名已註冊為快捷方式檔案類型，系統會自動將系統定義的連結重迭圖示 (小箭號) 至檔案的圖示。</span><span class="sxs-lookup"><span data-stu-id="ede9a-169">If a file has a file name extension that has been registered as a shortcut file type, the system automatically adds the system-defined link overlay icon (a small arrow) to the file's icon.</span></span> <span data-ttu-id="ede9a-170">若要將副檔名登錄為快捷方式檔案類型，您必須將 IsShortcut 值新增至副檔名的登錄描述，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="ede9a-170">To register a file name extension as a shortcut file type, you must add the IsShortcut value to the registry description of the file name extension, as shown in the example below.</span></span> <span data-ttu-id="ede9a-171">請注意，必須重新開機 Shell 圖示，重迭圖示才會生效。</span><span class="sxs-lookup"><span data-stu-id="ede9a-171">Note that the Shell must be restarted for the overlay icon to take effect.</span></span> <span data-ttu-id="ede9a-172">IsShortcut 沒有資料值。</span><span class="sxs-lookup"><span data-stu-id="ede9a-172">IsShortcut has no data value.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = XYZApp
   XYZApp
      IsShortcut
```

### <a name="shortcut-names"></a><span data-ttu-id="ede9a-173">快速鍵名稱</span><span class="sxs-lookup"><span data-stu-id="ede9a-173">Shortcut names</span></span>

<span data-ttu-id="ede9a-174">快速鍵的名稱（顯示在 Shell 連結圖示下方的字串）實際上是快捷方式本身的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ede9a-174">The shortcut's name, which is a string that appears below the Shell link icon, is actually the file name of the shortcut itself.</span></span> <span data-ttu-id="ede9a-175">使用者可以藉由選取並輸入新字串來編輯描述字串。</span><span class="sxs-lookup"><span data-stu-id="ede9a-175">The user can edit the description string by selecting it and entering a new string.</span></span>

### <a name="location-of-shortcuts-in-the-namespace"></a><span data-ttu-id="ede9a-176">命名空間中快捷方式的位置</span><span class="sxs-lookup"><span data-stu-id="ede9a-176">Location of shortcuts in the namespace</span></span>

<span data-ttu-id="ede9a-177">快速鍵可以存在於桌面或 Shell 命名空間中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="ede9a-177">A shortcut can exist on the desktop or anywhere in the Shell's namespace.</span></span> <span data-ttu-id="ede9a-178">同樣地，與快捷方式相關聯的物件也可以存在於 Shell 的命名空間中的任何位置。</span><span class="sxs-lookup"><span data-stu-id="ede9a-178">Similarly, the object that is associated with the shortcut can also exist anywhere in the Shell's namespace.</span></span> <span data-ttu-id="ede9a-179">應用程式可以使用 [**IShellLink：： SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) 方法來設定關聯物件的路徑和檔案名，並使用 [**IShellLink：： GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) 方法來取得物件的目前路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="ede9a-179">An application can use the [**IShellLink::SetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath) method to set the path and file name for the associated object, and the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) method to retrieve the current path and file name for the object.</span></span>

### <a name="shortcut-working-directory"></a><span data-ttu-id="ede9a-180">快速鍵工作目錄</span><span class="sxs-lookup"><span data-stu-id="ede9a-180">Shortcut working directory</span></span>

<span data-ttu-id="ede9a-181">工作目錄是在使用者未識別特定目錄時，快速鍵載入或儲存檔案之對應物件的目錄。</span><span class="sxs-lookup"><span data-stu-id="ede9a-181">The working directory is the directory where the corresponding object of a shortcut loads or stores files when the user does not identify a specific directory.</span></span> <span data-ttu-id="ede9a-182">連結檔案包含對應物件之工作目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9a-182">A link file contains the name of the working directory for the corresponding object.</span></span> <span data-ttu-id="ede9a-183">應用程式可以使用 [**IShellLink：： SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) 方法，為對應的物件設定工作目錄的名稱，而且可以使用 [**IShellLink：： GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) 方法來抓取對應物件目前工作目錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="ede9a-183">An application can set the name of the working directory for the corresponding object by using the [**IShellLink::SetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setworkingdirectory) method and can retrieve the name of the current working directory for the corresponding object by using the [**IShellLink::GetWorkingDirectory**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getworkingdirectory) method.</span></span>

### <a name="shortcut-command-line-arguments"></a><span data-ttu-id="ede9a-184">快速鍵命令列引數</span><span class="sxs-lookup"><span data-stu-id="ede9a-184">Shortcut command-line arguments</span></span>

<span data-ttu-id="ede9a-185">連結檔案包含命令列引數，這些引數會在使用者選取連結時，讓 Shell 傳遞給對應的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-185">A link file contains command-line arguments that the Shell passes to the corresponding object when the user selects the link.</span></span> <span data-ttu-id="ede9a-186">應用程式可以使用 [**IShellLink：： SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) 方法來設定快速鍵的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="ede9a-186">An application can set the command-line arguments for a shortcut by using the [**IShellLink::SetArguments**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments) method.</span></span> <span data-ttu-id="ede9a-187">當對應的應用程式（例如，連結器或編譯器）採用特殊旗標做為引數時，設定命令列引數會很有用。</span><span class="sxs-lookup"><span data-stu-id="ede9a-187">It is useful to set command-line arguments when the corresponding application, such as a linker or compiler, takes special flags as arguments.</span></span> <span data-ttu-id="ede9a-188">應用程式可以使用 [**IShellLink：： GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) 方法，從快捷方式取得命令列引數。</span><span class="sxs-lookup"><span data-stu-id="ede9a-188">An application can retrieve the command-line arguments from a shortcut by using the [**IShellLink::GetArguments**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments) method.</span></span>

### <a name="shortcut-show-commands"></a><span data-ttu-id="ede9a-189">快速鍵顯示命令</span><span class="sxs-lookup"><span data-stu-id="ede9a-189">Shortcut show commands</span></span>

<span data-ttu-id="ede9a-190">當使用者按兩下快捷方式時，系統會啟動與對應物件相關聯的應用程式，並根據快捷方式指定的 [顯示] 命令設定應用程式的初始顯示狀態。</span><span class="sxs-lookup"><span data-stu-id="ede9a-190">When the user double-clicks a shortcut, the system starts the application associated with the corresponding object and sets the initial show state of the application based on the show command specified by the shortcut.</span></span> <span data-ttu-id="ede9a-191">Show 命令可以是 \_ [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) 函式描述中包含的任何 SW 值。</span><span class="sxs-lookup"><span data-stu-id="ede9a-191">The show command can be any of the SW\_ values included in the description of the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span> <span data-ttu-id="ede9a-192">應用程式可以使用 [**IShellLink：： SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) 方法來設定快速鍵的 show 命令，而且可以使用 [**IShellLink：： GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) 方法來取出目前的 show 命令。</span><span class="sxs-lookup"><span data-stu-id="ede9a-192">An application can set the show command for a shortcut by using the [**IShellLink::SetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setshowcmd) method and can retrieve the current show command by using the [**IShellLink::GetShowCmd**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getshowcmd) method.</span></span>

### <a name="shortcut-icons"></a><span data-ttu-id="ede9a-193">快速鍵圖示</span><span class="sxs-lookup"><span data-stu-id="ede9a-193">Shortcut icons</span></span>

<span data-ttu-id="ede9a-194">就像其他 Shell 物件一樣，快捷方式也有一個圖示。</span><span class="sxs-lookup"><span data-stu-id="ede9a-194">Like other Shell objects, a shortcut has an icon.</span></span> <span data-ttu-id="ede9a-195">使用者只要按兩下快捷方式的圖示，即可存取與快捷方式相關聯的物件。</span><span class="sxs-lookup"><span data-stu-id="ede9a-195">The user accesses the object associated with a shortcut by double-clicking the shortcut's icon.</span></span> <span data-ttu-id="ede9a-196">當系統建立快捷方式的圖示時，會使用對應物件的點陣圖，並將系統定義的連結重迭圖示 (小箭號) 至左下角。</span><span class="sxs-lookup"><span data-stu-id="ede9a-196">When the system creates an icon for a shortcut, it uses the bitmap of the corresponding object and adds the system-defined link overlay icon (a small arrow) to the lower left corner.</span></span> <span data-ttu-id="ede9a-197">應用程式可以使用 [**IShellLink：： SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) 方法，設定快速鍵的圖示 (路徑和索引) 。</span><span class="sxs-lookup"><span data-stu-id="ede9a-197">An application can set the location (path and index) of a shortcut's icon by using the [**IShellLink::SetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation) method.</span></span> <span data-ttu-id="ede9a-198">應用程式可以使用 [**IShellLink：： GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) 方法來取得這個位置。</span><span class="sxs-lookup"><span data-stu-id="ede9a-198">An application can retrieve this location by using the [**IShellLink::GetIconLocation**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-geticonlocation) method.</span></span>

### <a name="shortcut-descriptions"></a><span data-ttu-id="ede9a-199">快速鍵描述</span><span class="sxs-lookup"><span data-stu-id="ede9a-199">Shortcut descriptions</span></span>

<span data-ttu-id="ede9a-200">快速鍵具有描述，但使用者從未看到它們。</span><span class="sxs-lookup"><span data-stu-id="ede9a-200">Shortcuts have descriptions, but the user never sees them.</span></span> <span data-ttu-id="ede9a-201">應用程式可以使用描述來儲存任何文字資訊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-201">An application can use a description to store any text information.</span></span> <span data-ttu-id="ede9a-202">描述是使用 [**IShellLink：： SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) 方法設定，並使用 [**IShellLink：： GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) 方法來抓取。</span><span class="sxs-lookup"><span data-stu-id="ede9a-202">Descriptions are set using the [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) method and retrieved using the [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) method.</span></span>

### <a name="shortcut-keyboard-shortcuts"></a><span data-ttu-id="ede9a-203">快速鍵鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="ede9a-203">Shortcut Keyboard Shortcuts</span></span>

<span data-ttu-id="ede9a-204">快捷方式物件可以有相關聯的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="ede9a-204">A shortcut object can have a keyboard shortcut associated with it.</span></span> <span data-ttu-id="ede9a-205">鍵盤快速鍵可讓使用者按下按鍵的組合，以啟用快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-205">Keyboard shortcuts allow a user to press a combination of keys to activate a shortcut.</span></span> <span data-ttu-id="ede9a-206">應用程式可以使用 [**IShellLink：： SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) 方法來設定快速鍵的鍵盤快速鍵，而且可以使用 [**IShellLink：： GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) 方法來取得目前的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="ede9a-206">An application can set the keyboard shortcut for a shortcut by using the [**IShellLink::SetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-sethotkey) method and can retrieve the current keyboard shortcut by using the [**IShellLink::GetHotkey**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey) method.</span></span>

### <a name="item-identifiers-and-identifier-lists"></a><span data-ttu-id="ede9a-207">專案識別碼和識別碼清單</span><span class="sxs-lookup"><span data-stu-id="ede9a-207">Item Identifiers and Identifier Lists</span></span>

<span data-ttu-id="ede9a-208">Shell 會使用 Shell 命名空間內的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="ede9a-208">The Shell uses object identifiers within the Shell's namespace.</span></span> <span data-ttu-id="ede9a-209">Shell 中顯示的所有物件 (檔案、目錄、伺服器、工作組等) 在其父資料夾內的物件之間有唯一的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ede9a-209">All objects visible in the Shell (files, directories, servers, workgroups, and so on) have unique identifiers among the objects within their parent folder.</span></span> <span data-ttu-id="ede9a-210">這些識別碼稱為專案識別碼，它們具有 [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) 資料類型，如 shtypes.idl .h 標頭檔中所定義。</span><span class="sxs-lookup"><span data-stu-id="ede9a-210">These identifiers are called item identifiers, and they have the [**SHITEMID**](/windows/desktop/api/Shtypes/ns-shtypes-shitemid) data type as defined in the Shtypes.h header file.</span></span> <span data-ttu-id="ede9a-211">專案識別碼是可變長度的位元組資料流程，包含可識別資料夾內物件的資訊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-211">An item identifier is a variable-length byte stream that contains information that identifies an object within a folder.</span></span> <span data-ttu-id="ede9a-212">只有專案識別碼的建立者知道識別碼的內容和格式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-212">Only the creator of an item identifier knows the content and format of the identifier.</span></span> <span data-ttu-id="ede9a-213">Shell 使用的專案識別碼的唯一部分是前兩個位元組，這兩個位元組會指定識別碼的大小。</span><span class="sxs-lookup"><span data-stu-id="ede9a-213">The only part of an item identifier that the Shell uses is the first two bytes, which specify the size of the identifier.</span></span>

<span data-ttu-id="ede9a-214">每個父資料夾都有自己的專案識別碼，可在它自己的上層資料夾中識別它。</span><span class="sxs-lookup"><span data-stu-id="ede9a-214">Each parent folder has its own item identifier that identifies it within its own parent folder.</span></span> <span data-ttu-id="ede9a-215">因此，任何 Shell 物件都可以透過專案識別碼清單來唯一識別。</span><span class="sxs-lookup"><span data-stu-id="ede9a-215">Thus, any Shell object can be uniquely identified by a list of item identifiers.</span></span> <span data-ttu-id="ede9a-216">父資料夾會保留它所包含之專案的識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="ede9a-216">A parent folder keeps a list of identifiers for the items it contains.</span></span> <span data-ttu-id="ede9a-217">此清單具有 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 資料類型。</span><span class="sxs-lookup"><span data-stu-id="ede9a-217">The list has the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) data type.</span></span> <span data-ttu-id="ede9a-218">專案識別碼清單是由 Shell 配置，並且可以跨 Shell 介面（例如 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)）傳遞。</span><span class="sxs-lookup"><span data-stu-id="ede9a-218">Item identifier lists are allocated by the Shell and may be passed across Shell interfaces, such as [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).</span></span> <span data-ttu-id="ede9a-219">請務必記住，專案識別碼清單中的每個識別碼，只有在其父資料夾的內容中才有意義。</span><span class="sxs-lookup"><span data-stu-id="ede9a-219">It is important to remember that each identifier in an item identifier list is only meaningful within the context of its parent folder.</span></span>

<span data-ttu-id="ede9a-220">應用程式可以使用 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 方法來設定快捷方式的專案識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="ede9a-220">An application can set a shortcut's item identifier list by using the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method.</span></span> <span data-ttu-id="ede9a-221">將快捷方式設定為非檔案的物件（例如印表機或磁片磁碟機）時，此方法很有用。</span><span class="sxs-lookup"><span data-stu-id="ede9a-221">This method is useful when setting a shortcut to an object that is not a file, such as a printer or disk drive.</span></span> <span data-ttu-id="ede9a-222">應用程式可以使用 [**IShellLink：： GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) 方法來取得快捷方式的專案識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="ede9a-222">An application can retrieve a shortcut's item identifier list by using the [**IShellLink::GetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getidlist) method.</span></span>

## <a name="using-shell-links"></a><span data-ttu-id="ede9a-223">使用 Shell 連結</span><span class="sxs-lookup"><span data-stu-id="ede9a-223">Using Shell Links</span></span>

<span data-ttu-id="ede9a-224">本章節包含的範例將示範如何從 Win32 應用程式內建立和解析快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-224">This section contains examples that demonstrate how to create and resolve shortcuts from within a Win32-based application.</span></span> <span data-ttu-id="ede9a-225">本節假設您已熟悉 Win32、c + + 和 OLE COM 程式設計。</span><span class="sxs-lookup"><span data-stu-id="ede9a-225">This section assumes you are familiar with Win32, C++, and OLE COM programming.</span></span>

### <a name="creating-a-shortcut-and-a-folder-shortcut-to-a-file"></a><span data-ttu-id="ede9a-226">建立檔案的快捷方式和資料夾快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-226">Creating a Shortcut and a Folder Shortcut to a File</span></span>

<span data-ttu-id="ede9a-227">下列範例中的 CreateLink 範例函數會建立快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-227">The CreateLink sample function in the following example creates a shortcut.</span></span> <span data-ttu-id="ede9a-228">這些參數包括要連結之檔案的名稱指標、您正在建立的快捷方式名稱指標，以及連結描述的指標。</span><span class="sxs-lookup"><span data-stu-id="ede9a-228">The parameters include a pointer to the name of the file to link to, a pointer to the name of the shortcut that you are creating, and a pointer to the description of the link.</span></span> <span data-ttu-id="ede9a-229">描述包含字串：「 **檔案名** 的快捷方式」，其中 **檔案名** 是要連結的目的檔案名。</span><span class="sxs-lookup"><span data-stu-id="ede9a-229">The description consists of the string, "Shortcut to **file name**," where **file name** is the name of the file to link to.</span></span>

<span data-ttu-id="ede9a-230">若要使用 CreateLink 範例函式建立資料夾快捷方式， [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)請使用 clsid \_ FolderShortcut （而不是 CLSID \_ ShellLink (clsid \_ FolderShortcut 支援 IShellLink) 來呼叫 CoCreateInstance。</span><span class="sxs-lookup"><span data-stu-id="ede9a-230">To create a folder shortcut using the CreateLink sample function, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) using CLSID\_FolderShortcut, instead of CLSID\_ShellLink (CLSID\_FolderShortcut supports IShellLink).</span></span> <span data-ttu-id="ede9a-231">所有其他程式碼都會保持不變。</span><span class="sxs-lookup"><span data-stu-id="ede9a-231">All other code remains the same.</span></span>

<span data-ttu-id="ede9a-232">因為 CreateLink 會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函式，所以會假設已經呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函數。</span><span class="sxs-lookup"><span data-stu-id="ede9a-232">Because CreateLink calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function, it is assumed that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="ede9a-233">CreateLink 會使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面來儲存快捷方式和 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 介面，以儲存檔案名和描述。</span><span class="sxs-lookup"><span data-stu-id="ede9a-233">CreateLink uses the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to save the shortcut and the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface to store the file name and description.</span></span>


```C++
// CreateLink - Uses the Shell's IShellLink and IPersistFile interfaces 
//              to create and store a shortcut to the specified object. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// lpszPathObj  - Address of a buffer that contains the path of the object,
//                including the file name.
// lpszPathLink - Address of a buffer that contains the path where the 
//                Shell link is to be stored, including the file name.
// lpszDesc     - Address of a buffer that contains a description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "winnls.h"
#include "shobjidl.h"
#include "objbase.h"
#include "objidl.h"
#include "shlguid.h"

HRESULT CreateLink(LPCWSTR lpszPathObj, LPCSTR lpszPathLink, LPCWSTR lpszDesc) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
 
    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called.
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Set the path to the shortcut target and add the description. 
        psl->SetPath(lpszPathObj); 
        psl->SetDescription(lpszDesc); 
 
        // Query IShellLink for the IPersistFile interface, used for saving the 
        // shortcut in persistent storage. 
        hres = psl->QueryInterface(IID_IPersistFile, (LPVOID*)&ppf); 
 
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszPathLink, -1, wsz, MAX_PATH); 
            
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Save the link by calling IPersistFile::Save. 
            hres = ppf->Save(wsz, TRUE); 
            ppf->Release(); 
        } 
        psl->Release(); 
    } 
    return hres; 
```



### <a name="resolving-a-shortcut"></a><span data-ttu-id="ede9a-234">解析快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-234">Resolving a Shortcut</span></span>

<span data-ttu-id="ede9a-235">應用程式可能需要存取和操作先前建立的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-235">An application may need to access and manipulate a shortcut that was previously created.</span></span> <span data-ttu-id="ede9a-236">這項操作稱為解析快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-236">This operation is referred to as resolving the shortcut.</span></span>

<span data-ttu-id="ede9a-237">下列範例中的應用程式定義 ResolveIt 函數會解析快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-237">The application-defined ResolveIt function in the following example resolves a shortcut.</span></span> <span data-ttu-id="ede9a-238">其參數包括視窗控制碼、快捷方式路徑的指標，以及接收物件之新路徑的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="ede9a-238">Its parameters include a window handle, a pointer to the path of the shortcut, and the address of a buffer that receives the new path to the object.</span></span> <span data-ttu-id="ede9a-239">視窗控點會識別命令介面可能需要顯示之任何訊息方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="ede9a-239">The window handle identifies the parent window for any message boxes that the Shell may need to display.</span></span> <span data-ttu-id="ede9a-240">例如，如果連結位於非共用媒體上，Shell 可以顯示訊息方塊，如果發生網路問題，使用者是否需要插入磁片，依此類推。</span><span class="sxs-lookup"><span data-stu-id="ede9a-240">For example, the Shell can display a message box if the link is on unshared media, if network problems occur, if the user needs to insert a floppy disk, and so on.</span></span>

<span data-ttu-id="ede9a-241">ResolveIt 函式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，並假設已呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 函式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-241">The ResolveIt function calls the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and assumes that the [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) function has already been called.</span></span> <span data-ttu-id="ede9a-242">請注意，ResolveIt 需要使用 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面來儲存連結資訊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-242">Note that ResolveIt needs to use the [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface to store the link information.</span></span> <span data-ttu-id="ede9a-243">**IPersistFile** 是由 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) 物件所執行。</span><span class="sxs-lookup"><span data-stu-id="ede9a-243">**IPersistFile** is implemented by the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) object.</span></span> <span data-ttu-id="ede9a-244">在抓取路徑資訊之前，必須先載入連結資訊，此範例稍後會顯示此資訊。</span><span class="sxs-lookup"><span data-stu-id="ede9a-244">The link information must be loaded before the path information is retrieved, which is shown later in the example.</span></span> <span data-ttu-id="ede9a-245">無法載入連結資訊會導致呼叫 [**IShellLink：： GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) 和 [**IShellLink：： GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) 成員函式失敗。</span><span class="sxs-lookup"><span data-stu-id="ede9a-245">Failing to load the link information causes the calls to the [**IShellLink::GetPath**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getpath) and [**IShellLink::GetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getdescription) member functions to fail.</span></span>


```C++
// ResolveIt - Uses the Shell's IShellLink and IPersistFile interfaces 
//             to retrieve the path and description from an existing shortcut. 
//
// Returns the result of calling the member functions of the interfaces. 
//
// Parameters:
// hwnd         - A handle to the parent window. The Shell uses this window to 
//                display a dialog box if it needs to prompt the user for more 
//                information while resolving the link.
// lpszLinkFile - Address of a buffer that contains the path of the link,
//                including the file name.
// lpszPath     - Address of a buffer that receives the path of the link
                  target, including the file name.
// lpszDesc     - Address of a buffer that receives the description of the 
//                Shell link, stored in the Comment field of the link
//                properties.

#include "stdafx.h"
#include "windows.h"
#include "shobjidl.h"
#include "shlguid.h"
#include "strsafe.h"
                            
HRESULT ResolveIt(HWND hwnd, LPCSTR lpszLinkFile, LPWSTR lpszPath, int iPathBufferSize) 
{ 
    HRESULT hres; 
    IShellLink* psl; 
    WCHAR szGotPath[MAX_PATH]; 
    WCHAR szDescription[MAX_PATH]; 
    WIN32_FIND_DATA wfd; 
 
    *lpszPath = 0; // Assume failure 

    // Get a pointer to the IShellLink interface. It is assumed that CoInitialize
    // has already been called. 
    hres = CoCreateInstance(CLSID_ShellLink, NULL, CLSCTX_INPROC_SERVER, IID_IShellLink, (LPVOID*)&psl); 
    if (SUCCEEDED(hres)) 
    { 
        IPersistFile* ppf; 
 
        // Get a pointer to the IPersistFile interface. 
        hres = psl->QueryInterface(IID_IPersistFile, (void**)&ppf); 
        
        if (SUCCEEDED(hres)) 
        { 
            WCHAR wsz[MAX_PATH]; 
 
            // Ensure that the string is Unicode. 
            MultiByteToWideChar(CP_ACP, 0, lpszLinkFile, -1, wsz, MAX_PATH); 
 
            // Add code here to check return value from MultiByteWideChar 
            // for success.
 
            // Load the shortcut. 
            hres = ppf->Load(wsz, STGM_READ); 
            
            if (SUCCEEDED(hres)) 
            { 
                // Resolve the link. 
                hres = psl->Resolve(hwnd, 0); 

                if (SUCCEEDED(hres)) 
                { 
                    // Get the path to the link target. 
                    hres = psl->GetPath(szGotPath, MAX_PATH, (WIN32_FIND_DATA*)&wfd, SLGP_SHORTPATH); 

                    if (SUCCEEDED(hres)) 
                    { 
                        // Get the description of the target. 
                        hres = psl->GetDescription(szDescription, MAX_PATH); 

                        if (SUCCEEDED(hres)) 
                        {
                            hres = StringCbCopy(lpszPath, iPathBufferSize, szGotPath);
                            if (SUCCEEDED(hres))
                            {
                                // Handle success
                            }
                            else
                            {
                                // Handle the error
                            }
                        }
                    }
                } 
            } 

            // Release the pointer to the IPersistFile interface. 
            ppf->Release(); 
        } 

        // Release the pointer to the IShellLink interface. 
        psl->Release(); 
    } 
    return hres; 
}
```



### <a name="creating-a-shortcut-to-a-nonfile-object"></a><span data-ttu-id="ede9a-246">建立非物件的快捷方式</span><span class="sxs-lookup"><span data-stu-id="ede9a-246">Creating a Shortcut to a Nonfile Object</span></span>

<span data-ttu-id="ede9a-247">建立非檔案系統的快捷方式（例如印表機）類似于建立檔案的快捷方式，但您必須將識別碼清單設定為印表機，而不是設定檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ede9a-247">Creating a shortcut to a nonfile object, such as a printer, is similar to creating a shortcut to a file except that rather than setting the path to the file, you must set the identifier list to the printer.</span></span> <span data-ttu-id="ede9a-248">若要設定識別碼清單，請呼叫 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 方法，並指定識別碼清單的位址。</span><span class="sxs-lookup"><span data-stu-id="ede9a-248">To set the identifier list, call the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) method, specifying the address of an identifier list.</span></span>

<span data-ttu-id="ede9a-249">Shell 命名空間中的每個物件都有一個專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="ede9a-249">Each object within the Shell's namespace has an item identifier.</span></span> <span data-ttu-id="ede9a-250">Shell 通常會將專案識別碼串連成以 null 終止的清單，其中包含任意數目的專案識別碼。</span><span class="sxs-lookup"><span data-stu-id="ede9a-250">The Shell often concatenates item identifiers into null-terminated lists consisting of any number of item identifiers.</span></span> <span data-ttu-id="ede9a-251">如需專案識別碼的詳細資訊，請參閱 [專案識別碼和識別碼清單](#item-identifiers-and-identifier-lists)。</span><span class="sxs-lookup"><span data-stu-id="ede9a-251">For more information about item identifiers, see [Item Identifiers and Identifier Lists](#item-identifiers-and-identifier-lists).</span></span>

<span data-ttu-id="ede9a-252">一般情況下，如果您需要設定沒有檔案名的專案快捷方式（例如印表機），則您已經有物件的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="ede9a-252">In general, if you need to set a shortcut to an item that does not have a file name, such as a printer, you will already have a pointer to the object's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface.</span></span> <span data-ttu-id="ede9a-253">**IShellFolder** 可用來建立命名空間延伸模組。</span><span class="sxs-lookup"><span data-stu-id="ede9a-253">**IShellFolder** is used to create namespace extensions.</span></span>

<span data-ttu-id="ede9a-254">當您擁有 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)的類別識別碼之後，就可以呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數來取出介面的位址。</span><span class="sxs-lookup"><span data-stu-id="ede9a-254">Once you have the class identifier for [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), you can call the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve the address of the interface.</span></span> <span data-ttu-id="ede9a-255">然後您可以呼叫介面，以列舉資料夾中的物件，並抓取您要搜尋之物件的專案識別碼位址。</span><span class="sxs-lookup"><span data-stu-id="ede9a-255">Then you can call the interface to enumerate the objects in the folder and retrieve the address of the item identifier for the object that you are searching for.</span></span> <span data-ttu-id="ede9a-256">最後，您可以在 [**IShellLink：： SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) 成員函式的呼叫中使用該位址，以建立物件的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="ede9a-256">Finally, you can use the address in a call to the [**IShellLink::SetIDList**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist) member function to create a shortcut to the object.</span></span>

 

 

---
description: 一旦您的應用程式找到檔案物件之後，下一個步驟通常會以某種方式採取行動。
ms.assetid: d774c3b2-4caf-460a-ac32-0ed603491d5f
title: '啟動應用程式 (ShellExecute、ShellExecuteEx、SHELLEXECUTEINFO) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ae5640acdbf4d959b97607cc66a4fd8fe8ac24
ms.sourcegitcommit: 89aa14b1f685f8d65d56ecbdb8bef12246c33cf9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/08/2021
ms.locfileid: "113508609"
---
# <a name="launching-applications-shellexecute-shellexecuteex-shellexecuteinfo"></a><span data-ttu-id="d7f87-103">啟動應用程式 (ShellExecute、ShellExecuteEx、SHELLEXECUTEINFO) </span><span class="sxs-lookup"><span data-stu-id="d7f87-103">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</span></span>

<span data-ttu-id="d7f87-104">一旦您的應用程式找到檔案物件之後，下一個步驟通常會以某種方式採取行動。</span><span class="sxs-lookup"><span data-stu-id="d7f87-104">Once your application has located a file object, the next step is often to act on it in some way.</span></span> <span data-ttu-id="d7f87-105">比方說，您的應用程式可能想要啟動另一個應用程式，讓使用者修改資料檔案。</span><span class="sxs-lookup"><span data-stu-id="d7f87-105">For instance, your application might want to launch another application that allows the user to modify a data file.</span></span> <span data-ttu-id="d7f87-106">如果您感興趣的檔案是可執行檔，您的應用程式可能只想要啟動它。</span><span class="sxs-lookup"><span data-stu-id="d7f87-106">If the file of interest is an executable, your application might want to simply launch it.</span></span> <span data-ttu-id="d7f87-107">本檔將討論如何使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來執行這些工作。</span><span class="sxs-lookup"><span data-stu-id="d7f87-107">This document discusses how to use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to perform these tasks.</span></span>

-   [<span data-ttu-id="d7f87-108">使用 ShellExecute 和 ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d7f87-108">Using ShellExecute and ShellExecuteEx</span></span>](#using-shellexecute-and-shellexecuteex)
    -   [<span data-ttu-id="d7f87-109">物件動詞</span><span class="sxs-lookup"><span data-stu-id="d7f87-109">Object Verbs</span></span>](#object-verbs)
    -   [<span data-ttu-id="d7f87-110">使用 ShellExecuteEx 從網站提供啟用服務</span><span class="sxs-lookup"><span data-stu-id="d7f87-110">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>](#using-shellexecuteex-to-provide-activation-services-from-a-site)
    -   <span data-ttu-id="d7f87-111">[使用 ShellExecute 啟動 [搜尋] 對話方塊](#using-shellexecute-to-launch-the-search-dialog-box)</span><span class="sxs-lookup"><span data-stu-id="d7f87-111">[Using ShellExecute to Launch the Search Dialog Box](#using-shellexecute-to-launch-the-search-dialog-box)</span></span>
-   [<span data-ttu-id="d7f87-112">如何使用 ShellExecuteEx 的簡單範例</span><span class="sxs-lookup"><span data-stu-id="d7f87-112">A Simple Example of How to Use ShellExecuteEx</span></span>](#a-simple-example-of-how-to-use-shellexecuteex)

## <a name="using-shellexecute-and-shellexecuteex"></a><span data-ttu-id="d7f87-113">使用 ShellExecute 和 ShellExecuteEx</span><span class="sxs-lookup"><span data-stu-id="d7f87-113">Using ShellExecute and ShellExecuteEx</span></span>

<span data-ttu-id="d7f87-114">若要使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)，您的應用程式必須指定要處理的檔案或資料夾物件，以及指定作業的 *動詞* 。</span><span class="sxs-lookup"><span data-stu-id="d7f87-114">To use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), your application must specify the file or folder object that is to be acted on, and a *verb* that specifies the operation.</span></span> <span data-ttu-id="d7f87-115">若為 **ShellExecute**，請將這些值指派給適當的參數。</span><span class="sxs-lookup"><span data-stu-id="d7f87-115">For **ShellExecute**, assign these values to the appropriate parameters.</span></span> <span data-ttu-id="d7f87-116">針對 **ShellExecuteEx**，請填入 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) 結構的適當成員。</span><span class="sxs-lookup"><span data-stu-id="d7f87-116">For **ShellExecuteEx**, fill in the appropriate members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="d7f87-117">另外還有其他幾個成員或參數可用來微調兩個函式的行為。</span><span class="sxs-lookup"><span data-stu-id="d7f87-117">There are also several other members or parameters that can be used to fine-tune the behavior of the two functions.</span></span>

<span data-ttu-id="d7f87-118">檔案和資料夾物件可以是檔案系統或虛擬物件的一部分，而且可以透過路徑或專案識別碼清單的指標來識別 (Pidl) 。</span><span class="sxs-lookup"><span data-stu-id="d7f87-118">File and folder objects can be part of the file system or virtual objects, and they can be identified by either paths or pointers to item identifier lists (PIDLs).</span></span>

### <a name="object-verbs"></a><span data-ttu-id="d7f87-119">物件動詞</span><span class="sxs-lookup"><span data-stu-id="d7f87-119">Object Verbs</span></span>

<span data-ttu-id="d7f87-120">物件的可用動詞本質上是您在物件的快捷方式功能表上找到的專案。</span><span class="sxs-lookup"><span data-stu-id="d7f87-120">The verbs available for an object are essentially the items that you find on an object's shortcut menu.</span></span> <span data-ttu-id="d7f87-121">若要尋找可用的動詞，請在登錄下查看</span><span class="sxs-lookup"><span data-stu-id="d7f87-121">To find which verbs are available, look in the registry under</span></span>

<span data-ttu-id="d7f87-122">**HKEY \_類別 \_ 根目錄** \\ **CLSID** \\ *{object \_ clsid}* \\ **Shell** \\ *動詞*</span><span class="sxs-lookup"><span data-stu-id="d7f87-122">**HKEY\_CLASSES\_ROOT**\\**CLSID**\\ *{object\_clsid}*\\**Shell**\\*verb*</span></span>

<span data-ttu-id="d7f87-123">其中 *物件 \_ clsid* 是物件 (clsid) 的類別識別碼，而 *verb* 則是可用動詞命令的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f87-123">where *object\_clsid* is the class identifier (CLSID) of the object, and *verb* is the name of the available verb.</span></span> <span data-ttu-id="d7f87-124">*動詞* \\ **命令** 子機碼包含的資料，指出叫用該動詞時所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="d7f87-124">The *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="d7f87-125">若要找出可用於 [預先定義之 Shell 物件](handlers.md)的動詞，請查看位於</span><span class="sxs-lookup"><span data-stu-id="d7f87-125">To find out which verbs are available for [predefined Shell objects](handlers.md), look in the registry under</span></span>

<span data-ttu-id="d7f87-126">**HKEY \_類別 \_ 根** \\ *物件 \_ 名稱* \\ **shell** \\ *動詞* 命令</span><span class="sxs-lookup"><span data-stu-id="d7f87-126">**HKEY\_CLASSES\_ROOT**\\*object\_name*\\**shell**\\*verb*</span></span>

<span data-ttu-id="d7f87-127">其中 *物件 \_ 名稱* 是預先定義之 Shell 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f87-127">where *object\_name* is the name of the predefined Shell object.</span></span> <span data-ttu-id="d7f87-128">同樣地，*動詞* \\ **命令** 子機碼包含的資料會指出叫用該動詞時所發生的情況。</span><span class="sxs-lookup"><span data-stu-id="d7f87-128">Again, the *verb*\\**command** subkey contains the data indicating what happens when that verb is invoked.</span></span>

<span data-ttu-id="d7f87-129">常見的可用動詞包括：</span><span class="sxs-lookup"><span data-stu-id="d7f87-129">Commonly available verbs include:</span></span>



| <span data-ttu-id="d7f87-130">動詞命令</span><span class="sxs-lookup"><span data-stu-id="d7f87-130">Verb</span></span>       | <span data-ttu-id="d7f87-131">描述</span><span class="sxs-lookup"><span data-stu-id="d7f87-131">Description</span></span>                                                                                              |
|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f87-132">編輯</span><span class="sxs-lookup"><span data-stu-id="d7f87-132">edit</span></span>       | <span data-ttu-id="d7f87-133">啟動編輯器並開啟要編輯的檔。</span><span class="sxs-lookup"><span data-stu-id="d7f87-133">Launches an editor and opens the document for editing.</span></span>                                                   |
| <span data-ttu-id="d7f87-134">尋找</span><span class="sxs-lookup"><span data-stu-id="d7f87-134">find</span></span>       | <span data-ttu-id="d7f87-135">從指定的目錄起始搜尋。</span><span class="sxs-lookup"><span data-stu-id="d7f87-135">Initiates a search starting from the specified directory.</span></span>                                                |
| <span data-ttu-id="d7f87-136">開啟</span><span class="sxs-lookup"><span data-stu-id="d7f87-136">open</span></span>       | <span data-ttu-id="d7f87-137">啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-137">Launches an application.</span></span> <span data-ttu-id="d7f87-138">如果此檔案不是可執行檔，則會啟動其相關聯的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-138">If this file is not an executable file, its associated application is launched.</span></span> |
| <span data-ttu-id="d7f87-139">print</span><span class="sxs-lookup"><span data-stu-id="d7f87-139">print</span></span>      | <span data-ttu-id="d7f87-140">列印檔案檔。</span><span class="sxs-lookup"><span data-stu-id="d7f87-140">Prints the document file.</span></span>                                                                                |
| <span data-ttu-id="d7f87-141">properties</span><span class="sxs-lookup"><span data-stu-id="d7f87-141">properties</span></span> | <span data-ttu-id="d7f87-142">顯示物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="d7f87-142">Displays the object's properties.</span></span>                                                                        |
| <span data-ttu-id="d7f87-143">runas</span><span class="sxs-lookup"><span data-stu-id="d7f87-143">runas</span></span>      | <span data-ttu-id="d7f87-144">以系統管理員身分啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-144">Launches an application as Administrator.</span></span> <span data-ttu-id="d7f87-145">使用者帳戶控制 (UAC) 會提示使用者同意執行提高許可權的應用程式，或輸入用來執行應用程式之系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="d7f87-145">User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.</span></span> |



<span data-ttu-id="d7f87-146">每個動詞命令都對應至用來從主控台視窗啟動應用程式的命令。</span><span class="sxs-lookup"><span data-stu-id="d7f87-146">Each verb corresponds to the command that would be used to launch the application from a console window.</span></span> <span data-ttu-id="d7f87-147">**Open** 動詞是很好的範例，因為它通常是受支援的。</span><span class="sxs-lookup"><span data-stu-id="d7f87-147">The **open** verb is a good example, as it is commonly supported.</span></span> <span data-ttu-id="d7f87-148">針對 .exe 檔案， **開啟** 只會啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-148">For .exe files, **open** simply launches the application.</span></span> <span data-ttu-id="d7f87-149">不過，這通常是用來啟動在特定檔案上運作的應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-149">However, it is more commonly used to launch an application that operates on a particular file.</span></span> <span data-ttu-id="d7f87-150">比方說，Microsoft WordPad 可以開啟 .txt 的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7f87-150">For instance, .txt files can be opened by Microsoft WordPad.</span></span> <span data-ttu-id="d7f87-151">因此，.txt 檔案的 **open** 動詞會對應至類似下列的命令：</span><span class="sxs-lookup"><span data-stu-id="d7f87-151">The **open** verb for a .txt file would thus correspond to something like the following command:</span></span>


```C++
C:\Program Files\Windows NT\Accessories\Wordpad.exe" "%1"
```



<span data-ttu-id="d7f87-152">當您使用 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 或 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 來開啟 .txt 檔案時，Wordpad.exe 會以指定的檔案作為其引數來啟動。</span><span class="sxs-lookup"><span data-stu-id="d7f87-152">When you use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) or [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to open a .txt file, Wordpad.exe is launched with the specified file as its argument.</span></span> <span data-ttu-id="d7f87-153">某些命令可以有額外的引數（例如旗標），可視需要新增以正確啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-153">Some commands can have additional arguments, such as flags, that can be added as needed to launch the application properly.</span></span> <span data-ttu-id="d7f87-154">如需快捷方式功能表和動詞的進一步討論，請參閱 [擴充快捷方式功能表](context.md)。</span><span class="sxs-lookup"><span data-stu-id="d7f87-154">For further discussion of shortcut menus and verbs, see [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="d7f87-155">一般情況下，嘗試判斷特定檔案的可用動詞清單會有點複雜。</span><span class="sxs-lookup"><span data-stu-id="d7f87-155">In general, trying to determine the list of available verbs for a particular file is somewhat complicated.</span></span> <span data-ttu-id="d7f87-156">在許多情況下，您只要將 *lpVerb* 參數設定為 **Null**，就會叫用檔案類型的預設命令。</span><span class="sxs-lookup"><span data-stu-id="d7f87-156">In many cases, you can simply set the *lpVerb* parameter to **NULL**, which invokes the default command for the file type.</span></span> <span data-ttu-id="d7f87-157">此程式通常相當於將 *lpVerb* 設定為「開啟」，但某些檔案類型可能會有不同的預設命令。</span><span class="sxs-lookup"><span data-stu-id="d7f87-157">This procedure is usually equivalent to setting *lpVerb* to "open", but some file types may have a different default command.</span></span> <span data-ttu-id="d7f87-158">如需詳細資訊，請參閱 [擴充快捷方式功能表](context.md) 和 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) 參考檔。</span><span class="sxs-lookup"><span data-stu-id="d7f87-158">For further information, see [Extending Shortcut Menus](context.md) and the [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) reference documentation.</span></span>

### <a name="using-shellexecuteex-to-provide-activation-services-from-a-site"></a><span data-ttu-id="d7f87-159">使用 ShellExecuteEx 從網站提供啟用服務</span><span class="sxs-lookup"><span data-stu-id="d7f87-159">Using ShellExecuteEx to Provide Activation Services from a Site</span></span>

<span data-ttu-id="d7f87-160">網站鏈的服務可以控制專案啟用的許多行為。</span><span class="sxs-lookup"><span data-stu-id="d7f87-160">A site chain's services can control many behaviors of item activation.</span></span> <span data-ttu-id="d7f87-161">Windows 8，您可以提供指向 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)的網站鏈指標，以啟用這些行為。</span><span class="sxs-lookup"><span data-stu-id="d7f87-161">As of Windows 8, you can provide a pointer to the site chain to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) to enable these behaviors.</span></span> <span data-ttu-id="d7f87-162">若要提供網站給 **ShellExecuteEx**：</span><span class="sxs-lookup"><span data-stu-id="d7f87-162">To provide the site to **ShellExecuteEx**:</span></span>

-   <span data-ttu-id="d7f87-163">\_ \_ \_ \_ \_ 在 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)的 **fMask** 成員中，指定 HINST 為 SITE 旗標的 [請參閱遮罩旗標]。</span><span class="sxs-lookup"><span data-stu-id="d7f87-163">Specify the SEE\_MASK\_FLAG\_HINST\_IS\_SITE flag in the **fMask** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>
-   <span data-ttu-id="d7f87-164">在 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa)的 **hInstApp** 成員中提供 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 。</span><span class="sxs-lookup"><span data-stu-id="d7f87-164">Provide the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) in the **hInstApp** member of [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa).</span></span>

### <a name="using-shellexecute-to-launch-the-search-dialog-box"></a><span data-ttu-id="d7f87-165">使用 ShellExecute 啟動 [搜尋] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="d7f87-165">Using ShellExecute to Launch the Search Dialog Box</span></span>

<span data-ttu-id="d7f87-166">當使用者以滑鼠右鍵按一下 Windows 檔案總管中的資料夾圖示時，其中一個功能表項目是 [搜尋]。</span><span class="sxs-lookup"><span data-stu-id="d7f87-166">When a user right-clicks a folder icon in Windows Explorer, one of the menu items is "Search".</span></span> <span data-ttu-id="d7f87-167">如果他們選取該專案，則 Shell 會啟動其搜尋公用程式。</span><span class="sxs-lookup"><span data-stu-id="d7f87-167">If they select that item, the Shell launches its Search utility.</span></span> <span data-ttu-id="d7f87-168">此公用程式會顯示一個對話方塊，可用來搜尋指定文字字串的檔案。</span><span class="sxs-lookup"><span data-stu-id="d7f87-168">This utility displays a dialog box that can be used to search files for a specified text string.</span></span> <span data-ttu-id="d7f87-169">應用程式可以透過呼叫 [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)，以程式設計方式啟動目錄的搜尋公用程式，並以 "find" 作為 *lpVerb* 參數，並以目錄路徑作為 *lpFile* 參數。</span><span class="sxs-lookup"><span data-stu-id="d7f87-169">An application can programmatically launch the Search utility for a directory by calling [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), with "find" as the *lpVerb* parameter, and the directory path as the *lpFile* parameter.</span></span> <span data-ttu-id="d7f87-170">比方說，下面這行程式碼會啟動 c： MyPrograms 目錄的搜尋公用程式 \\ 。</span><span class="sxs-lookup"><span data-stu-id="d7f87-170">For instance, the following line of code launches the Search utility for the c:\\MyPrograms directory.</span></span>


```C++
ShellExecute(hwnd, "find", "c:\\MyPrograms", NULL, NULL, 0);
```



## <a name="a-simple-example-of-how-to-use-shellexecuteex"></a><span data-ttu-id="d7f87-171">如何使用 ShellExecuteEx 的簡單範例</span><span class="sxs-lookup"><span data-stu-id="d7f87-171">A Simple Example of How to Use ShellExecuteEx</span></span>

<span data-ttu-id="d7f87-172">下列範例主控台應用程式示範如何使用 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)。</span><span class="sxs-lookup"><span data-stu-id="d7f87-172">The following sample console application illustrates the use of [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span> <span data-ttu-id="d7f87-173">為了清楚起見，已省略大部分的錯誤檢查程式碼。</span><span class="sxs-lookup"><span data-stu-id="d7f87-173">Most error checking code has been omitted for clarity.</span></span>


```C++
#include <shlobj.h>
#include <shlwapi.h>
#include <objbase.h>

main()
{
    LPITEMIDLIST pidlWinFiles = NULL;
    LPITEMIDLIST pidlItems = NULL;
    IShellFolder *psfWinFiles = NULL;
    IShellFolder *psfDeskTop = NULL;
    LPENUMIDLIST ppenum = NULL;
    STRRET strDispName;
    TCHAR pszParseName[MAX_PATH];
    ULONG celtFetched;
    SHELLEXECUTEINFO ShExecInfo;
    HRESULT hr;
    BOOL fBitmap = FALSE;

    hr = SHGetFolderLocation(NULL, CSIDL_WINDOWS, NULL, NULL, &pidlWinFiles);

    hr = SHGetDesktopFolder(&psfDeskTop);

    hr = psfDeskTop->BindToObject(pidlWinFiles, NULL, IID_IShellFolder, (LPVOID *) &psfWinFiles);
    hr = psfDeskTop->Release();

    hr = psfWinFiles->EnumObjects(NULL,SHCONTF_FOLDERS | SHCONTF_NONFOLDERS, &ppenum);

    while( hr = ppenum->Next(1,&pidlItems, &celtFetched) == S_OK && (celtFetched) == 1)
    {
        psfWinFiles->GetDisplayNameOf(pidlItems, SHGDN_FORPARSING, &strDispName);
        StrRetToBuf(&strDispName, pidlItems, pszParseName, MAX_PATH);
        CoTaskMemFree(pidlItems);
        if(StrCmpI(PathFindExtension(pszParseName), TEXT( ".bmp")) == 0)
        {
            fBitmap = TRUE;
            break;
        }
    }

    ppenum->Release();

    if(fBitmap)
    {
        ShExecInfo.cbSize = sizeof(SHELLEXECUTEINFO);
        ShExecInfo.fMask = NULL;
        ShExecInfo.hwnd = NULL;
        ShExecInfo.lpVerb = NULL;
        ShExecInfo.lpFile = pszParseName;
        ShExecInfo.lpParameters = NULL;
        ShExecInfo.lpDirectory = NULL;
        ShExecInfo.nShow = SW_MAXIMIZE;
        ShExecInfo.hInstApp = NULL;

        ShellExecuteEx(&ShExecInfo);
    }

    CoTaskMemFree(pidlWinFiles);
    psfWinFiles->Release();

    return 0;
}
```



<span data-ttu-id="d7f87-174">應用程式會先抓取 Windows 目錄的 PIDL，並列舉其內容，直到找到第一個 .bmp 檔案為止。</span><span class="sxs-lookup"><span data-stu-id="d7f87-174">The application first retrieves the PIDL of the Windows directory, and enumerates its contents until it finds the first .bmp file.</span></span> <span data-ttu-id="d7f87-175">不同于先前的範例， [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 是用來抓取檔案的剖析名稱，而不是其顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d7f87-175">Unlike the earlier example, [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) is used to retrieve the file's parsing name instead of its display name.</span></span> <span data-ttu-id="d7f87-176">因為這是檔系統資料夾，所以剖析名稱是完整路徑，這是 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)所需的路徑。</span><span class="sxs-lookup"><span data-stu-id="d7f87-176">Because this is a file system folder, the parsing name is a fully qualified path, which is what is needed for [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

<span data-ttu-id="d7f87-177">一旦找到第一個 .bmp 檔案，就會將適當的值指派給 [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) 結構的成員。</span><span class="sxs-lookup"><span data-stu-id="d7f87-177">Once the first .bmp file has been located, appropriate values are assigned to the members of a [**SHELLEXECUTEINFO**](/windows/desktop/api/Shellapi/ns-shellapi-shellexecuteinfoa) structure.</span></span> <span data-ttu-id="d7f87-178">**LpFile** 成員會設定為檔案的剖析名稱，而 **lpVerb** 成員會設定為 **Null**，以開始預設作業。</span><span class="sxs-lookup"><span data-stu-id="d7f87-178">The **lpFile** member is set to the parsing name of the file, and the **lpVerb** member to **NULL**, to begin the default operation.</span></span> <span data-ttu-id="d7f87-179">在此情況下，預設作業為 "open"。</span><span class="sxs-lookup"><span data-stu-id="d7f87-179">In this case, the default operation is "open".</span></span> <span data-ttu-id="d7f87-180">然後，會將結構傳遞至 [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)，以啟動點陣圖檔案的預設處理常式（通常 MSPaint.exe）來開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="d7f87-180">The structure is then passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), which launches the default handler for bitmap files, typically MSPaint.exe, to open the file.</span></span> <span data-ttu-id="d7f87-181">函數傳回之後，pidl 就會釋出，並釋放 Windows 資料夾的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面。</span><span class="sxs-lookup"><span data-stu-id="d7f87-181">After the function returns, the PIDLs are freed and the Windows folder's [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) interface is released.</span></span>

 

 

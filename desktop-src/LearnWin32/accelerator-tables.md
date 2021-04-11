---
title: 快速鍵對應表
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023486"
---
# <a name="accelerator-tables"></a><span data-ttu-id="1a88b-103">快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="1a88b-103">Accelerator Tables</span></span>

<span data-ttu-id="1a88b-104">應用程式通常會定義鍵盤快速鍵，例如 [開啟檔案] 命令的 CTRL + O。</span><span class="sxs-lookup"><span data-stu-id="1a88b-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="1a88b-105">您可以藉由處理個別的 [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) 訊息來執行鍵盤快速鍵，但快速鍵對應表提供了更好的解決方案：</span><span class="sxs-lookup"><span data-stu-id="1a88b-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="1a88b-106">需要較少的編碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-106">Requires less coding.</span></span>
-   <span data-ttu-id="1a88b-107">將您所有的快捷方式合併成一個資料檔案。</span><span class="sxs-lookup"><span data-stu-id="1a88b-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="1a88b-108">支援其他語言的當地語系化。</span><span class="sxs-lookup"><span data-stu-id="1a88b-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="1a88b-109">啟用快速鍵和功能表命令以使用相同的應用程式邏輯。</span><span class="sxs-lookup"><span data-stu-id="1a88b-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="1a88b-110">*快速鍵對應表* 是將鍵盤組合（例如 CTRL + O）對應到應用程式命令的資料資源。</span><span class="sxs-lookup"><span data-stu-id="1a88b-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="1a88b-111">在瞭解如何使用快速鍵對應表之前，我們需要資源的快速簡介。</span><span class="sxs-lookup"><span data-stu-id="1a88b-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="1a88b-112">*資源* 是在應用程式二進位 (EXE 或 DLL) 內建的資料 blob。</span><span class="sxs-lookup"><span data-stu-id="1a88b-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="1a88b-113">資源會儲存應用程式所需的資料，例如功能表、資料指標、圖示、影像、文字字串或任何自訂應用程式資料。</span><span class="sxs-lookup"><span data-stu-id="1a88b-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="1a88b-114">應用程式會在執行時間從二進位檔載入資源資料。</span><span class="sxs-lookup"><span data-stu-id="1a88b-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="1a88b-115">若要將資源包含在二進位檔中，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1a88b-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="1a88b-116"> ( .rc) 檔案建立資源定義。</span><span class="sxs-lookup"><span data-stu-id="1a88b-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="1a88b-117">此檔案會定義資源類型及其識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="1a88b-118">資源定義檔可能包含其他檔案的參考。</span><span class="sxs-lookup"><span data-stu-id="1a88b-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="1a88b-119">例如，在 .rc 檔中宣告圖示資源，但圖示影像會儲存在不同的檔案中。</span><span class="sxs-lookup"><span data-stu-id="1a88b-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="1a88b-120">使用 Microsoft Windows 資源編譯器 (RC) 將資源定義檔編譯成已編譯的資源 ( .res) 檔。</span><span class="sxs-lookup"><span data-stu-id="1a88b-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="1a88b-121">RC 編譯器隨附 Visual Studio 以及 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="1a88b-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="1a88b-122">將已編譯的資源檔連結至二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="1a88b-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="1a88b-123">這些步驟大致上等同于程式碼檔案的編譯/連結程式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="1a88b-124">Visual Studio 提供一組資源編輯器，可讓您輕鬆地建立及修改資源。</span><span class="sxs-lookup"><span data-stu-id="1a88b-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="1a88b-125"> (這些工具不適用於 Visual Studio 的 Express 版本。 ) 但 .rc 檔只是文字檔，而語法記載于 MSDN 上，因此可以使用任何文字編輯器建立 .rc 檔。</span><span class="sxs-lookup"><span data-stu-id="1a88b-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="1a88b-126">如需詳細資訊，請參閱 [關於資源檔](/windows/desktop/menurc/about-resource-files)。</span><span class="sxs-lookup"><span data-stu-id="1a88b-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="1a88b-127">定義快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="1a88b-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="1a88b-128">快速鍵對應表是鍵盤快速鍵的表格。</span><span class="sxs-lookup"><span data-stu-id="1a88b-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="1a88b-129">每個快捷方式的定義方式如下：</span><span class="sxs-lookup"><span data-stu-id="1a88b-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="1a88b-130">數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-130">A numeric identifier.</span></span> <span data-ttu-id="1a88b-131">這個數位會識別要由快捷方式叫用的應用程式命令。</span><span class="sxs-lookup"><span data-stu-id="1a88b-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="1a88b-132">快速鍵的 ASCII 字元或虛擬按鍵碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="1a88b-133">選擇性輔助按鍵： ALT、SHIFT 或 CTRL。</span><span class="sxs-lookup"><span data-stu-id="1a88b-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="1a88b-134">快速鍵對應表本身具有數值識別碼，可識別應用程式資源清單中的資料表。</span><span class="sxs-lookup"><span data-stu-id="1a88b-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="1a88b-135">讓我們建立簡單繪圖程式的快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="1a88b-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="1a88b-136">此程式將會有兩種模式：繪圖模式和選取模式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="1a88b-137">在繪製模式中，使用者可以繪製圖形。</span><span class="sxs-lookup"><span data-stu-id="1a88b-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="1a88b-138">在選取模式中，使用者可以選取 [圖形]。</span><span class="sxs-lookup"><span data-stu-id="1a88b-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="1a88b-139">在這個程式中，我們想要定義下列鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="1a88b-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="1a88b-140">快速鍵</span><span class="sxs-lookup"><span data-stu-id="1a88b-140">Shortcut</span></span> | <span data-ttu-id="1a88b-141">命令</span><span class="sxs-lookup"><span data-stu-id="1a88b-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="1a88b-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="1a88b-142">CTRL+M</span></span>   | <span data-ttu-id="1a88b-143">切換模式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="1a88b-144">F1</span><span class="sxs-lookup"><span data-stu-id="1a88b-144">F1</span></span>       | <span data-ttu-id="1a88b-145">切換至繪圖模式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="1a88b-146">F2</span><span class="sxs-lookup"><span data-stu-id="1a88b-146">F2</span></span>       | <span data-ttu-id="1a88b-147">切換至選取模式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="1a88b-148">首先，定義資料表和應用程式命令的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="1a88b-149">這些值是任意的。</span><span class="sxs-lookup"><span data-stu-id="1a88b-149">These values are arbitrary.</span></span> <span data-ttu-id="1a88b-150">您可以在標頭檔中定義識別碼以指派其符號常數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="1a88b-151">例如：</span><span class="sxs-lookup"><span data-stu-id="1a88b-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="1a88b-152">在此範例中，值會 `IDR_ACCEL1` 識別快速鍵對應表，接下來的三個常數則會定義應用程式命令。</span><span class="sxs-lookup"><span data-stu-id="1a88b-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="1a88b-153">依照慣例，定義資源常數的標頭檔通常名為 resource .h。</span><span class="sxs-lookup"><span data-stu-id="1a88b-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="1a88b-154">下一個清單顯示資源定義檔。</span><span class="sxs-lookup"><span data-stu-id="1a88b-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="1a88b-155">快速鍵會定義在大括弧內。</span><span class="sxs-lookup"><span data-stu-id="1a88b-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="1a88b-156">每個快捷方式都包含下列專案。</span><span class="sxs-lookup"><span data-stu-id="1a88b-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="1a88b-157">叫用快捷方式的虛擬金鑰程式碼或 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="1a88b-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="1a88b-158">應用程式命令。</span><span class="sxs-lookup"><span data-stu-id="1a88b-158">The application command.</span></span> <span data-ttu-id="1a88b-159">請注意，此範例中會使用符號常數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="1a88b-160">資源定義檔包含資源 .h，其中定義了這些常數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="1a88b-161">關鍵字 **VIRTKEY** 表示第一個專案是虛擬金鑰程式碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="1a88b-162">另一個選項是使用 ASCII 字元。</span><span class="sxs-lookup"><span data-stu-id="1a88b-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="1a88b-163">選擇性修飾詞： ALT、CONTROL 或 SHIFT。</span><span class="sxs-lookup"><span data-stu-id="1a88b-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="1a88b-164">如果您將 ASCII 字元用於快速鍵，則小寫字元將會是與大寫字元不同的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="1a88b-165"> (例如，輸入 ' a ' 可能會叫用不同于輸入 ' A ' 的命令。 ) 可能會讓使用者混淆，因此通常最好是使用虛擬機器碼（而非 ASCII 字元）的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="1a88b-166">載入快速鍵對應表</span><span class="sxs-lookup"><span data-stu-id="1a88b-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="1a88b-167">必須先載入快速鍵對應表的資源，程式才能使用它。</span><span class="sxs-lookup"><span data-stu-id="1a88b-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="1a88b-168">若要載入快速鍵對應表，請呼叫 [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) 函數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="1a88b-169">請在輸入訊息迴圈之前呼叫這個函數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="1a88b-170">第一個參數是模組的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="1a88b-171"> (此參數會傳遞至您的 [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) 函數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="1a88b-172">如需詳細資訊，請參閱 [WinMain：應用程式進入點](winmain--the-application-entry-point.md)。 ) 第二個參數是資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="1a88b-173">函數會傳回資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="1a88b-174">回想一下，控制碼是一種不透明的類型，參考系統所管理的物件。</span><span class="sxs-lookup"><span data-stu-id="1a88b-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="1a88b-175">如果函式失敗，則會傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1a88b-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="1a88b-176">您可以藉由呼叫 [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable)來釋放快速鍵對應表。</span><span class="sxs-lookup"><span data-stu-id="1a88b-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="1a88b-177">不過，系統會在程式結束時自動釋出資料表，因此，如果您要以另一個資料表取代某個資料表，則只需要呼叫此函數。</span><span class="sxs-lookup"><span data-stu-id="1a88b-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="1a88b-178">在 [建立使用者可編輯加速器](/windows/desktop/menurc/using-keyboard-accelerators)的主題中，有一個有趣的範例。</span><span class="sxs-lookup"><span data-stu-id="1a88b-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="1a88b-179">將按鍵筆劃轉譯成命令</span><span class="sxs-lookup"><span data-stu-id="1a88b-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="1a88b-180">快速鍵轉換表的運作方式是將按鍵筆劃轉譯成 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息。</span><span class="sxs-lookup"><span data-stu-id="1a88b-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="1a88b-181">**WM \_ 命令** 的 *wParam* 參數包含命令的數值識別碼。</span><span class="sxs-lookup"><span data-stu-id="1a88b-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="1a88b-182">例如，使用先前顯示的表格，按鍵筆觸 CTRL + M 會轉譯為具有值的 **WM \_ 命令** 訊息 `ID_TOGGLE_MODE` 。</span><span class="sxs-lookup"><span data-stu-id="1a88b-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="1a88b-183">若要這樣做，請將您的訊息迴圈變更為下列內容：</span><span class="sxs-lookup"><span data-stu-id="1a88b-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="1a88b-184">這段程式碼會將呼叫新增至訊息迴圈內的 [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) 函式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="1a88b-185">**TranslateAccelerator** 函式會檢查每個視窗訊息，以尋找重要的訊息。</span><span class="sxs-lookup"><span data-stu-id="1a88b-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="1a88b-186">如果使用者按下快速鍵對應表中所列的其中一個按鍵組合， **TranslateAccelerator** 會將 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息傳送至視窗。</span><span class="sxs-lookup"><span data-stu-id="1a88b-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="1a88b-187">函數會直接叫用視窗程式來傳送 **WM \_ 命令** 。</span><span class="sxs-lookup"><span data-stu-id="1a88b-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="1a88b-188">當 **TranslateAccelerator** 成功轉譯按鍵筆劃時，此函式會傳回非零的值，這表示您應該略過訊息的正常處理。</span><span class="sxs-lookup"><span data-stu-id="1a88b-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="1a88b-189">否則， **TranslateAccelerator** 會傳回零。</span><span class="sxs-lookup"><span data-stu-id="1a88b-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="1a88b-190">在這種情況下，請將視窗訊息傳遞給 [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) 和 [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)，如往常一般。</span><span class="sxs-lookup"><span data-stu-id="1a88b-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="1a88b-191">繪圖程式可能處理 [**WM \_ 命令**](/windows/desktop/menurc/wm-command) 訊息的方式如下：</span><span class="sxs-lookup"><span data-stu-id="1a88b-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="1a88b-192">這段程式碼假設 `SetMode` 是應用程式所定義的函式，可在這兩種模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="1a88b-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="1a88b-193">您要如何處理每個命令的詳細資料，顯然取決於您的程式。</span><span class="sxs-lookup"><span data-stu-id="1a88b-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="1a88b-194">下一個</span><span class="sxs-lookup"><span data-stu-id="1a88b-194">Next</span></span>

[<span data-ttu-id="1a88b-195">設定游標影像</span><span class="sxs-lookup"><span data-stu-id="1a88b-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 
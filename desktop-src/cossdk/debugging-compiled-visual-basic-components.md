---
description: 因為在許多情況下，您將只能在 Microsoft Visual Basic 環境中，針對部分元件功能進行偵錯工具，所以在某些情況下，您將需要在編譯之後，對以 Visual Basic 建立的元件進行 debug。 由於 Visual Basic 環境並不會啟用這種情況，因此您必須改為使用 Microsoft Visual C++ 環境。
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: 已編譯的 Visual Basic 元件的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110641"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="a5a93-104">已編譯的 Visual Basic 元件的調試</span><span class="sxs-lookup"><span data-stu-id="a5a93-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="a5a93-105">假設在許多情況下，您只能夠在 Microsoft Visual Basic 環境內進行部分元件功能的偵錯工具，在某些情況下，您將需要在編譯之後，對以 Visual Basic 建立的元件進行處理。</span><span class="sxs-lookup"><span data-stu-id="a5a93-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="a5a93-106">由於 Visual Basic 環境並不會啟用這種情況，因此您必須改為使用 Microsoft Visual C++ 環境。</span><span class="sxs-lookup"><span data-stu-id="a5a93-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="a5a93-107">**若要在 Visual C++ 環境中進行 Visual Basic 元件的調試**</span><span class="sxs-lookup"><span data-stu-id="a5a93-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="a5a93-108">在 Visual Basic 6.0 中，開啟您要進行偵錯工具的 Visual Basic 專案。</span><span class="sxs-lookup"><span data-stu-id="a5a93-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="a5a93-109">**在 [檔案**] 功能表上，按一下 [**進行 YourProject.dll**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="a5a93-110">在 [ **製作專案** ] 對話方塊中，按一下 [ **選項**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="a5a93-111">在 [ **專案屬性** ] 對話方塊的 [ **編譯** ] 索引標籤上，按一下 [ **編譯成機器碼** 而 **不優化** ]，然後選取 [ **建立符號偵錯工具資訊** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="a5a93-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="a5a93-112">按一下 **[確定]**，然後再按一次 **[確定]** ，以編譯您的專案。</span><span class="sxs-lookup"><span data-stu-id="a5a93-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="a5a93-113">將已編譯的 DLL 移至通常已安裝 COM + 應用程式的位置。</span><span class="sxs-lookup"><span data-stu-id="a5a93-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="a5a93-114">如果您未移動 DLL，可能會收到錯誤訊息，告知您找不到 DLL 的符號調試資訊。</span><span class="sxs-lookup"><span data-stu-id="a5a93-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="a5a93-115">如果您無法讓偵錯工具在元件的中斷點上停止，請確認 DLL 位於標準封裝目錄中，從封裝中刪除該元件，然後重新加入元件。</span><span class="sxs-lookup"><span data-stu-id="a5a93-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="a5a93-116">開始 Visual C++。</span><span class="sxs-lookup"><span data-stu-id="a5a93-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="a5a93-117">**在 [檔案**] 功能表上，按一下 [**開啟工作區**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="a5a93-118">在 [ **開啟工作區** ] 對話方塊中，將 [ **檔案類型** ] 設定為 [所有檔案] **(\* 。 \*)**，選取已編譯的元件，然後按一下 [ **開啟**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="a5a93-119">**在 [檔案**] 功能表中，按一下 [**開啟** (未 **開啟工作區**]) ，然後開啟您想要進行偵錯工具的 Visual Basic 模組 (. bas) 、表單 (. keyfromnode.frm) 或類別 (。</span><span class="sxs-lookup"><span data-stu-id="a5a93-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="a5a93-120">在 [ **專案** ] 功能表上，按一下 [ **設定**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="a5a93-121">在 [**專案設定**] 對話方塊的 [**調試**] 索引標籤上，選取 [**類別目錄**] 方塊中的 **[一般**]。</span><span class="sxs-lookup"><span data-stu-id="a5a93-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="a5a93-122">在 [ **用於偵錯工具的可執行檔** ] 方塊中，輸入 Dllhost.exe 的完整路徑，後面接著一個引數，指定包含元件的 com + 應用程式的處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5a93-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="a5a93-123">您會在 [COM + 應用程式的 **屬性**] 對話方塊的 [**一般**] 索引標籤上找到處理序識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5a93-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="a5a93-124">以下是範例： C： \\ Winnt \\ System32 \\Dllhost.exe/ProcessID： { <processID> }。</span><span class="sxs-lookup"><span data-stu-id="a5a93-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="a5a93-125">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="a5a93-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5a93-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5a93-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5a93-127">COM + Visual Basic 支援與 MTS 對比</span><span class="sxs-lookup"><span data-stu-id="a5a93-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="a5a93-128">Visual Basic IDE 中的調試</span><span class="sxs-lookup"><span data-stu-id="a5a93-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 




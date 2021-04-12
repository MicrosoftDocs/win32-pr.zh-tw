---
description: 使用 GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: 使用 GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513676"
---
# <a name="using-graphedit"></a><span data-ttu-id="a378d-103">使用 GraphEdit</span><span class="sxs-lookup"><span data-stu-id="a378d-103">Using GraphEdit</span></span>

<span data-ttu-id="a378d-104">GraphEdit 可在 Microsoft Windows 軟體開發套件 (SDK)  () 中取得 <https://go.microsoft.com/fwlink/p/?linkid=62332> 。</span><span class="sxs-lookup"><span data-stu-id="a378d-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="a378d-105">GraphEdit 應用程式的名稱為 "graphedt.exe"。</span><span class="sxs-lookup"><span data-stu-id="a378d-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="a378d-106">安裝 SDK 之後，"graphedt.exe" 位於下列目錄： \[ Program Files \] \\ Microsoft sdk \\ Windows \\ \[ version \] \\ Bin \\ 。</span><span class="sxs-lookup"><span data-stu-id="a378d-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="a378d-107">執行 GraphEdit 之前，請使用 regsvr32 公用程式來註冊下列位於相同目錄中的 Dll：</span><span class="sxs-lookup"><span data-stu-id="a378d-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="a378d-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="a378d-108">proppage.dll</span></span>
-   <span data-ttu-id="a378d-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="a378d-109">evrprop.dll</span></span>

<span data-ttu-id="a378d-110">這些 Dll 可讓 GraphEdit 顯示某些內建的 DirectShow 篩選器的屬性頁。</span><span class="sxs-lookup"><span data-stu-id="a378d-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="a378d-111">建立檔案播放圖表</span><span class="sxs-lookup"><span data-stu-id="a378d-111">Build a File Playback Graph</span></span>

<span data-ttu-id="a378d-112">GraphEdit 可以建立檔案播放的篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a378d-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="a378d-113">這項功能相當於在應用程式中呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 方法。</span><span class="sxs-lookup"><span data-stu-id="a378d-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="a378d-114">**在 [檔案**] 功能表中，按一下 [轉譯 **媒體** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="a378d-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="a378d-115">GraphEdit 會顯示 [ **開啟** 檔案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a378d-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="a378d-116">選取多媒體檔案，然後按一下 [ **開啟**]。</span><span class="sxs-lookup"><span data-stu-id="a378d-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="a378d-117">GraphEdit 會建立一個篩選圖形來播放您所選取的檔案。</span><span class="sxs-lookup"><span data-stu-id="a378d-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="a378d-118">您也可以轉譯位於 URL 的媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="a378d-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="a378d-119">**在 [檔案**] 功能表中，按一下 [轉譯 **URL**]。</span><span class="sxs-lookup"><span data-stu-id="a378d-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="a378d-120">GraphEdit 會顯示對話方塊，以在其中輸入 URL。</span><span class="sxs-lookup"><span data-stu-id="a378d-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="a378d-121">建立篩選圖形</span><span class="sxs-lookup"><span data-stu-id="a378d-121">Build a Filter Graph</span></span>

<span data-ttu-id="a378d-122">GraphEdit 可以使用您系統上註冊的任何篩選器來建立自訂篩選圖形。</span><span class="sxs-lookup"><span data-stu-id="a378d-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="a378d-123">在 [ **圖形]** 功能表中，按一下 [ **插入篩選**]。</span><span class="sxs-lookup"><span data-stu-id="a378d-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="a378d-124">隨即出現一個對話方塊，內含您系統上的篩選器清單，依篩選分類進行組織。</span><span class="sxs-lookup"><span data-stu-id="a378d-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="a378d-125">GraphEdit 會從登錄中的資訊建立此清單。</span><span class="sxs-lookup"><span data-stu-id="a378d-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="a378d-126">下圖顯示對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a378d-126">The following illustration shows the dialog box.</span></span>

![您要插入哪些篩選準則？](images/gedit12.png)

<span data-ttu-id="a378d-128">若要將篩選新增至圖形，請選取篩選的名稱，然後按一下 [ **插入篩選** ] 按鈕，或按兩下篩選名稱。</span><span class="sxs-lookup"><span data-stu-id="a378d-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="a378d-129">加入篩選之後，您可以將滑鼠從某個篩選的輸出圖釘拖曳至另一個篩選的輸入圖釘，以連接兩個篩選器。</span><span class="sxs-lookup"><span data-stu-id="a378d-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="a378d-130">如果 pin 接受連線，GraphEdit 會繪製箭號來連接它們。</span><span class="sxs-lookup"><span data-stu-id="a378d-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![連接兩個篩選](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="a378d-132">執行圖形</span><span class="sxs-lookup"><span data-stu-id="a378d-132">Run the Graph</span></span>

<span data-ttu-id="a378d-133">在圖形編輯中建立篩選圖形之後，您就可以執行圖形來查看它是否如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="a378d-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="a378d-134">[ **圖形]** 功能表包含 [ **播放**]、[ **暫停**] 和 [ **停止**] 功能表命令。</span><span class="sxs-lookup"><span data-stu-id="a378d-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="a378d-135">這些命令會分別叫用 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 方法，分別 [**執行**](/windows/desktop/api/Control/nf-control-imediacontrol-run)、 [**暫停**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)和 [**停止**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。</span><span class="sxs-lookup"><span data-stu-id="a378d-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="a378d-136">GraphEdit 工具列也有這些命令的按鈕：</span><span class="sxs-lookup"><span data-stu-id="a378d-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![[暫停]、[播放] 和 [停止] 按鈕](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="a378d-138">GraphEdit **Stop** 命令會先暫停圖形並搜尋時間零 (假設圖形是可搜尋的) 。</span><span class="sxs-lookup"><span data-stu-id="a378d-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="a378d-139">針對檔案播放，此動作會將影片視窗重設為第一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="a378d-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="a378d-140">然後，GraphEdit 會呼叫 [**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。</span><span class="sxs-lookup"><span data-stu-id="a378d-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="a378d-141">如果圖表是可搜尋的，您可以拖曳出現在工具列下方的滑動軸來進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="a378d-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="a378d-142">拖曳滑杆列會叫用 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。</span><span class="sxs-lookup"><span data-stu-id="a378d-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="a378d-143">視圖屬性頁</span><span class="sxs-lookup"><span data-stu-id="a378d-143">View Property Pages</span></span>

<span data-ttu-id="a378d-144">某些篩選準則支援自訂屬性頁，可提供使用者介面來設定篩選準則的屬性。</span><span class="sxs-lookup"><span data-stu-id="a378d-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="a378d-145">若要在 GraphEdit 中查看篩選的屬性頁，請以滑鼠右鍵按一下篩選器，然後從快顯視窗中選取 [ **屬性** ]。</span><span class="sxs-lookup"><span data-stu-id="a378d-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="a378d-146">GraphEdit 會顯示內容頁，其中包含篩選 (所定義的屬性工作表（如果有任何) ）。</span><span class="sxs-lookup"><span data-stu-id="a378d-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="a378d-147">此外，GraphEdit 還包含篩選上每個釘選的屬性工作表。</span><span class="sxs-lookup"><span data-stu-id="a378d-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="a378d-148">釘選屬性工作表是由 GraphEdit 定義，而不是由篩選所定義。</span><span class="sxs-lookup"><span data-stu-id="a378d-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="a378d-149">如果連接釘選，[釘選] 屬性工作表會顯示連線的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a378d-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="a378d-150">否則，它會列出釘選的慣用媒體類型。</span><span class="sxs-lookup"><span data-stu-id="a378d-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="a378d-151">若要使用 GraphEdit 的內建屬性頁，您必須註冊 proppage.dll。</span><span class="sxs-lookup"><span data-stu-id="a378d-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="a378d-152">此 DLL 可在 Windows SDK 中使用。</span><span class="sxs-lookup"><span data-stu-id="a378d-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="a378d-153">此 DLL 也包含一些 DirectShow 篩選器的其他屬性頁。</span><span class="sxs-lookup"><span data-stu-id="a378d-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="a378d-154">這些屬性頁僅供進行偵錯工具之用。</span><span class="sxs-lookup"><span data-stu-id="a378d-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a378d-155">相關主題</span><span class="sxs-lookup"><span data-stu-id="a378d-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a378d-156">使用 GraphEdit 模擬圖表建立</span><span class="sxs-lookup"><span data-stu-id="a378d-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




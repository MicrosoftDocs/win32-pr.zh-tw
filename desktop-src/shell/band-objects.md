---
description: Microsoft Internet Explorer 4.0 引進了 Explorer 列，以提供與瀏覽器窗格連續的顯示區域。
title: 建立自訂瀏覽器列、工具區和桌上區
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104556943"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="0736c-103">建立自訂的瀏覽器列、工具區和書桌區</span><span class="sxs-lookup"><span data-stu-id="0736c-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="0736c-104">Microsoft Internet Explorer 4.0 引進了 Explorer 列，以提供與瀏覽器窗格連續的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="0736c-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="0736c-105">基本上它是 Windows Internet Explorer 視窗中的子視窗，它可以用來顯示資訊，並以許多相同的方式與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="0736c-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="0736c-106">Explorer 橫條最常顯示為 [瀏覽器] 窗格左側的垂直窗格。</span><span class="sxs-lookup"><span data-stu-id="0736c-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="0736c-107">不過，您也可以在瀏覽器窗格下方，以水準方式顯示 Explorer 列。</span><span class="sxs-lookup"><span data-stu-id="0736c-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![顯示垂直和水準瀏覽器列的螢幕擷取畫面。](images/expl1.jpg)

<span data-ttu-id="0736c-109">Explorer 列有各式各樣的可能用途。</span><span class="sxs-lookup"><span data-stu-id="0736c-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="0736c-110">使用者可以透過數種不同的方式來選取想要查看的選項，包括從 [ **View** ] 功能表的 [ **Explorer** ] 列子功能表選取它，或按一下工具列按鈕。</span><span class="sxs-lookup"><span data-stu-id="0736c-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="0736c-111">Internet Explorer 提供數個標準 Explorer 列，包括我的最愛和搜尋。</span><span class="sxs-lookup"><span data-stu-id="0736c-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="0736c-112">您可以自訂 Internet Explorer 的其中一種方式是加入自訂的瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="0736c-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="0736c-113">當執行並註冊時，它會加入至 [ **View** ] 功能表的 [ **Explorer Bar** ] 功能表中。</span><span class="sxs-lookup"><span data-stu-id="0736c-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="0736c-114">當使用者選取此選項時，就可以使用 Explorer 列的顯示區域來顯示資訊，並以一般視窗的相同方式來進行使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="0736c-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![explorer 列的螢幕擷取畫面](images/expl2.jpg)

<span data-ttu-id="0736c-116">若要建立自訂的瀏覽器列，您必須先執行並註冊一個 *帶線物件*。</span><span class="sxs-lookup"><span data-stu-id="0736c-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="0736c-117">在版本4.71 中引進了頻外物件，並提供類似于一般 windows 的功能。</span><span class="sxs-lookup"><span data-stu-id="0736c-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="0736c-118">不過，因為它們是元件物件模型 (COM) 物件，並由 Internet Explorer 或 Shell 所包含，所以會以不同的方式來執行。</span><span class="sxs-lookup"><span data-stu-id="0736c-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="0736c-119">簡單的帶狀物件是用來建立第一個圖形中所顯示的範例瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="0736c-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="0736c-120">將在稍後的章節中詳細討論垂直 Explorer Bar 範例的執行。</span><span class="sxs-lookup"><span data-stu-id="0736c-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="0736c-121">工具區</span><span class="sxs-lookup"><span data-stu-id="0736c-121">Tool Bands</span></span>

<span data-ttu-id="0736c-122">「 *工具區* 」是一種以 Microsoft Internet Explorer 5 引進的寬線物件，可支援 Windows 選項按鈕功能。</span><span class="sxs-lookup"><span data-stu-id="0736c-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="0736c-123">Internet Explorer 的工具列實際上是包含數個[工具列控制項](../controls/toolbar-control-reference.md)的[Rebar 控制項](../controls/rebar-controls.md)。</span><span class="sxs-lookup"><span data-stu-id="0736c-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="0736c-124">藉由建立工具區，您就可以在該 Rebar 控制項中加入一個頻外。</span><span class="sxs-lookup"><span data-stu-id="0736c-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="0736c-125">不過，如同 Explorer 橫條，工具區是一般用途的視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![工具區段的螢幕擷取畫面](images/toolband1.jpg)

<span data-ttu-id="0736c-127">使用者可以從 [ **View** ] 功能表的 [**工具列**] 子功能表，或是以滑鼠右鍵按一下工具列區域所顯示的快捷方式功能表中選取工具列來顯示工具列。</span><span class="sxs-lookup"><span data-stu-id="0736c-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="0736c-128">書桌區</span><span class="sxs-lookup"><span data-stu-id="0736c-128">Desk Bands</span></span>

<span data-ttu-id="0736c-129">頻外物件也可以用來建立 *桌面* 群組。</span><span class="sxs-lookup"><span data-stu-id="0736c-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="0736c-130">雖然其基本的執行類似于 Explorer 列，但服務中心區與 Internet Explorer 無關。</span><span class="sxs-lookup"><span data-stu-id="0736c-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="0736c-131">桌上型電腦區基本上是在桌面上建立可停駐視窗的方式。</span><span class="sxs-lookup"><span data-stu-id="0736c-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="0736c-132">使用者可以在工作列上按一下滑鼠右鍵，然後從 [ **工具列** ] 子功能表中選取它來選取它。</span><span class="sxs-lookup"><span data-stu-id="0736c-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![顯示範例服務中心的螢幕擷取畫面。](images/desk2.png)

<span data-ttu-id="0736c-134">一開始，桌面群組會停駐在工作列上。</span><span class="sxs-lookup"><span data-stu-id="0736c-134">Initially, desk bands are docked on the taskbar.</span></span>

![螢幕擷取畫面，顯示停駐在工作列上的桌面群組。](images/desk1.jpg)

<span data-ttu-id="0736c-136">然後，使用者可以將書桌波段拖曳至桌面，它就會顯示為一般視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![書桌波段的螢幕擷取畫面](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="0736c-138">執行帶狀物件</span><span class="sxs-lookup"><span data-stu-id="0736c-138">Implementing Band Objects</span></span>

<span data-ttu-id="0736c-139">討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="0736c-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="0736c-140">頻外物件基本概念</span><span class="sxs-lookup"><span data-stu-id="0736c-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="0736c-141">頻外註冊</span><span class="sxs-lookup"><span data-stu-id="0736c-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="0736c-142">自訂 Explorer 列的簡單範例</span><span class="sxs-lookup"><span data-stu-id="0736c-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="0736c-143">頻外物件基本概念</span><span class="sxs-lookup"><span data-stu-id="0736c-143">Band Object Basics</span></span>

<span data-ttu-id="0736c-144">雖然它們可以像一般視窗一樣使用，但頻外物件是存在於容器內的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="0736c-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="0736c-145">Explorer 列是由 Internet Explorer 所包含，而服務台則包含在 Shell 中。</span><span class="sxs-lookup"><span data-stu-id="0736c-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="0736c-146">雖然它們可提供不同的功能，但其基本的執行非常類似。</span><span class="sxs-lookup"><span data-stu-id="0736c-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="0736c-147">主要差異在於如何註冊波段物件，進而控制物件和其容器的類型。</span><span class="sxs-lookup"><span data-stu-id="0736c-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="0736c-148">本節將討論所有帶狀物件通用的執行層面。</span><span class="sxs-lookup"><span data-stu-id="0736c-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="0736c-149">如需其他的執行詳細資料，請參閱 [自訂 Explorer 列的簡單範例](#a-simple-example-of-a-custom-explorer-bar) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="0736c-150">除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 和 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)，所有的帶狀物件都必須執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="0736c-151">**IDeskBand**</span><span class="sxs-lookup"><span data-stu-id="0736c-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="0736c-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="0736c-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="0736c-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="0736c-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="0736c-154">除了將其類別識別碼註冊 (CLSID) 之外，還必須針對適當的元件類別註冊 Explorer Bar 和書桌等物件。</span><span class="sxs-lookup"><span data-stu-id="0736c-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="0736c-155">註冊元件類別會決定物件類型及其容器。</span><span class="sxs-lookup"><span data-stu-id="0736c-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="0736c-156">工具群組使用不同的註冊程式，且沒有 (CATID) 的分類識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="0736c-157">需要它們的三個頻外物件的 Catid 是：</span><span class="sxs-lookup"><span data-stu-id="0736c-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="0736c-158">頻外類型</span><span class="sxs-lookup"><span data-stu-id="0736c-158">Band Type</span></span>               | <span data-ttu-id="0736c-159">元件類別</span><span class="sxs-lookup"><span data-stu-id="0736c-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="0736c-160">垂直瀏覽器列</span><span class="sxs-lookup"><span data-stu-id="0736c-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="0736c-161">CATID \_ InfoBand</span><span class="sxs-lookup"><span data-stu-id="0736c-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="0736c-162">水準瀏覽器列</span><span class="sxs-lookup"><span data-stu-id="0736c-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="0736c-163">CATID \_ CommBand</span><span class="sxs-lookup"><span data-stu-id="0736c-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="0736c-164">書桌區</span><span class="sxs-lookup"><span data-stu-id="0736c-164">Desk Band</span></span>               | <span data-ttu-id="0736c-165">CATID \_ DeskBand</span><span class="sxs-lookup"><span data-stu-id="0736c-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="0736c-166">請參閱 [頻外註冊](#band-registration) ，以進一步討論如何註冊波段物件。</span><span class="sxs-lookup"><span data-stu-id="0736c-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="0736c-167">如果寬線物件是接受使用者輸入，則也必須執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)。</span><span class="sxs-lookup"><span data-stu-id="0736c-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="0736c-168">若要將專案加入至 Explorer 橫條圖或書桌群組的快捷方式功能表，必須將 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)匯出。</span><span class="sxs-lookup"><span data-stu-id="0736c-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="0736c-169">工具區不支援快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="0736c-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="0736c-170">因為頻外物件會執行子視窗，所以它們也必須執行視窗程式來處理 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="0736c-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="0736c-171">頻外物件可以透過容器的 [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) 介面，將命令傳送到其容器。</span><span class="sxs-lookup"><span data-stu-id="0736c-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="0736c-172">若要取得介面指標，請呼叫容器的 [**IInputObjectSite：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，並要求 IID \_ IOleCommandTarget。</span><span class="sxs-lookup"><span data-stu-id="0736c-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="0736c-173">然後，您可以使用 [**IOleCommandTarget：： Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec)將命令傳送至容器。</span><span class="sxs-lookup"><span data-stu-id="0736c-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="0736c-174">命令群組為 CGID \_ DeskBand。</span><span class="sxs-lookup"><span data-stu-id="0736c-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="0736c-175">當呼叫帶狀物件的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) 方法時，容器會使用 *dwBandID* 參數來指派用於三個命令的一個識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="0736c-176">支援四個 **IOleCommandTarget：： Exec** 命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="0736c-177">DBID \_ BANDINFOCHANGED</span><span class="sxs-lookup"><span data-stu-id="0736c-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="0736c-178">波段的資訊已變更。</span><span class="sxs-lookup"><span data-stu-id="0736c-178">The band's information has changed.</span></span> <span data-ttu-id="0736c-179">將 *pvaIn* 參數設定為最新的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)呼叫中所收到的頻外識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="0736c-180">容器會呼叫波段物件的 **IDeskBand：： GetBandInfo** 方法，以要求更新的資訊。</span><span class="sxs-lookup"><span data-stu-id="0736c-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="0736c-181">DBID \_ MAXIMIZEBAND</span><span class="sxs-lookup"><span data-stu-id="0736c-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="0736c-182">最大化頻外。</span><span class="sxs-lookup"><span data-stu-id="0736c-182">Maximize the band.</span></span> <span data-ttu-id="0736c-183">將 *pvaIn* 參數設定為最新的 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)呼叫中所收到的頻外識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="0736c-184">DBID \_ SHOWONLY</span><span class="sxs-lookup"><span data-stu-id="0736c-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="0736c-185">開啟或關閉容器中的其他波段。</span><span class="sxs-lookup"><span data-stu-id="0736c-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="0736c-186">將 *pvaIn* 參數設定為 \_ 具有下列其中一個值的 VT 未知類型：</span><span class="sxs-lookup"><span data-stu-id="0736c-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="0736c-187">值</span><span class="sxs-lookup"><span data-stu-id="0736c-187">Value</span></span> | <span data-ttu-id="0736c-188">描述</span><span class="sxs-lookup"><span data-stu-id="0736c-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0736c-189">朋 克</span><span class="sxs-lookup"><span data-stu-id="0736c-189">pUnk</span></span>  | <span data-ttu-id="0736c-190">頻外物件的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0736c-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0736c-191">所有其他的桌面群組將會隱藏。</span><span class="sxs-lookup"><span data-stu-id="0736c-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="0736c-192">0</span><span class="sxs-lookup"><span data-stu-id="0736c-192">0</span></span>     | <span data-ttu-id="0736c-193">隱藏所有的桌上波段。</span><span class="sxs-lookup"><span data-stu-id="0736c-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="0736c-194">1</span><span class="sxs-lookup"><span data-stu-id="0736c-194">1</span></span>     | <span data-ttu-id="0736c-195">顯示所有的桌面群組。</span><span class="sxs-lookup"><span data-stu-id="0736c-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="0736c-196">DBID \_ PUSHCHEVRON</span><span class="sxs-lookup"><span data-stu-id="0736c-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="0736c-197">[第5版](versions.md)。</span><span class="sxs-lookup"><span data-stu-id="0736c-197">[Version 5](versions.md).</span></span> <span data-ttu-id="0736c-198">顯示箭號功能表。</span><span class="sxs-lookup"><span data-stu-id="0736c-198">Display a chevron menu.</span></span> <span data-ttu-id="0736c-199">容器會傳送 [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) 訊息，而此寬線物件會收到 [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) 通知，提示它顯示箭號功能表。</span><span class="sxs-lookup"><span data-stu-id="0736c-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="0736c-200">將 [**IOleCommandTarget：： Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) 方法的 *nCmdExecOpt* 參數設定為最近呼叫 [**IDeskBand：： GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)時所收到的頻外識別碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="0736c-201">使用應用程式定義的值，將 **IOleCommandTarget：： Exec** 方法的 *pvaIn* 參數設定為 VT \_ I4 類型。</span><span class="sxs-lookup"><span data-stu-id="0736c-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="0736c-202">它會將 RBN CHEVRONPUSHED 通知的 *lAppValue* 值傳回給波段物件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0736c-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="0736c-203">頻外註冊</span><span class="sxs-lookup"><span data-stu-id="0736c-203">Band Registration</span></span>

<span data-ttu-id="0736c-204">波段物件必須註冊為支援單元執行緒的 OLE 同進程伺服器。</span><span class="sxs-lookup"><span data-stu-id="0736c-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="0736c-205">伺服器的預設值是功能表文字字串。</span><span class="sxs-lookup"><span data-stu-id="0736c-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="0736c-206">若是 Explorer 橫條，它會出現在 [Internet Explorer **View** ] 功能表的 [ **Explorer Bar** ] 子功能表中。</span><span class="sxs-lookup"><span data-stu-id="0736c-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="0736c-207">針對工具群組，它會出現在 [Internet Explorer **視圖**] 功能表的 [**工具列**] 子功能表中。</span><span class="sxs-lookup"><span data-stu-id="0736c-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="0736c-208">若為 [中]，則會出現在工作列快捷方式功能表的 [ **工具列** ] 子功能表中。</span><span class="sxs-lookup"><span data-stu-id="0736c-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="0736c-209">如同功能表資源，在字母前面加上連字號 (&) 會讓它加上底線，並啟用鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="0736c-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="0736c-210">例如，第一個圖形中顯示的垂直 Explorer 列的功能表字串為 "Sample &垂直 Explorer Bar"。</span><span class="sxs-lookup"><span data-stu-id="0736c-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="0736c-211">一開始，Internet Explorer 會使用元件類別，從登錄中取出已註冊之 Explorer Bar 物件的列舉。</span><span class="sxs-lookup"><span data-stu-id="0736c-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="0736c-212">為了提高效能，它會快取此列舉，進而忽略後續新增的瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="0736c-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="0736c-213">若要強制 Windows Internet Explorer 重建快取並辨識新的瀏覽器列，請在註冊新的瀏覽器列時刪除下列登錄機碼：</span><span class="sxs-lookup"><span data-stu-id="0736c-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="0736c-214">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **元件類別** \\ **{00021493-0000-0000-C000-000000000046}** \\ **Enum**</span><span class="sxs-lookup"><span data-stu-id="0736c-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="0736c-215">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **Discardable** \\ **PostSetup** \\ **元件類別** \\ **{00021494-0000-0000-C000-000000000046}** \\ **Enum**</span><span class="sxs-lookup"><span data-stu-id="0736c-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="0736c-216">因為系統會為每個使用者建立 Explorer Bar 快取，所以您的安裝應用程式可能需要列舉所有使用者登錄區，或新增每個使用者的存根，以在使用者第一次登入時執行。</span><span class="sxs-lookup"><span data-stu-id="0736c-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="0736c-217">一般情況下，寬線物件的基本登錄專案會如下所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="0736c-218">工具群組也必須將其物件的 CLSID 註冊 Internet Explorer。</span><span class="sxs-lookup"><span data-stu-id="0736c-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="0736c-219">若要這樣做，請在 [ **HKEY \_ 本機 \_ 電腦** 軟體 Microsoft Internet Explorer] 工具列上指派值（以 \\  \\  \\  \\ 工具區物件的 CLSID GUID 命名），如下所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="0736c-220">它的資料值會被忽略，因此值型別不重要。</span><span class="sxs-lookup"><span data-stu-id="0736c-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="0736c-221">您也可以將數個選擇性值新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="0736c-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="0736c-222">比方說，如果您想要使用 Explorer 列來顯示 HTML，所顯示的值不是範例，而是應該使用的實際值，則必須使用下列值。</span><span class="sxs-lookup"><span data-stu-id="0736c-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="0736c-223">搭配上述的值使用時，如果您想要使用 Explorer 列來顯示 HTML，也需要下列選用值。</span><span class="sxs-lookup"><span data-stu-id="0736c-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="0736c-224">此值應該設定為包含 Explorer 列 HTML 內容之檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="0736c-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="0736c-225">另一個選擇性值會定義 Explorer 列的預設寬度或高度，取決於它是垂直或水準。</span><span class="sxs-lookup"><span data-stu-id="0736c-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="0736c-226">BarSize 值應該設定為橫條的寬度或高度。</span><span class="sxs-lookup"><span data-stu-id="0736c-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="0736c-227">值需要八個位元組，並以二進位值的形式放在登錄中。</span><span class="sxs-lookup"><span data-stu-id="0736c-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="0736c-228">前四個位元組以十六進位格式指定以圖元為單位的大小，從最左邊的位元組開始。</span><span class="sxs-lookup"><span data-stu-id="0736c-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="0736c-229">最後四個位元組是保留的，而且應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="0736c-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="0736c-230">例如，這裡顯示預設寬度為 291 (0x123) 圖元的 HTML 可用瀏覽器列的完整登錄專案。</span><span class="sxs-lookup"><span data-stu-id="0736c-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="0736c-231">您可以透過程式設計方式來處理帶物件 CATID 的註冊。</span><span class="sxs-lookup"><span data-stu-id="0736c-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="0736c-232"> (CLSID StdComponentCategoriesMgr) 建立元件類別管理員物件 \_ ，並要求其 [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="0736c-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="0736c-233">將帶狀物件的 CLSID 和 CATID 傳遞給 [**ICatRegister：： RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories)。</span><span class="sxs-lookup"><span data-stu-id="0736c-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="0736c-234">自訂 Explorer 列的簡單範例</span><span class="sxs-lookup"><span data-stu-id="0736c-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="0736c-235">這個範例會逐步解說簡介中所顯示的範例垂直瀏覽器列。</span><span class="sxs-lookup"><span data-stu-id="0736c-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="0736c-236">建立自訂瀏覽器列的基本程式如下所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="0736c-237">[執行 DLL 所需的函數](#dll-functions)。</span><span class="sxs-lookup"><span data-stu-id="0736c-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="0736c-238">執行必要的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="0736c-239">執行任何想要的選擇性 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="0736c-240">註冊物件的 CLSID 和（如有必要）元件類別。</span><span class="sxs-lookup"><span data-stu-id="0736c-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="0736c-241">建立 Internet Explorer 的子視窗，調整大小以符合 Explorer 橫條圖的顯示區域。</span><span class="sxs-lookup"><span data-stu-id="0736c-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="0736c-242">您可以使用子視窗來顯示資訊，並與使用者互動。</span><span class="sxs-lookup"><span data-stu-id="0736c-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="0736c-243">在 Explorer Bar 範例中使用的非常簡單的實作為，只要針對適當的元件類別註冊，就可以用於任一種類型的 Explorer Bar 或書桌波段。</span><span class="sxs-lookup"><span data-stu-id="0736c-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="0736c-244">針對每個物件類型的顯示區域和容器，必須自訂更複雜的實作為。</span><span class="sxs-lookup"><span data-stu-id="0736c-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="0736c-245">不過，您可以藉由採用範例程式碼並將熟悉的 Windows 程式設計技術套用至子視窗，來完成這項自訂作業。</span><span class="sxs-lookup"><span data-stu-id="0736c-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="0736c-246">例如，您可以加入控制項以進行使用者互動，或為圖形提供更豐富的顯示。</span><span class="sxs-lookup"><span data-stu-id="0736c-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="0736c-247">DLL 函數</span><span class="sxs-lookup"><span data-stu-id="0736c-247">DLL Functions</span></span>

<span data-ttu-id="0736c-248">這三個物件都會封裝在單一 DLL 中，這會公開下列函式。</span><span class="sxs-lookup"><span data-stu-id="0736c-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="0736c-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="0736c-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="0736c-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="0736c-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="0736c-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="0736c-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="0736c-252">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="0736c-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="0736c-253">前三個函式是標準的實作為，將不會在此討論。</span><span class="sxs-lookup"><span data-stu-id="0736c-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="0736c-254">Class Factory 實也是標準的。</span><span class="sxs-lookup"><span data-stu-id="0736c-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="0736c-255">必要的介面實現</span><span class="sxs-lookup"><span data-stu-id="0736c-255">Required Interface Implementations</span></span>

<span data-ttu-id="0736c-256">垂直 Explorer 列範例會實作為 CExplorerBar 類別一部分的四個必要介面： [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)、 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)、 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)和 [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="0736c-257">函式、函式和 **IUnknown** 實作為簡單的，而且不會在這裡討論。</span><span class="sxs-lookup"><span data-stu-id="0736c-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="0736c-258">如需詳細資訊，請參閱範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-258">See the sample code for details.</span></span>

<span data-ttu-id="0736c-259">以下是詳細討論的介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="0736c-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="0736c-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="0736c-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="0736c-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="0736c-262">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="0736c-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="0736c-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="0736c-263">IObjectWithSite</span></span>

<span data-ttu-id="0736c-264">當使用者選取 Explorer 列時，容器會呼叫對應的帶狀物件的 [**IObjectWithSite：： SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 方法。</span><span class="sxs-lookup"><span data-stu-id="0736c-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="0736c-265">*PunkSite* 參數將設定為網站的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)指標。</span><span class="sxs-lookup"><span data-stu-id="0736c-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="0736c-266">一般情況下， [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 執行應該執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="0736c-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="0736c-267">釋放目前保留的任何網站指標。</span><span class="sxs-lookup"><span data-stu-id="0736c-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="0736c-268">如果傳遞至 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 的指標設為 **Null**，則會移除該頻外。</span><span class="sxs-lookup"><span data-stu-id="0736c-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="0736c-269">**SetSite** 可以傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="0736c-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="0736c-270">如果傳遞至 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 的指標為非 **Null**，則會設定新的網站。</span><span class="sxs-lookup"><span data-stu-id="0736c-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="0736c-271">**SetSite** 應該執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="0736c-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="0736c-272">針對其 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)介面呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="0736c-273">呼叫 [**IOleWindow：： GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 來取得父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="0736c-274">儲存控制碼以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="0736c-274">Save the handle for later use.</span></span> <span data-ttu-id="0736c-275">如果不再需要，請發行 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="0736c-276">建立帶狀物件的視窗，作為上一個步驟中取得之視窗的子系。</span><span class="sxs-lookup"><span data-stu-id="0736c-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="0736c-277">請勿將它建立為可見視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="0736c-278">如果寬線物件會執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject)，請針對其 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite)介面呼叫網站上的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="0736c-279">將指標儲存至此介面，以供稍後使用。</span><span class="sxs-lookup"><span data-stu-id="0736c-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="0736c-280">如果所有步驟都成功，請返回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="0736c-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="0736c-281">如果不是，則傳回 OLE 自訂錯誤碼，指出失敗的內容。</span><span class="sxs-lookup"><span data-stu-id="0736c-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="0736c-282">Explorer Bar 範例以下列方式執行 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="0736c-283">在下列程式碼中， *m \_ pSite* 是保存 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) 指標的私用成員變數，而 *m \_ hwndParent* 會保存父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="0736c-284">在此範例中，也會處理視窗建立。</span><span class="sxs-lookup"><span data-stu-id="0736c-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="0736c-285">如果視窗不存在，這個方法會將 Explorer 列的視窗建立為 **SetSite** 所取得之父視窗的適當大小子系。</span><span class="sxs-lookup"><span data-stu-id="0736c-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="0736c-286">子視窗的控制碼會儲存在 *m \_ hwnd* 中。</span><span class="sxs-lookup"><span data-stu-id="0736c-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="0736c-287">範例的 [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite)實只要使用 [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite)所儲存的網站指標來包裝對網站的 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="0736c-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="0736c-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="0736c-288">IPersistStream</span></span>

<span data-ttu-id="0736c-289">Internet Explorer 會呼叫 Explorer 列的 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) 介面，以允許 explorer 列載入或儲存持續性資料。</span><span class="sxs-lookup"><span data-stu-id="0736c-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="0736c-290">如果沒有持續性資料，則方法仍必須傳回成功碼。</span><span class="sxs-lookup"><span data-stu-id="0736c-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="0736c-291">**IPersistStream** 介面繼承自 [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist)，因此必須執行五個方法。</span><span class="sxs-lookup"><span data-stu-id="0736c-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="0736c-292">**IPersist：： GetClassID**</span><span class="sxs-lookup"><span data-stu-id="0736c-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="0736c-293">**IPersistStream：： IsDirty**</span><span class="sxs-lookup"><span data-stu-id="0736c-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="0736c-294">**IPersistStream：： Load**</span><span class="sxs-lookup"><span data-stu-id="0736c-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="0736c-295">**IPersistStream：： Save**</span><span class="sxs-lookup"><span data-stu-id="0736c-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="0736c-296">**IPersistStream：： GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="0736c-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="0736c-297">Explorer Bar 範例不會使用任何持續性資料，而且只有最基本的 [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)執行。</span><span class="sxs-lookup"><span data-stu-id="0736c-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="0736c-298">[**IPersist：： GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) 會傳回物件的 CLSID (clsid \_ SampleExplorerBar) ，其餘部分則會傳回 \_ [OK]、[ \_ FALSE] 或 [E >notimpl] \_ 。</span><span class="sxs-lookup"><span data-stu-id="0736c-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="0736c-299">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="0736c-299">IDeskBand</span></span>

<span data-ttu-id="0736c-300">[**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)介面是適用于頻外物件的。</span><span class="sxs-lookup"><span data-stu-id="0736c-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="0736c-301">除了它的方法之外，它也繼承自 [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)，而後者又繼承自 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)。</span><span class="sxs-lookup"><span data-stu-id="0736c-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="0736c-302">有兩種 [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) 方法： [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) 和 [**IOleWindow：： CoNtextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp)。</span><span class="sxs-lookup"><span data-stu-id="0736c-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="0736c-303">Explorer Bar 範例的 **GetWindow** 會傳回 explorer 列的子視窗控制碼（ *m \_ hwnd*）。</span><span class="sxs-lookup"><span data-stu-id="0736c-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="0736c-304">不會執行即時線上說明，因此 **CoNtextSensitiveHelp** 會傳回 **E \_ >notimpl**。</span><span class="sxs-lookup"><span data-stu-id="0736c-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="0736c-305">[**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)介面有三個方法。</span><span class="sxs-lookup"><span data-stu-id="0736c-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="0736c-306">**IDockingWindow::ShowDW**</span><span class="sxs-lookup"><span data-stu-id="0736c-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="0736c-307">**IDockingWindow::CloseDW**</span><span class="sxs-lookup"><span data-stu-id="0736c-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="0736c-308">**IDockingWindow::ResizeBorderDW**</span><span class="sxs-lookup"><span data-stu-id="0736c-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="0736c-309">[**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)方法不會與任何類型的波段物件一起使用，且一律會傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="0736c-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="0736c-310">[**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)方法會根據其參數的值顯示或隱藏 Explorer 工具列的視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="0736c-311">[**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)方法會終結 Explorer 工具列的視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="0736c-312">其餘的方法 [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)是 **IDeskBand** 專用的。</span><span class="sxs-lookup"><span data-stu-id="0736c-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="0736c-313">Internet Explorer 使用它來指定 Explorer 列的識別碼和瀏覽模式。</span><span class="sxs-lookup"><span data-stu-id="0736c-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="0736c-314">Internet Explorer 也可能會填入以第三個參數傳遞之 [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo)結構的 **dwMask** 成員，以從 Explorer 列要求一或多個資訊。</span><span class="sxs-lookup"><span data-stu-id="0736c-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="0736c-315">**GetBandInfo** 應該儲存識別碼和查看模式，並以要求的資料填入 **DESKBANDINFO** 結構。</span><span class="sxs-lookup"><span data-stu-id="0736c-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="0736c-316">Explorer Bar 範例會實 **GetBandInfo** ，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="0736c-317">選用介面實作為</span><span class="sxs-lookup"><span data-stu-id="0736c-317">Optional Interface Implementations</span></span>

<span data-ttu-id="0736c-318">有兩個介面不是必要的，但可能有助於實作為： [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) 和 [**ICoNtextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="0736c-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="0736c-319">Explorer Bar 範例會執行 **IInputObject**。</span><span class="sxs-lookup"><span data-stu-id="0736c-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="0736c-320">如需如何執行 **ICoNtextMenu** 的相關資訊，請參閱檔。</span><span class="sxs-lookup"><span data-stu-id="0736c-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="0736c-321">IInputObject</span><span class="sxs-lookup"><span data-stu-id="0736c-321">IInputObject</span></span>

<span data-ttu-id="0736c-322">如果波段物件接受使用者輸入，則必須執行 [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="0736c-323">Internet Explorer 會執行 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) ，並使用 **IInputObject** 來維持適當的使用者輸入焦點（當它有一個以上的包含視窗時）。</span><span class="sxs-lookup"><span data-stu-id="0736c-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="0736c-324">有三種方法需要由 Explorer 列來執行。</span><span class="sxs-lookup"><span data-stu-id="0736c-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="0736c-325">**IInputObject::UIActivateIO**</span><span class="sxs-lookup"><span data-stu-id="0736c-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="0736c-326">**IInputObject::HasFocusIO**</span><span class="sxs-lookup"><span data-stu-id="0736c-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="0736c-327">**IInputObject::TranslateAcceleratorIO**</span><span class="sxs-lookup"><span data-stu-id="0736c-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="0736c-328">Internet Explorer 會呼叫 [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) 來通知 Explorer 列正在啟用或停用。</span><span class="sxs-lookup"><span data-stu-id="0736c-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="0736c-329">啟用時，Explorer Bar 範例會呼叫 [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) 將焦點設定至其視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="0736c-330">Internet Explorer 在嘗試判斷哪個視窗具有焦點時，會呼叫 [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) 。</span><span class="sxs-lookup"><span data-stu-id="0736c-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="0736c-331">如果 Explorer 列的視窗或其中一個子代具有焦點，則 **HasFocusIO** 應該會傳回 \_ [確定]。</span><span class="sxs-lookup"><span data-stu-id="0736c-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="0736c-332">如果沒有，則應該傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="0736c-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="0736c-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) 可讓物件處理鍵盤快捷。</span><span class="sxs-lookup"><span data-stu-id="0736c-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="0736c-334">Explorer Bar 範例不會執行此方法，因此它會傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="0736c-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="0736c-335">範例列的 [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) 執行如下所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="0736c-336">CLSID 註冊</span><span class="sxs-lookup"><span data-stu-id="0736c-336">CLSID Registration</span></span>

<span data-ttu-id="0736c-337">和所有 COM 物件一樣，必須註冊 Explorer 列的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="0736c-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="0736c-338">為了讓物件能夠與 Internet Explorer 正常運作，它也必須註冊 (CATID InfoBand) 的適當元件類別 \_ 。</span><span class="sxs-lookup"><span data-stu-id="0736c-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="0736c-339">下列程式碼範例會顯示 Explorer 列的相關程式碼區段。</span><span class="sxs-lookup"><span data-stu-id="0736c-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="0736c-340">範例中的頻外物件註冊會使用一般 COM 程式。</span><span class="sxs-lookup"><span data-stu-id="0736c-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="0736c-341">除了 CLSID 之外，也必須針對一或多個元件類別目錄註冊帶狀物件服務器。</span><span class="sxs-lookup"><span data-stu-id="0736c-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="0736c-342">這實際上是在垂直和水準瀏覽器橫條圖範例之間執行的主要差異。</span><span class="sxs-lookup"><span data-stu-id="0736c-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="0736c-343">這項處理常式的處理方式是建立元件類別管理員物件 (CLSID \_ StdComponentCategoriesMgr) 並使用 [**ICatRegister：： RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) 方法來註冊帶的物件服務器。</span><span class="sxs-lookup"><span data-stu-id="0736c-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="0736c-344">在此範例中，元件類別註冊的處理方式是將 Explorer Bar 範例的 CLSID 和 CATID 傳遞至私用函式（**RegisterComCat**），如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="0736c-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="0736c-345">視窗程式</span><span class="sxs-lookup"><span data-stu-id="0736c-345">The Window Procedure</span></span>

<span data-ttu-id="0736c-346">因為寬線物件會使用子視窗來顯示它，所以它必須執行視窗程式來處理 Windows 訊息。</span><span class="sxs-lookup"><span data-stu-id="0736c-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="0736c-347">頻外範例有最基本的功能，因此其視窗程式只會處理五個訊息：</span><span class="sxs-lookup"><span data-stu-id="0736c-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="0736c-348">**WM \_ NCCREATE**</span><span class="sxs-lookup"><span data-stu-id="0736c-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="0736c-349">**WM \_ 油漆**</span><span class="sxs-lookup"><span data-stu-id="0736c-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="0736c-350">**WM \_ 命令**</span><span class="sxs-lookup"><span data-stu-id="0736c-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="0736c-351">**WM \_ SETFOCUS**</span><span class="sxs-lookup"><span data-stu-id="0736c-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="0736c-352">**WM \_ KILLFOCUS**</span><span class="sxs-lookup"><span data-stu-id="0736c-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="0736c-353">您可以輕鬆地展開程式以容納額外的訊息，以支援更多的功能。</span><span class="sxs-lookup"><span data-stu-id="0736c-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="0736c-354">WM \_ 命令處理常式只會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0736c-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="0736c-355">在 \_ 簡介中，WM 油漆處理常式會建立顯示在 Explorer Bar 範例中的簡單文字顯示。</span><span class="sxs-lookup"><span data-stu-id="0736c-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="0736c-356">WM \_ SETFOCUS 和 WM \_ KILLFOCUS 處理常式會藉由呼叫網站的 [**IInputObjectSite：： OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) 方法，來通知網站焦點變更。</span><span class="sxs-lookup"><span data-stu-id="0736c-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="0736c-357">頻外物件可透過建立自訂的瀏覽器列，提供有彈性且功能強大的方式來擴充 Internet Explorer 的功能。</span><span class="sxs-lookup"><span data-stu-id="0736c-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="0736c-358">執行服務台區可讓您延伸一般視窗的功能。</span><span class="sxs-lookup"><span data-stu-id="0736c-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="0736c-359">雖然需要一些 COM 程式設計，但最終還是會為您的使用者介面提供子視窗。</span><span class="sxs-lookup"><span data-stu-id="0736c-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="0736c-360">從該處，大部分的執行都可以使用熟悉的 Windows 程式設計技術。</span><span class="sxs-lookup"><span data-stu-id="0736c-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="0736c-361">雖然這裡所討論的範例僅具有有限的功能，但它也說明了一個頻外物件的所有必要功能，而且可以輕鬆擴充以建立獨特且功能強大的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="0736c-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 

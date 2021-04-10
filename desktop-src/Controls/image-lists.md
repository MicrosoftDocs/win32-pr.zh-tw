---
title: 關於影像清單
description: 影像清單是相同大小的影像集合，每個影像都可由其索引參考。
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f059e89b04d16088fff1d937bd29cb23a427d4c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316531"
---
# <a name="about-image-lists"></a>關於影像清單

影像清單是相同大小的影像集合，每個影像都可由其索引參考。 影像清單用來有效管理大量圖示或點陣圖。 影像清單中的所有影像都包含在螢幕裝置格式的單一全寬點陣圖中。 影像清單也可以包含用來以透明方式繪製影像 (圖示樣式) 的單色點陣圖。

Microsoft WIN32 API 提供影像清單函式和宏，可讓您建立和終結影像清單、新增和移除影像、取代和合併影像、繪製影像，以及拖曳影像。 若要使用影像清單函式，請在原始程式碼檔中包含通用控制項標頭檔，並連結至通用控制項匯出程式庫。 此外，在呼叫任何影像清單函式之前，請先使用 [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) 或 [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) 函式，以確保已載入通用控制項 DLL。

本節將討論下列主題：

-   [類型](#types)
-   [建立和終結影像清單](#creating-and-destroying-image-lists)
-   [新增和移除映射](#adding-and-removing-images)
-   [取代和合併影像](#replacing-and-merging-images)
-   [繪圖影像](#drawing-images)
-   [拖曳影像](#dragging-images)
-   [影像資訊](#image-information)
-   [影像覆蓋](#image-overlays)
-   [32位反鋸齒圖示](#32-bit-antialiased-icons)

## <a name="types"></a>類型

影像清單有兩種類型： nonmasked 和遮罩。 Nonmasked 影像清單包含包含一或多個影像的色彩點陣圖。 遮罩的影像清單包含兩個大小相同的點陣圖。 第一個是包含影像的色彩點陣圖，而第二個則是包含一連串遮罩的單色點陣圖（第一個點陣圖中的每個影像各一個）。

繪製 nonmasked 映射時，它只會複製到目標裝置內容中;也就是說，它會繪製在裝置內容的現有背景色彩上。 繪製遮罩的影像時，影像的位會與遮罩的位結合，通常會在點陣圖中產生透明區域，其中目標裝置內容的背景色彩會透過該點陣圖顯示。 當您繪製遮罩影像時，可以指定多個繪製樣式。 例如，您可以指定影像為遞色以表示選取的物件。

## <a name="creating-and-destroying-image-lists"></a>建立和終結影像清單

您可以藉由呼叫 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函數來建立影像清單。 這些參數包含要建立的影像清單類型、每個影像的維度，以及您想要新增至清單的影像數目。 針對 nonmasked 影像清單，此函式會建立夠大的單一點陣圖，以容納指定維度的指定數目影像。 然後，它會建立與螢幕相容的裝置內容，並在其中選取點陣圖。 針對遮罩影像清單，此函式會建立兩個位圖和兩個螢幕相容的裝置內容。 它會將影像點陣圖選取為一個裝置內容，並將遮罩點陣圖選取至另一個。 通用控制項 DLL 包含影像清單函式的可執行程式碼。

在 [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)中，您會指定將在影像清單中的初始影像數目，以及清單可成長的影像數目。 因此，如果您嘗試新增的影像數目超過最初指定的數目，則影像清單會自動成長以容納新的影像。

如果 [**ImageList \_ 建立**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 成功，它會傳回 HIMAGELIST 類型的控制碼。 您可以使用其他影像清單函式中的這個控制碼來存取影像清單和管理影像。 您可以新增和移除影像、將影像從某個影像清單複製到另一個影像清單，以及合併兩個不同影像清單中的影像。 當您不再需要影像清單時，可以在對 [**ImageList 損 \_ 毀**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) 函式的呼叫中指定其控制碼來終結它。

## <a name="adding-and-removing-images"></a>新增和移除映射

您可以將點陣圖影像、圖示或游標加入影像清單中。 您可以在對 [**ImageList \_ add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) 函式的呼叫中指定兩個位圖的控制碼，以新增點陣圖影像。 第一個點陣圖包含一或多個要加入影像點陣圖的影像，而第二個位圖包含要加入遮罩點陣圖的遮罩。 針對 nonmasked 影像清單，會忽略第二個位圖控制碼;可以設定為 **Null**。

[**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)函式也會將點陣圖影像新增至遮罩影像清單。 此函式類似于 [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)，不同之處在于您未指定遮罩點陣圖。 相反地，您可以指定一種色彩，讓系統與影像點陣圖合併以自動產生遮罩。 影像點陣圖中指定之色彩的每個圖元都會變更為黑色，且遮罩中的對應位會設定為1。 因此，繪製影像時，影像中符合指定色彩的任何圖元都是透明的。

[**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon)宏會將圖示或游標加入影像清單中。 如果影像清單已遮罩， **ImageList \_ AddIcon** 會將以圖示或游標提供的遮罩加入遮罩點陣圖。 如果影像清單是 nonmasked，則繪製影像時不會使用圖示或游標的遮罩。

您可以使用 [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) 函式，根據影像清單中的影像和遮罩來建立圖示。 函數會將控制碼傳回至新的圖示。

[**ImageList \_Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add)、 [**imagelist \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)和 [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) 會在每個影像新增至影像清單時，將索引指派給每個影像。 索引是以零為基底;也就是說，清單中的第一個影像的索引為零，下一個影像的索引為1，依此類推。 新增單一映射之後，函式會傳回影像的索引。 當一次新增一個以上的映射時，函式會傳回第一個影像的索引。

[**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove)函數會從影像清單中移除影像。

## <a name="replacing-and-merging-images"></a>取代和合併影像

[**Imagelist \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace)和 [**imagelist \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon)函式會以新的影像取代影像清單中的影像。 **ImageList \_Replace** 會以點陣圖影像和遮罩取代影像，而 **ImageList \_ ReplaceIcon** 會以圖示或游標取代影像。

[**ImageList \_ 合併**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge)函式會合並兩個影像，並將新的影像儲存在新的影像清單中。 新的影像會以在第一個影像上繪製透明的第二個影像來立。 新映射的遮罩是在兩個現有映射的遮罩位上執行邏輯 **OR** 運算的結果。

## <a name="drawing-images"></a>繪圖影像

若要繪製影像，請使用 [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 函數。 您可以指定影像清單的控制碼、要繪製之影像的索引、目的地裝置內容的控制碼、裝置內容中的位置，以及一或多個繪製樣式。

當您指定 **I ... \_ 透明** 樣式時， [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 會使用兩個步驟的程式來繪製遮罩的影像。 首先，它會對影像的位和遮罩的位執行邏輯 **and** 運算。 然後，它會在第一個作業的結果和目的地裝置內容的背景位上執行邏輯 **XOR** 運算。 這個程序會在產生的影像中建立透明區域，即遮罩中每個白色位元會使產生影像的對應位元變成透明。

在純色背景上繪製遮罩影像之前，您應該使用 [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) 函式，將影像清單的背景色彩設定為與目的地相同的色彩。 設定色彩不需要在影像中建立透明區域，而且可讓 [**imagelist \_ 繪圖**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 只將影像複製到目的地裝置內容，進而大幅提升效能。 若要繪製影像，請在對 **imagelist \_ Draw** 或 **imagelist \_ DrawEx** 的呼叫中指定 **i ... \_ NORMAL** 樣式。

您可以隨時設定遮罩影像清單的背景色彩，以便在任何穩固的背景上正確地繪製。 將背景色彩設定為 CLR \_ NONE，預設會導致影像以透明的方式繪製。 若要取得影像清單的背景色彩，請使用 [**ImageList \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) 函數。

[ **I ... \_ BLEND25** ] 和 [ **i ... \_ BLEND50** ] 樣式會以系統反白顯示色彩來遞色影像。 如果您使用代表使用者可選取之物件的遮罩影像，這些樣式便可派上用場。 例如，您可以使用 **I ... \_ BLEND50** 樣式，在使用者選取影像時繪製影像。

Nonmasked 映射會使用 SRCCOPY 點陣運算複製到目的地裝置內容。 不論裝置內容的背景色彩為何，影像色彩都與之相同。 在 [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 中指定的繪圖樣式也不會影響 nonmasked 影像的外觀。

## <a name="dragging-images"></a>拖曳影像

WIN32 API 包含在螢幕上拖曳影像的功能。 拖曳函式平滑且沒有游標閃爍地移動彩色影像。 遮罩影像和未遮罩影像都可以拖曳。

[**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)函式會開始拖曳作業。 這些參數包括影像清單的控制碼、要拖曳的影像索引，以及影像內的作用點位置。 作用點是拖曳函式辨認為影像的實際螢幕位置的單一像素。 一般而言，應用程式設定作用點，以便使其與滑鼠游標的作用點相符。 [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove)函式會將影像移至新的位置。

[**ImageList \_ system.windows.dragdrop.dragenter>**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter)函式會設定在視窗內拖曳影像的初始位置，並在該位置繪製影像。 這些參數包含視窗的控制碼，可在其中繪製影像以及視窗內初始位置的座標。 座標是相對於視窗左上角，而非工作區。 將座標視為參數的所有影像拖曳函式也是如此。 這表示當指定座標時，您必須補償視窗元素的寬度，例如框線、標題列和功能表列。 如果您在呼叫 **ImageList \_ system.windows.dragdrop.dragenter>** 時指定 **Null** 視窗控制碼，則拖曳函式會在與桌面視窗相關聯的裝置內容中繪製影像，而座標則是相對於畫面的左上角。

[**ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage)函式會藉由結合指定的影像， (通常是使用目前拖曳影像) 的滑鼠游標影像，來建立新的拖曳影像。 因為拖曳函式會在拖曳作業期間使用新的影像，所以您應該使用 [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) 函式在呼叫 **ImageList \_ SetDragCursorImage** 之後隱藏實際的滑鼠游標。 否則，系統可能會在拖曳作業期間出現兩個滑鼠游標。

當應用程式呼叫 [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag)時，系統會建立暫時性的內部影像清單，然後將指定的拖曳影像複製到內部清單。 您可以使用 [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) 函式取出暫存拖曳影像清單的控制碼。 函式也會擷取目前拖曳位置以及拖曳影像相對於拖曳位置的位移。

## <a name="image-information"></a>影像資訊

有一些函數可從影像清單中取出資訊。 [**ImageList \_ GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo)函式會以單一影像的相關資訊填入 [**IMAGEINFO**](/windows/desktop/api)結構，包括影像和遮罩點陣圖的控制碼、色彩平面的數目和每圖元的位數，以及影像點陣圖內影像的周框。 您可以使用此項資訊直接操作影像的點陣圖。 [**ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount)函式會捕獲影像清單中的影像數目。

## <a name="image-overlays"></a>影像覆蓋

每個影像清單都包含用來做為重迭的索引清單。 覆迭是以透明方式繪製在另一個影像上的影像。 目前在影像清單中的任何影像都可以用來做為重迭。 您最多可以為每個影像清單指定四個重迭。 在4.71 版中，此限制已擴充為15。

您可以使用 [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 函式、指定影像清單的控制碼、現有影像的索引，以及所需的重迭索引，將影像的索引加入至重迭清單。 如此一來，就會向影像清單指出 "index *x* 上的影像可作為重迭，而我想要將覆迭當做重迭索引 *y* 參考。" 覆迭索引是以1為基礎，而不是以零為起始，因為覆迭索引為零表示不會使用任何覆迭。

使用 [**imagelist \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) 或 [**imagelist \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) 函式繪製影像時，您會指定覆迭。 覆迭的指定方式是在所需的繪圖旗標和 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)宏的結果之間執行邏輯 **OR** 運算。 **INDEXTOOVERLAYMASK** 宏會接受覆迭索引，並將其格式化以包含這些函式的旗標。 這會繪製具有指定覆迭的影像。 下列範例示範如何在繪製影像時新增和指定重迭。


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



這會繪製影像1，然後以影像0覆迭影像。 因為3是您在 [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 呼叫中指定的重迭索引，所以會在 [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) 宏中放置3。

## <a name="32-bit-antialiased-icons"></a>32位反鋸齒圖示

消除鋸齒是一種柔化或模糊邊緣的技巧。 這可提供影像更自然的外觀。 Windows Vista 和 Windows 7 中的影像清單支援使用32位的反鋸齒圖示和點陣圖。 色彩值使用24位，而8個位則是用來作為圖示上的 Alpha 色板。 若要建立可處理每圖元32位 (bpp) 映射的影像清單，請呼叫 [**ImageList \_ create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) 函式，並傳入 ilc.out \_ COLOR32 旗標。

若要正確撰寫32位的圖示，您必須為每個圖示建立多個影像，如下圖所示。

![圖例顯示三個色彩深度的三個圖示大小](images/theme2.png)

-   前三個影像處於16色模式，可在安全模式中使用。
-   接下來的三個圖示會在256色彩模式下使用。
-   最後三個圖示具有 Alpha 色板，而且只能在執行24位或更高版本的作業系統中使用。
-   圖示格式的影像順序並不重要。 如果順序錯誤，則在解壓縮圖示時，較舊的 Windows 版本功能會不佳。 不正確地將圖示解壓縮可能會導致記憶體損毀和轉譯不當。
-   舊版 Windows 有10個圖示的資源限制。

> [!Note]  
> 您可以使用協力廠商工具來產生包含 Alpha 色板的圖示檔和點陣圖。 如果您使用 [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) 載入包含 Alpha 的 32 bpp 點陣圖，您需要指定 LR \_ CREATEDIBSECTION 旗標。

 

 

 
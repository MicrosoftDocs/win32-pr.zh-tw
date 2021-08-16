---
description: 使用 GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: 使用 GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f12dd613339680ac22352f4538b7029d8c9cea213c55f66e1986a8d32d0a68ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072148"
---
# <a name="using-graphedit"></a>使用 GraphEdit

GraphEdit 可在 Microsoft Windows 軟體開發套件 (SDK)  () 中取得 <https://go.microsoft.com/fwlink/p/?linkid=62332> 。

GraphEdit 應用程式的名稱為 "graphedt.exe"。 安裝 SDK 之後，"graphedt.exe" 位於下列目錄： \[ Program Files \] \\ Microsoft sdk \\ Windows \\ \[ \] \\ Bin 版 \\ 。

執行 GraphEdit 之前，請使用 regsvr32 公用程式來註冊下列位於相同目錄中的 Dll：

-   proppage.dll
-   evrprop.dll

這些 dll 可讓 GraphEdit 顯示某些內建 DirectShow 篩選準則的屬性頁。

## <a name="build-a-file-playback-graph"></a>建立檔案播放 Graph

GraphEdit 可以建立檔案播放的篩選圖形。 這項功能相當於在應用程式中呼叫 [**IGraphBuilder：： RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) 方法。 **在 [檔案**] 功能表中，按一下 [轉譯 **媒體** 檔案]。 GraphEdit 會顯示 [ **開啟** 檔案] 對話方塊。 選取多媒體檔案，然後按一下 [ **開啟**]。 GraphEdit 會建立一個篩選圖形來播放您所選取的檔案。

您也可以轉譯位於 URL 的媒體檔案。 **在 [檔案**] 功能表中，按一下 [轉譯 **URL**]。 GraphEdit 會顯示對話方塊，以在其中輸入 URL。

## <a name="build-a-filter-graph"></a>建立篩選 Graph

GraphEdit 可以使用您系統上註冊的任何篩選器來建立自訂篩選圖形。 在 [ **Graph** ] 功能表中，按一下 [**插入篩選**]。 隨即出現一個對話方塊，內含您系統上的篩選器清單，依篩選分類進行組織。 GraphEdit 會從登錄中的資訊建立此清單。 下圖顯示對話方塊。

![您要插入哪些篩選準則？](images/gedit12.png)

若要將篩選新增至圖形，請選取篩選的名稱，然後按一下 [ **插入篩選** ] 按鈕，或按兩下篩選名稱。 加入篩選之後，您可以將滑鼠從某個篩選的輸出圖釘拖曳至另一個篩選的輸入圖釘，以連接兩個篩選器。 如果 pin 接受連線，GraphEdit 會繪製箭號來連接它們。

![連接兩個篩選](images/gedit-connect.png)

## <a name="run-the-graph"></a>執行 Graph

當您在 Graph 編輯中建立篩選圖形後，就可以執行圖形來查看它是否如預期般運作。 [ **Graph** ] 功能表包含 [**播放**]、[**暫停**] 和 [**停止**] 功能表命令。 這些命令會分別叫用 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 方法，分別 [**執行**](/windows/desktop/api/Control/nf-control-imediacontrol-run)、 [**暫停**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)和 [**停止**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。 GraphEdit 工具列也有這些命令的按鈕：

![[暫停]、[播放] 和 [停止] 按鈕](images/gedit-toolbar.png)

> [!Note]  
> GraphEdit **Stop** 命令會先暫停圖形並搜尋時間零 (假設圖形是可搜尋的) 。 針對檔案播放，此動作會將影片視窗重設為第一個畫面格。 然後，GraphEdit 會呼叫 [**IMediaControl：： Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)。

 

如果圖表是可搜尋的，您可以拖曳出現在工具列下方的滑動軸來進行搜尋。 拖曳滑杆列會叫用 [**IMediaSeeking：： SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) 方法。

## <a name="view-property-pages"></a>視圖屬性頁

某些篩選準則支援自訂屬性頁，可提供使用者介面來設定篩選準則的屬性。 若要在 GraphEdit 中查看篩選的屬性頁，請以滑鼠右鍵按一下篩選器，然後從快顯視窗中選取 [ **屬性** ]。 GraphEdit 會顯示內容頁，其中包含篩選 (所定義的屬性工作表（如果有任何) ）。 此外，GraphEdit 還包含篩選上每個釘選的屬性工作表。 釘選屬性工作表是由 GraphEdit 定義，而不是由篩選所定義。 如果連接釘選，[釘選] 屬性工作表會顯示連線的媒體類型。 否則，它會列出釘選的慣用媒體類型。

> [!Note]  
> 若要使用 GraphEdit 的內建屬性頁，您必須註冊 proppage.dll。 此 DLL 可在 Windows SDK 中使用。 DLL 也包含某些 DirectShow 篩選準則的其他屬性頁。 這些屬性頁僅供進行偵錯工具之用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 GraphEdit 模擬 Graph 建立](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 




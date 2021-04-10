---
title: 硬體繪圖功能
description: 硬體繪圖功能
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、繪圖
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) ，繪圖
- ICGetInfo 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021549"
---
# <a name="hardware-drawing-capabilities"></a>硬體繪圖功能

某些轉譯器可以在將影片畫面解壓縮時，直接繪製到影片硬體。 這些轉譯器會傳回 VIDCF \_ DRAW 旗標以回應 [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) 函數。 使用這種類型的轉譯器時，您的應用程式不需要處理解壓縮的資料。 它可讓轉譯器保留解壓縮的資料以供繪製。

如果您的應用程式使用具有繪製功能的轉譯器，它必須處理下列工作：

-   選取轉譯器。
-   指定影像格式。
-   初始化轉譯器。
-   繪製資料。
-   控制繪圖參數。

## <a name="renderer-selection"></a>轉譯器選取專案

[**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)宏會開啟轉譯器，以使用指定的格式繪製影像。 如果成功，則會傳回轉譯器的控制碼; 否則會傳回零。 此宏會使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 函式來開啟轉譯器。

## <a name="specifying-image-formats"></a>指定影像格式

因為您的應用程式不需要繪製解壓縮的資料，所以不需要特定的輸出格式。 但是，它必須確保轉譯器可以使用輸入格式來繪製，方法是使用 [**ICM \_ draw \_ 查詢**](icm-draw-query.md) 訊息 (或使用 [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) 宏) 。 此訊息無法判斷轉譯器是否可以繪製點陣圖。 如果您的應用程式必須判斷轉譯器是否可以繪製點陣圖，請使用此訊息搭配 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 函數。

您的應用程式可以使用 [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) 函式，讓轉譯器建議輸入格式。 當轉譯器將繪圖功能與解壓縮功能分開時，會使用此函式。 大部分使用繪圖函式的應用程式都不需要決定輸出格式。

## <a name="renderer-initialization"></a>轉譯器初始化

[**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin)函式會初始化轉譯器，並將其告知繪圖目的地。 此函式也可以執行下列工作：

-   判斷轉譯器是否支援特定輸入格式。
-   指定繪圖作業是否佔用視窗或整個畫面。
-   使用來源矩形來指定要顯示的影像部分。
-   定義影像順序的播放速率。

某些轉譯器會緩衝處理壓縮的資料，以便更有效率地運作。 您的應用程式可以傳送 [**ICM \_ GETBUFFERSWANTED**](icm-getbufferswanted.md) 訊息 (或使用 [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) 宏) 來判斷轉譯器要求的緩衝區數目。 您的應用程式應該預先載入這些緩衝區，並在繪製之前將它們傳送至轉譯器。

## <a name="drawing-the-data"></a>繪製資料

您可以使用 [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) 函數將資料解壓縮以進行繪製。 但是，在您的應用程式傳送 [**ICM \_ DRAW \_ 開始**](icm-draw-start.md) 訊息 (或使用 [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) 宏) 之前，轉譯器不會開始繪製資料。 當您的應用程式呼叫這個函式時，轉譯器會開始依 *dwRate* 參數所指定的速率除以 *dwScale* 參數來繪製框架;當應用程式使用 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 函式初始化轉譯器時，會提供這些參數。 繪圖會繼續進行，直到您的應用程式傳送 [**ICM \_ DRAW \_ 停止**](icm-draw-stop.md) 訊息 (或使用 [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) 宏) 。

> [!Note]  
> 如果轉譯器在繪圖之前緩衝資料，您的應用程式就不應該使用 **ICDrawStart** 宏，直到傳送轉譯器針對 **ICGetBuffersWanted** 宏傳回的框架數為止。

 

[**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw)的 *lTime* 參數會指定繪製框架的時間。 轉譯器會將這個整數除以以 [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) 指定的時間範圍，以取得實際時間。 **ICDraw** 函數的時間相對於 **ICDrawStart**。 **ICDrawStart** 會將時鐘設定為零。 例如，如果您的應用程式針對 *lTime* 的時間刻度和75指定1000，則轉譯器會將畫面格75毫秒繪製到序列中。

## <a name="controlling-drawing-parameters"></a>控制繪圖參數

您可以藉由傳送 [**icm \_ draw \_ GETTIME**](icm-draw-gettime.md) 訊息 (或使用 [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) 宏) 來監視轉譯器的時鐘，也可以設定轉譯器的時鐘，藉由傳送 [**ICM \_ draw \_ SETTIME**](icm-draw-settime.md) 訊息 (或使用 [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) 宏) 來繪製資料。

若要在轉譯器繪製時變更目前的位置，您的應用程式可以傳送 [**ICM \_ 繪製 \_ 視窗**](icm-draw-window.md) 訊息 (或使用 [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) 宏) 來錨定視窗。 當視窗變更時，應用程式通常會使用此訊息。

如果播放視窗取得好用的調色板訊息，則您的應用程式必須傳送 [**ICM \_ DRAW \_ 實現**](icm-draw-realize.md) 訊息 (或使用 [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) 宏) ，讓轉譯器再次發現該調色板以供播放。 應用程式可以藉由傳送 [**icm \_ draw \_ CHANGEPALETTE**](icm-draw-changepalette.md) 訊息 (或使用 [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) 宏) 來變更選擇區，並藉由傳送 [**icm \_ draw \_ GET \_ 調板**](icm-draw-get-palette.md) 訊息來取得目前的調色板。

某些轉譯器必須明確指示，以顯示傳遞給它們的畫面格。 傳送 [**ICM \_ DRAW \_ RENDERBUFFER**](icm-draw-renderbuffer.md) 訊息 (或使用 [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) 宏) 會導致這些轉譯器繪製框架。

 

 





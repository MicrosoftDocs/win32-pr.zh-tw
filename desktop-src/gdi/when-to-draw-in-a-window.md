---
description: 應用程式會在不同的時間繪製視窗：當您在第一次建立視窗時、變更視窗的大小時、將視窗從另一個視窗移至最小化或最大化時、從開啟的檔案顯示資料，以及滾動、變更或選取部分顯示的資料時。
ms.assetid: 4b5d6842-5707-4884-a55a-e09e342cea46
title: 在視窗中繪製的時機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42c8c157de5a591be5ad1a6ad3e319cf83220e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319031"
---
# <a name="when-to-draw-in-a-window"></a>在視窗中繪製的時機

應用程式會在不同的時間繪製視窗：當您在第一次建立視窗時、變更視窗的大小時、將視窗從另一個視窗移至最小化或最大化時、從開啟的檔案顯示資料，以及滾動、變更或選取部分顯示的資料時。

系統會管理動作，例如移動和調整視窗的大小。 如果動作會影響視窗的內容，系統會將視窗中受影響的部分標示為已準備好進行更新，並在下一個機會將 [**WM \_ 油漆**](wm-paint.md) 訊息傳送至視窗的視窗程式。 此訊息是應用程式用來判斷必須更新的內容，以及執行必要繪圖的信號。

某些動作是由應用程式管理，例如顯示開啟的檔案和選取顯示的資料。 針對這些動作，應用程式可以標示為更新受此動作影響的視窗部分，而導致在下一個機會傳送 [**WM \_ 油漆**](wm-paint.md) 訊息。 如果動作需要立即提出意見反應，應用程式可以在動作發生時進行繪製，而不需要等候 **WM \_ 油漆**。 例如，一般應用程式會反白顯示使用者選取的區域，而不是等候下一個 **WM \_ 油漆** 訊息來更新區域。

在所有情況下，應用程式只要建立，就可以在視窗中繪製。 若要在視窗中繪製，應用程式必須先取得視窗的顯示裝置內容控制碼。 在理想的情況下，應用程式會在處理 [**WM \_ 油漆**](wm-paint.md) 訊息時，執行大部分的繪圖作業。 在此情況下，應用程式會藉由呼叫 [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) 函式來抓取顯示裝置內容。 如果應用程式在任何其他時間（例如從 [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) 內或在鍵盤或滑鼠訊息的處理期間）繪製，則會呼叫 [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) 或 [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) 函式來取出顯示 DC。

 

 

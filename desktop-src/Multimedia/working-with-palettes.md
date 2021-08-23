---
title: 使用調色板
description: 使用調色板
ms.assetid: 0ad0d78b-4c2c-499c-ad5e-8324b59e89fc
keywords:
- WM_CAP_PAL_PASTE 訊息
- capPalettePaste 宏
- WM_CAP_PAL_OPEN 訊息
- capPaletteOpen 宏
- WM_CAP_PAL_AUTOCREATE 訊息
- capPaletteAuto 宏
- WM_CAP_PAL_MANUALCREATE 訊息
- capPaletteManual 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51f9399520b5a3cefc046959c0d59d7abe9d0f1b6ab19662f750720afd16447
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686708"
---
# <a name="working-with-palettes"></a>使用調色板

一開始，如果影片拍攝格式需要調色板，則 [捕獲] 視窗會使用 capture 驅動程式所提供的調色板。 這個調色板可能包含黑白重制的灰色縮放值，或廣泛的色彩值選取。 您可以使用 [ [**wm \_ cap \_ pal \_ 貼**](wm-cap-pal-paste.md) 上] 或 [ [**wm \_ cap \_ pal \_ 開啟**](wm-cap-pal-open.md) 訊息 (] 或 [ [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) 或 [**capPaletteOpen**](/windows/desktop/api/Vfw/nf-vfw-cappaletteopen) 宏]) ，來取出現有的調色板來取代預設的調色板。 或者，您也可以建立自訂調色盤來取代預設的調色板，方法是使用 [**WM \_ cap \_ pal \_**](wm-cap-pal-autocreate.md) 自動建立或 [**WM \_ cap \_ pal \_ MANUALCREATE**](wm-cap-pal-manualcreate.md) message (或 [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) 或 [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) 宏) 。 取代預設的調色板之後，[捕獲] 視窗和驅動程式會使用取代的調色板，直到您建立或開啟另一個調色板為止。

WM \_ cap pal 自動建立 \_ \_ 或 WM \_ cap \_ pal \_ MANUALCREATE 訊息會根據目前的影片輸入建立優化的調色板。 此自訂調色盤提供最佳色彩精確度的影片順序，因為它是以存在於序列中的色彩為基礎。 [Capture （capture）] 視窗會建立其範例色彩的三維長條圖。 它會藉由檢查相鄰色彩之間的絕對誤差，並以最小誤差值進行合併，來減少色彩數目。

當您自動加入 WM \_ CAP \_ PAL 時 \_ ，您必須指定 AVICap 至範例的框架數目，並指定色調色板的大小。 指定畫面格數目時，請包含足夠的畫面格，以確保會取樣序列中的所有色彩。

您可以使用 WM \_ CAP PAL MANUALCREATE 來取樣目前的畫面格 \_ \_ 。 藉由使用此訊息搭配數個手動選取的畫面格，您可以建立包含您想要在調色板中顯示之色彩的調色板。

一個調色板最多可包含256的色彩。 如果您合併調色板或影片序列要同時與其他影片或影像一起顯示，您應該使用較小的色彩選取範圍，讓每個影像或影片剪輯的色彩可以並存。

您可以使用 [**wm \_ cap \_ pal 的 \_ Save**](wm-cap-pal-save.md) message (或 [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) 宏) 來儲存新的調色板，並在稍後使用 [**wm \_ cap \_ pal \_ 開啟**](wm-cap-pal-open.md) 的訊息來取得它。 您可以儲存調色板以進行後置處理，或在另一個應用程式中使用。

您可以使用 [**WM \_ CAP \_ PAL \_ 貼**](wm-cap-pal-paste.md) 上訊息，將 [剪貼簿] 從 [剪貼簿] 貼到 [捕獲] 視窗。 [捕獲] 視窗會將此選擇區傳送至 capture 驅動程式。 其他應用程式可以將調色板複製到剪貼簿。 您也可以使用 [ [**WM \_ CAP \_ 編輯 \_ 複製**](wm-cap-edit-copy.md) 訊息 (] 或 [ [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) 宏) ，將調色板複製到剪貼簿。 此訊息會將影片框架緩衝區（包括調色板）複製到剪貼簿。

 

 





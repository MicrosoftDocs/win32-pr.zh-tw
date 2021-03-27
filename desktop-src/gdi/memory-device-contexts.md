---
description: 若要讓應用程式將輸出放在記憶體中，而不是將輸出傳送至實際裝置，請使用特殊的裝置內容進行點陣圖作業，稱為記憶體裝置內容。
ms.assetid: 0a682dc4-31a4-43c8-b0b1-ab01986b1dac
title: 記憶體裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095de04fdf965a87011895015ad7ea6c9782e286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691868"
---
# <a name="memory-device-contexts"></a>記憶體裝置內容

若要讓應用程式將輸出放在記憶體中，而不是將輸出傳送至實際裝置，請使用特殊的裝置內容進行點陣圖作業，稱為 *記憶體裝置內容*。 記憶體 DC 可讓系統將部分的記憶體視為虛擬裝置。 它是記憶體中的位陣列，應用程式可以暫時使用它來儲存在一般繪圖介面上建立之點陣圖的色彩資料。 由於點陣圖與裝置相容，因此記憶體 DC 有時也稱為 *相容的裝置內容*。

記憶體 DC 會儲存特定裝置的點陣圖影像。 應用程式可以藉由呼叫 [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) 函數來建立記憶體 DC。

記憶體 DC 中的原始點陣圖只是預留位置。 其維度是一個圖元到一個圖元。 在應用程式開始繪圖之前，必須藉由呼叫 [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) 函式，在 DC 中選取具有適當寬度和高度的點陣圖。 若要建立適當維度的點陣圖，請使用 [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)、 [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)或 [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) 函數。 將點陣圖選取到記憶體 DC 之後，系統會以夠大的陣列來取代單一位陣列，以儲存指定之圖元矩形的色彩資訊。

當應用程式將 [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc) 傳回的控制碼傳遞給其中一個繪圖函式時，要求的輸出不會出現在裝置的繪圖介面上。 相反地，系統會將結果行、曲線、文字或區域的色彩資訊儲存在位的陣列中。 應用程式可以藉由呼叫 [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) 函式，將記憶體 DC 識別為來源裝置內容，並將視窗或螢幕 DC 作為目標裝置內容，將儲存在記憶體中的影像複製回繪圖介面上。

顯示從調色板裝置上的 DIB 建立的 DIB 或 DDB 時，您可以藉由排列邏輯調色板以符合系統元件的配置，來改善繪製影像的速度。 若要這樣做，請使用 NUMRESERVED 值呼叫 [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) ，以取得系統中的保留色彩數目。 然後呼叫 [**GetSystemPaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getsystempaletteentries) ，並在邏輯調色板的第一個和最後一個 NUMRESERVED/2 專案中填入對應的系統色彩。 例如，如果 NUMRESERVED 是20，您就會在邏輯調色板的第一個和最後10個專案中填入系統色彩。 然後，在我們的範例中，填妥 (邏輯調色板的其餘 256-NUMRESERVED 色彩，其餘236色彩) 具有來自 DIB 的色彩，並設定 \_ 每個色彩的電腦 NOCOLLAPSE 旗標。

如需色彩和調色板的詳細資訊，請參閱 [色彩](colors.md)。 如需點陣圖和點陣圖作業的詳細資訊，請參閱 [點陣圖](bitmaps.md)。

 

 




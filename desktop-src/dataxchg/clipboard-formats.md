---
title: 剪貼簿格式
description: 視窗可以在剪貼簿上放置一個以上的物件，每個物件都代表不同剪貼簿格式的相同資訊。 使用者不需要留意剪貼簿上物件所使用的剪貼簿格式。
ms.assetid: fe42baec-6b00-4816-b379-7f335da8a197
keywords:
- 剪貼簿，格式
- 剪貼簿、windows
- 剪貼簿，標準格式
- 剪貼簿，已註冊的格式
- 剪貼簿，合成格式
- 標準剪貼簿格式
- 已註冊的剪貼簿格式
- 合成的剪貼簿格式
- 雲端剪貼簿格式
- 剪貼簿歷程記錄格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac6bd2dc9dda8c8ccecd164123af68865005d9d28d328ce5489abf23926113ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991338"
---
# <a name="clipboard-formats"></a>剪貼簿格式

視窗可以在剪貼簿上放置一個以上的物件，每個物件都代表不同剪貼簿格式的相同資訊。 使用者不需要留意剪貼簿上物件所使用的剪貼簿格式。

下列主題描述剪貼簿格式。

-   [標準剪貼簿格式](#standard-clipboard-formats)
-   [已註冊的剪貼簿格式](#registered-clipboard-formats)
-   [私用剪貼簿格式](#private-clipboard-formats)
-   [多個剪貼簿格式](#multiple-clipboard-formats)
-   [合成的剪貼簿格式](#synthesized-clipboard-formats)
-   [雲端剪貼簿和剪貼簿歷程記錄格式](#cloud-clipboard-and-clipboard-history-formats)

## <a name="standard-clipboard-formats"></a>標準剪貼簿格式

系統定義的剪貼簿格式稱為 *標準剪貼簿格式*。 這些剪貼簿格式會以 [**標準剪貼簿格式**](standard-clipboard-formats.md)描述。

## <a name="registered-clipboard-formats"></a>已註冊的剪貼簿格式

許多應用程式會使用無法轉譯成標準剪貼簿格式的資料，而不會遺失資訊。 這些應用程式可以建立自己的剪貼簿格式。 應用程式所定義的剪貼簿格式，稱為 [已註冊的剪貼簿格式](#registered-clipboard-formats)。 例如，如果文字處理應用程式使用標準文字格式將格式化的文字複製到剪貼簿，則會遺失格式化資訊。 解決方案是註冊新的剪貼簿格式，例如 rtf)  (rtf 格式。

若要註冊新的剪貼簿格式，請使用 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函數。 此函式會採用格式的名稱，並傳回不帶正負號的整數值，表示已註冊的剪貼簿格式。 若要取出已註冊之剪貼簿格式的名稱，請將不帶正負號的整數值傳遞給 [**GetClipboardFormatName**](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea) 函式。

如果有一個以上的應用程式使用完全相同的名稱來註冊剪貼簿格式，剪貼簿格式只會註冊一次。 對 [**RegisterClipboardFormat**](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata) 函數的兩個呼叫都會傳回相同的值。 如此一來，兩個不同的應用程式就可以使用已註冊的剪貼簿格式來共用資料。

## <a name="private-clipboard-formats"></a>私用剪貼簿格式

應用程式可以藉由定義範圍 **cf \_ PRI加值稅EFIRST** 到 **cf \_ PRI加值稅ELAST** 的值，來識別私用剪貼簿格式。 應用程式可以針對不需要向系統註冊的應用程式定義資料格式，使用私用剪貼簿格式。

系統不會自動釋放與私人剪貼簿格式相關聯的資料控制碼。 如果您的 windows 使用私用剪貼簿格式，您可以使用 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息來釋放任何不再需要的相關資源。

如需有關 [**WM \_ DESTROYCLIPBOARD**](wm-destroyclipboard.md) 訊息的詳細資訊，請參閱 [剪貼簿擁有權](clipboard-operations.md)。

應用程式可以藉由在 **cf \_ GDIOBJFIRST** 到 **cf \_ GDIOBJLAST** 的範圍中定義私用格式，將資料控點放置在剪貼簿上。 使用這個範圍中的值時，資料處理程式不是 Windows 圖形裝置介面 (GDI) 物件的控制碼，而是 [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc)函式所配置的控制碼與 GMEM \_ 可移動旗標。 當剪貼簿清空時，系統會使用 [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) 函式自動刪除物件。

## <a name="multiple-clipboard-formats"></a>多個剪貼簿格式

視窗可以在剪貼簿上放置一個以上的剪貼簿物件，每個物件都代表不同剪貼簿格式的相同資訊。 將資訊放在剪貼簿上時，視窗應該盡可能提供最多格式的資料。 若要瞭解目前在剪貼簿上使用多少種格式，請呼叫 [**CountClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats) 函數。

包含最多資訊的剪貼簿格式應先放在剪貼簿上，後面接著較不具描述性的格式。 從剪貼簿貼上資訊的視窗，通常會以它所辨識的第一種格式抓取剪貼簿物件。 由於剪貼簿格式是依放置在剪貼簿上的順序來列舉，因此第一次辨識的格式也是最具描述性的格式。

例如，假設使用者從文字處理檔案複製了樣式的文字。 包含檔的視窗可能會先以註冊的格式（例如 RTF）將資料放在剪貼簿上。 接著，視窗會以較不描述性的格式將資料放在剪貼簿上，例如文字 (**CF \_ 文字**) 。

當剪貼簿的內容貼到另一個視窗時，此視窗會以其辨識的最具描述性格式抓取資料。 如果視窗辨識 RTF，對應的資料就會貼入檔中。 否則會將文字資料貼到檔中，並遺失格式化資訊。

## <a name="synthesized-clipboard-formats"></a>合成的剪貼簿格式

系統會以隱含方式在特定剪貼簿格式之間轉換資料：如果視窗要求非剪貼簿格式的資料，系統會將可用格式轉換成所要求的格式。 系統可以轉換如下表所示的資料。



| 剪貼簿格式     | 轉換格式    |
|----------------------|----------------------|
| **CF \_ 點陣圖**       | **CF \_ DIB**          |
| **CF \_ 點陣圖**       | **CF \_ DIBV5**        |
| **CF \_ DIB**          | **CF \_ 點陣圖**       |
| **CF \_ DIB**          | **CF \_ 調色板**      |
| **CF \_ DIB**          | **CF \_ DIBV5**        |
| **CF \_ DIBV5**        | **CF \_ 點陣圖**       |
| **CF \_ DIBV5**        | **CF \_ DIB**          |
| **CF \_ DIBV5**        | **CF \_ 調色板**      |
| **CF \_ ENHMETAFILE**  | **CF \_ METAFILEPICT** |
| **CF \_ METAFILEPICT** | **CF \_ ENHMETAFILE**  |
| **CF \_ OEMTEXT**      | **CF \_ 文字**         |
| **CF \_ OEMTEXT**      | **CF \_ UNICODETEXT**  |
| **CF \_ 文字**         | **CF \_ OEMTEXT**      |
| **CF \_ 文字**         | **CF \_ UNICODETEXT**  |
| **CF \_ UNICODETEXT**  | **CF \_ OEMTEXT**      |
| **CF \_ UNICODETEXT**  | **CF \_ 文字**         |



 

如果系統針對特定的剪貼簿格式提供自動類型轉換，則將轉換格式 (s) 在剪貼簿上沒有任何優點。

如果系統針對特定的剪貼簿格式提供自動類型轉換，而且您呼叫 [**EnumClipboardFormats**](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats) 來列舉剪貼簿資料格式，系統會先列舉剪貼簿上的格式，後面接著可以轉換成的格式。

複製點陣圖時，最好將 **cf \_ .Dib** 或 **cf \_ DIBV5** 格式放置在剪貼簿上。 這是因為裝置相關點陣圖中的色彩 (**CF \_ 點陣圖**) 相對於系統選擇區（可能會在貼上點陣圖之前變更）。 如果 **CF \_ DIB** 或 **cf \_ DIBV5** 格式位於剪貼簿，而視窗要求 **CF \_ 點陣圖** 格式，則系統會在該時間使用目前的調色板，轉譯與裝置無關的點陣圖 (DIB) 。

如果您將 **cf \_ 點陣圖** 格式放在剪貼簿上 (而不是 **cf \_ DIB**) ，則系統會在關閉剪貼簿時立即呈現 **cf \_ dib** 或 **cf \_ DIBV5** 剪貼簿格式。 這可確保使用正確的調色板來產生 DIB。 如果您使用剪貼簿中的點陣圖色彩空間資訊來放置 **CF \_ DIBV5** 格式，則系統會在要求 **cf \_ DIB** 或 **cf \_ DIBV5** 時，將點陣圖的位從點陣圖色彩空間轉換成 sRGB 色彩空間。 如果在剪貼簿中沒有色彩空間資訊時要求 **CF \_ DIBV5** ，系統會在 [**BITMAPV5HEADER**](/windows/desktop/api/wingdi/ns-wingdi-bitmapv5header) 結構中傳回 sRGB 色彩空間資訊。 在需要時，會在其他剪貼簿格式之間進行轉換。

如果剪貼簿包含 **CF \_ 調色板** 格式的資料，應用程式應該使用 [**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette) 和 [**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette) 函式，以針對該邏輯元件來實現剪貼簿中的任何其他資料。

中繼檔有兩種剪貼簿格式： **cf \_ ENHMETAFILE** 和 **cf \_ METAFILEPICT**。 為 Windows 的中繼檔指定 **cf \_ ENHMETAFILE** for 增強的中繼檔和 **cf \_ METAFILEPICT** 。

## <a name="cloud-clipboard-and-clipboard-history-formats"></a>雲端剪貼簿和剪貼簿歷程記錄格式

某些版本的 Windows 包括[雲端剪貼](/windows/whats-new/whats-new-windows-10-version-1809#cloud-clipboard)簿，可保留最近剪貼簿資料項目的歷程記錄，並可在使用者的裝置之間進行同步處理。
如果您不想要將應用程式放在剪貼簿上的資料放在剪貼簿歷程記錄中，或與其他裝置同步處理，則您的應用程式可以藉由將資料放在 Windows 系統已知名稱的特定[已註冊剪貼簿格式](#registered-clipboard-formats)中，來控制這項行為：

- **ExcludeClipboardContentFromMonitorProcessing** ：將任何資料放在剪貼簿上的格式，以防止所有剪貼簿格式包含在剪貼簿歷程記錄中，或同步處理到使用者的其他裝置。
- **CanIncludeInClipboardHistory** ：使用此格式將序列化的 **[DWORD](../WinProg/windows-data-types.md)** 值設為零，以防止所有剪貼簿格式包含在剪貼簿歷程記錄中，或將值設為1，以明確要求剪貼簿專案包含在剪貼簿歷程記錄中。 這不會影響與使用者其他裝置的同步處理。
- **CanUploadToCloudClipboard** ：使用此格式將序列化的 **[DWORD](../WinProg/windows-data-types.md)** 值設為零，以防止所有剪貼簿格式同步處理到使用者的其他裝置，或將剪貼簿的值改為明確要求將剪貼簿專案同步處理到其他裝置。 這不會影響本機裝置的剪貼簿歷程記錄。

如同其他已註冊的剪貼簿格式，您將需要使用 [**RegisterClipboardFormat**](
/windows/win32/api/winuser/nf-winuser-registerclipboardformata) 函式來取得可識別上述3種格式的不帶正負號的整數值。
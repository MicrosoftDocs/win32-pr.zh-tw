---
description: 點陣圖標頭類型
ms.assetid: 6df4655a-f707-4893-b6e6-f7e4d7f67b4e
title: 點陣圖標頭類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5910b0fb5be1166e807db1f3362186a206abc2b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848576"
---
# <a name="bitmap-header-types"></a>點陣圖標頭類型

點陣圖有四個基本的標頭類型：

-   [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)
-   [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))
-   [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)
-   [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)

點陣圖標頭的四種類型會以 **大小** 成員來區分，也就是每個結構中的第一個 **DWORD** 。

[**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)結構是延伸的 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)結構，也就是延伸的 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))結構。 不過， **BITMAPINFOHEADER** 和 [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) 只有與其他點陣圖標頭結構共通的 **大小** 成員。

[**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)和 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)格式分別由 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))和 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header)格式取代。 提供 **BITMAPCOREHEADER** 和 **BITMAPV4HEADER** 格式，以提供完整性和回溯相容性。

DIB 的格式如下 (如需詳細資訊，請參閱 [點陣圖儲存體](bitmap-storage.md) ) ：

-   [**BITMAPFILEHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapfileheader)結構
-   可能是 [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader)、 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)或 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) 結構。
-   選擇性的色彩表，也就是一組 [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) 結構或一組 [**RGBTRIPLE**](/windows/win32/api/wingdi/ns-wingdi-rgbtriple) 結構。
-   點陣圖資料
-   選用的設定檔資料

色彩表描述圖元值如何對應至 RGB 色彩值。 RGB 是一種模型，用來描述發出光線所產生的色彩。

*設定檔資料* 指的是設定檔名稱 (連結設定檔) 或實際的設定檔位 (內嵌設定檔) 。 檔案格式會將設定檔資料放在檔案的結尾。 設定檔資料會放在色彩表 (（如果有) 的話）的正上方。 但是，如果函式收到封裝的 DIB，則設定檔資料會出現在點陣圖位之後，例如檔案格式。

設定檔資料只會存在於 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) 結構，其中 **BV5CSTYPE** 是設定檔 \_ 連結或設定檔 \_ 內嵌。 針對接收已封裝 Dib 的函式，設定檔資料會出現在點陣圖資料之後。

調色盤裝置是使用調色板指派色彩的任何裝置。 調色盤裝置的典型範例是以8位色彩深度執行的顯示 (也就是256色彩) 。 此模式中的顯示會使用小型色彩表將色彩指派給點陣圖。 點陣圖中的色彩會指派給裝置所使用之調色板中最接近的色彩。 調色盤裝置不會建立最佳的調色板來顯示點陣圖;它只會使用目前調色板中的任何內容。 應用程式會負責建立調色板，並將其選取到系統中。 一般情況下，每圖元 16-、24-和32位 (bpp) 點陣圖不包含色彩表 (也稱為 點陣圖) 的最佳調色板;在此情況下，應用程式會負責產生最佳的調色板。 不過，16-、24和 32-bpp 點陣圖可以包含這類適合在調色盤裝置上顯示的最佳色彩表;在此情況下，應用程式只需要根據點陣圖檔案中顯示的色彩表來建立調色板。

1、4或 8 bpp 的點陣圖必須有色彩表，而且大小上限是以 bpp 為基礎。 1、4和 8 bpp 點陣圖的大小上限為2到 bpp 的威力。 因此，1 bpp 點陣圖最多有兩個色彩，4 bpp 點陣圖最多16個色彩，而 8 bpp 點陣圖最多為256個色彩。

16、24或 32-bpp 的點陣圖不需要色彩表，但可能會讓它們指定調色盤裝置的色彩。 如果有適用于16、24或 32-bpp 點陣圖的色彩表， **biClrUsed** 成員會指定色彩資料表的大小，而色彩資料表在其中必須有許多色彩。 如果 **biClrUsed** 為零，則不會有色彩表。

BI 位點陣圖的 red、綠和 blue 等位遮罩會 \_ 立即遵循 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))、 [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header)和 [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) 結構。 **BITMAPV4HEADER** 和 **BITMAPV5HEADER** 結構包含紅色、綠色和藍色遮罩的其他成員，如下所示。



| 成員        | 意義                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------|
| **RedMask**   | 指定每個圖元之紅色元件的色彩遮罩，只有當 **壓縮** 成員設為 BI 位欄位時才有效 \_ 。   |
| **GreenMask** | 指定每個圖元綠色元件的色彩遮罩，只有當 **壓縮** 成員設為 BI 位欄位時才有效 \_ 。 |
| **BlueMask**  | 指定每個圖元藍色元件的色彩遮罩，只有當 **壓縮** 成員設為 BI 位欄位時才有效 \_ 。  |



 

當 [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))的 **biCompression** 成員設定為 BI 位欄位， \_ 且函式收到 **LPBITMAPINFO** 類型的引數時，色彩遮罩會緊接在標頭後面。 色彩表（如果有的話）會遵循色彩遮罩。 [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) 點陣圖不支援色遮罩。

依預設，點陣圖資料的格式為下而下。 下一步表示點陣圖資料中的第一個掃描行是要顯示的最後一個掃描行。 例如，10圖元 x 10 圖元點陣圖之點陣圖資料<sup>第</sup>0 個掃描行的<sup>第0個圖元，</sup>將是顯示或列印影像的<sup>第9個</sup>掃描行的<sup>第</sup>0 個圖元。 執行長度編碼 (RLE) 格式點陣圖和 [**BITMAPCOREHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapcoreheader) 點陣圖不可以是由上而下的點陣圖。 掃描行是 **DWORD** 對齊的，但以 RLE 壓縮的點陣圖除外。 它們必須以位元組為單位填補，以位元組為單位，但不能平均整除四個，但不包括 RLE 壓縮點陣圖。 例如，10 x 10 圖元 24 bpp 點陣圖在每個掃描行的結尾都有兩個填補位元組。

 

 

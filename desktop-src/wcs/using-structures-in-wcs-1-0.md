---
title: 在 WCS 1.0 中使用結構
description: WCS 1.0 所使用的大部分結構非常簡單，只需要一點說明。 這些檔記載于有權參考結構的 WCS 1.0 參考區段中。
ms.assetid: 8d3682e2-38fd-4a33-b386-ab0716bb6972
keywords:
- Windows Color System (WCS) ，結構
- WCS (Windows 色彩系統) ，結構
- 影像色彩管理，結構
- 色彩管理，結構
- 色彩，結構
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d6e434ccfa6d96aa815f0c1997dc7f34178a32
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106982158"
---
# <a name="using-structures-in-wcs-10"></a>在 WCS 1.0 中使用結構

WCS 1.0 所使用的大部分結構非常簡單，只需要一點說明。 這些檔記載于有權參考 [結構](structures.md)的 WCS 1.0 參考區段中。

例外狀況是 [**SetupColorMatchingW**](/windows/win32/api/icm/nf-icm-setupcolormatchingw)函數所使用的 [**COLORMATCHSETUPW**](/windows/win32/api/icm/ns-icm-colormatchsetupw)結構，以及 Wingdi 中定義的下列 Windows 結構：

-   [BITMAPV5HEADER](#windows-bitmap-header-structures)
-   [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)
-   [**CIEXYZ**](/windows/desktop/api/Wingdi/ns-wingdi-tagciexyz)
-   [**CIEXYZTRIPLE**](/windows/desktop/api/Wingdi/ns-wingdi-tagicexyztriple)

下列主題會以更高的長度討論：

-   [Windows 點陣圖標頭結構](#windows-bitmap-header-structures)
-   [V4 和 V5 標頭之間的差異](#differences-between-v4-and-v5-headers)
-   [Bitmap.exe：用於轉換點陣圖標頭的 Command-Line 公用程式](#bitmapexe-a-command-line-utility-for-converting-bitmap-headers)

## <a name="windows-bitmap-header-structures"></a>Windows 點陣圖標頭結構

WCS 1.0 允許將 ICC 色彩設定檔連結或內嵌于與裝置無關的點陣圖 (Dib) 。 這可讓 DIB 色彩的特性比在 Windows 95 中使用 WCS 更準確。 [BITMAPV5HEADER](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) 是新的點陣圖標頭結構，在 Windows 98 版本的 Wingdi 中定義。 基於開發目的，這個程式設計人員的參考也包含在 file Icm 中。 **BITMAPV5HEADER** 結構如下所示：


```C++
typedef struct {
    DWORD        bV5Size;
    LONG         bV5Width;
    LONG         bV5Height;
    WORD         bV5Planes;
    WORD         bV5BitCount;
    DWORD        bV5Compression;
    DWORD        bV5SizeImage;
    LONG         bV5XPelsPerMeter;
    LONG         bV5YPelsPerMeter;
    DWORD        bV5ClrUsed;
    DWORD        bV5ClrImportant;
    DWORD        bV5RedMask;
    DWORD        bV5GreenMask;
    DWORD        bV5BlueMask;
    DWORD        bV5AlphaMask;
    DWORD        bV5CSType;
    CIEXYZTRIPLE bV5Endpoints;
    DWORD        bV5GammaRed;
    DWORD        bV5GammaGreen;
    DWORD        bV5GammaBlue;
    DWORD        bV5Intent;         // Rendering intent for bitmap 
    DWORD        bV5ProfileData;    // Offset to profile data 
    DWORD        bV5ProfileSize;    // Size of embedded profile data 
    DWORD        bV5Reserved;       // Should be zero 
} BITMAPV5HEADER, FAR *LPBITMAPV5HEADER, *PBITMAPV5HEADER;
```



成員 **bV5CSType** 可以將值設定檔 \_ 內嵌或設定檔 \_ 連結，以指定設定檔是否內嵌或連結到 DIB。 成員 **bV5ProfileData** 是從 **BITMAPV5HEADER** 結構的開頭到設定檔資料開頭的位移（以位元組為單位）。 如果設定檔是內嵌的，則設定檔資料是實際的設定檔，如果已連結，則設定檔資料是設定檔以 null 終止的檔案名。 這不可以是 Unicode 字串。 它必須以專用於 Windows 字元集的字元來撰寫 (字碼頁 1252) 。

當 DIB 載入記憶體時，設定檔資料 (（如果有的話）) 應該接在 color 資料表之後， **bV5ProfileData** 就應該從 **BITMAPV5HEADER** 結構的開頭提供設定檔資料的位移。 此成員的值現在將會不同，因為點陣圖位不會在記憶體中的色彩表之後。 應用程式應該在將 DIB 載入記憶體之後，修改 **bV5ProfileData** 成員。

針對壓縮的 Dib，設定檔資料應遵循點陣圖位，類似于檔案格式。 **BV5ProfileData** 成員仍應從 **BITMAPV5HEADER** 結構的開頭提供設定檔資料的位移。

只有當 **bV5Size**  ==  **sizeof** ( **BITMAPV5HEADER** ) **ANDbV5CSType** 是設定檔 \_ 內嵌或設定檔連結時，應用程式才應該存取設定檔資料 \_ 。

如果設定檔連結，設定檔的路徑可以是任何完整名稱 (包括可以使用 Win32 **CreateFile** 函數開啟的網路路徑) 。

## <a name="differences-between-v4-and-v5-headers"></a>V4 和 V5 標頭之間的差異

使用新的點陣圖結構時，辨識 **BITMAPV4HEADER** 和 **BITMAPV5HEADER** 結構設定方式的差異會很有用：



| V4 標頭     | 意義                                                                                                                              |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **bV4CSType** | LCS \_ 校正 \_ 的 RGB。 這個值表示會在適當的欄位中提供端點和 gammas。 假值會造成問題。 |
| **bV4CSType** | LCS \_ sRGB。 此值表示點陣圖位於 sRGB 色彩空間 (gammas，且已忽略) 的端點。                                 |
| **bV4CSType** | LCS \_ WINDOWS \_ 色彩 \_ 空間。 此值表示點陣圖在 Windows 預設色彩空間中。                                    |



 



| V5 標頭     | 意義                                                                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bV5CSType** | LCS \_ 校正 \_ 的 RGB。 這個值表示會在適當的欄位中提供端點和 gammas。 假值會造成問題。                         |
| **bV5CSType** | LCS \_ sRGB。 此值表示點陣圖位於 sRGB 色彩空間 (gammas，且已忽略) 的端點。                                                         |
| **bV5CSType** | \_內嵌的設定檔。 此值表示 **bV5ProfileData** 指向記憶體緩衝區，其中包含要使用的設定檔 (gammas 和端點會被忽略) 。 |
| **bV5CSType** | 設定檔已 \_ 連結。 此值表示 **bV5ProfileData** 會指向要使用之設定檔的檔案名 (gammas 和端點會被忽略) 。                |
| **bV5CSType** | LCS \_ WINDOWS \_ 色彩 \_ 空間。 此值表示點陣圖在 Windows 預設色彩空間中。                                                            |



 

為了將舊版點陣圖轉換成新的 BITMAPV5HEADER 結構或從新的結構進行轉換，WCS 1.0 程式設計人員參考中包含名為 Bitmap.exe 的命令列轉換公用程式檔。

## <a name="bitmapexe-a-command-line-utility-for-converting-bitmap-headers"></a>BitMap.exe：用於轉換點陣圖標頭的 Command-Line 公用程式

Bitmap.exe 是一個命令列公用程式，位於 \\ 您指定之安裝資料夾下的 Bin 資料夾中。 它會修改 Windows 點陣圖的標頭，讓您可以將現有的點陣圖從 **BITMAPINFOHEADER** 和 **BITMAPV4HEADER** 標頭結構轉換為較新的 **BITMAPV5HEADER** 結構，再轉換回來。 命令列語法如下所示：


```C++
BITMAP [/d] [/1|4|5] [/s] [/f] 
filename
```



命令列參數有下列效果。



| 參數 | 意義                                                                  |
|--------|--------------------------------------------------------------------------|
| /d     | 預設值會自動輸入在轉換的標頭中。       |
| /1     | 將指定的點陣圖轉換成 **BITMAPINFOHEADER**                    |
| /4     | 將指定的點陣圖轉換成 **BITMAPV4HEADER**                      |
| /5     | 將指定的點陣圖轉換成 **BITMAPV5HEADER**                      |
| /f     | 強制轉換，即使點陣圖已經有右邊的標頭       |
| /s     | 轉換指定資料夾和其下所有子目錄中的點陣圖 |



 

 

 
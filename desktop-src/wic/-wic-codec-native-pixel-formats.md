---
description: 本主題介紹 Windows 影像處理元件 (WIC) 所提供的像素格式。
ms.assetid: 348b6d15-e339-4dce-99f3-4d639ee9bf7d
title: 原生像素格式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379e67d422ccbd05ef178e67eb25c973e6b5943ef85d22873097f245f8914a23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206336"
---
# <a name="native-pixel-formats-overview"></a>原生像素格式總覽

本主題介紹 Windows 影像處理元件 (WIC) 所提供的像素格式。

像素格式會描述點陣圖中每個圖元的記憶體配置。 此記憶體配置描述點陣圖的影像資料如何藉由指定數值格式和色彩通道組織進行編碼。 WIC 支援多種色彩通道組織配置的數種數值格式，提供各式各樣的像素格式。

-   [位深度](#bit-depth)
-   [數值編碼](#numerical-encoding)
-   [色彩頻道](#color-channels)
    -   [RGB/BGR 色彩模型](#rgbbgr-color-model)
    -   [CMYK 色彩模型](#cmyk-color-model)
    -   [n 聲道色模型](#n-channel-color-model)
    -   [索引和灰階色彩模型](#indexed-and-grayscale-color-models)
    -   [Y'CbCr 色彩模型](#ycbcr-color-model)
-   [WIC 像素格式](#wic-pixel-format)
    -   [未定義的像素格式](#undefined-pixel-formats)
    -   [索引像素格式](#indexed-pixel-formats)
    -   [封裝的位像素格式](#packed-bit-pixel-formats)
    -   [灰階像素格式](#grayscale-pixel-formats)
    -   [RGB/BGR 像素格式](#rgbbgr-pixel-formats)
    -   [CMYK 像素格式](#cmyk-pixel-formats)
    -   [n 聲道像素格式](#n-channel-pixel-formats)
    -   [僅限 Alpha 像素格式](#alpha-only-pixel-formats)
    -   [Y'CbCr 像素格式](#ycbcr-pixel-formats)
-   [色彩空間](#color-space)
-   [原生映射格式](#native-image-formats)
    -   [BMP 原生編解碼器](#bmp-native-codec)
    -   [GIF 原生編解碼器](#gif-native-codec)
    -   [.ICO 原生編解碼器](#ico-native-codec)
    -   [JPEG 原生編解碼器](#jpeg-native-codec)
    -   [PNG 原生編解碼器](#png-native-codec)
    -   [TIFF 原生編解碼器](#tiff-native-codec)
    -   [JPEG XR 原生編解碼器](#jpeg-xr-native-codec)
-   [DDS 原生編解碼器](#dds-native-codec)
-   [像素格式延伸](#pixel-format-extensibility)
-   [相關主題](#related-topics)

## <a name="bit-depth"></a>位深度

*位深度* 是用來將每個色彩通道編碼的位數。 目前，大部分的數位影像使用的是8位，表示圖元中的每個顏色通道都是以8個位表示，提供2個⁸ (256) 每個通道的唯一值。 有位深度為8和三色通道的影像 (例如紅色、綠色和藍色) 使用每圖元24位 (bpp) ，每圖元提供2個²⁴ (16777216) 不同的色彩。

若要獲得更佳的色彩解析度，可以使用16或32等的深度。 這會提供每個顏色通道2¹⁶ (65536) 或2³²唯一值，且每個圖元的記憶體成本較高。

在某些格式中，位深度不是8的倍數。 這些格式稱為「 *壓縮* 格式」，因為圖元中的色彩通道不會對齊位元組界限。 例如，如果位深度為5，三個色頻可以用16個位儲存 (包括1位的填補，以圖元為單位調整) 。 當記憶體或處理能力有限時，壓縮的格式會很有用。

## <a name="numerical-encoding"></a>數值編碼

對於現今大部分的數位影像而言，不帶正負號的位元組和不帶正負號的短整數會用來描述每個色頻的數值範圍。 最小值 (0) 在單一色頻中代表零濃度，而當所有色彩通道都為零時，就會達到黑色。 同樣地，最大值表示全濃度，而當所有色彩通道都具有全濃度時，就會達到白色。 稍微深度為8時，UINT 提供256每色通道的唯一值 (0-255) 。 16位 UINT 提供65536每色通道的唯一值 (0-65535) 。

此外，WIC 還支援固定點和浮點數格式。 這些格式支援較大的動態範圍，因為每個顏色通道的整個數值範圍大於可見的範圍。 如此一來，在影像處理的中繼步驟期間，可以在可見範圍的上方或下方調整色彩，而不會遺失影像資訊。

### <a name="fixed-point-numerical-encoding"></a>Fixed-Point 數值編碼

16位的固定點值會轉譯為2.13： sign bit、兩個整數位和十三個小數位。 使用這項解讀，從−4.0 到 + 3.999 的數值範圍 .。。可以表示，並以帶正負號整數值 8192 (0x2000) 的1.0 值表示。

32位的固定點值會轉譯為 s 7.24：正負號位、七個整數位和二十-四個小數位。 使用這項解讀，從−128.0 到 + 127.999 的數值範圍 .。。可以表示，並以帶正負號的整數值16777216表示的1.0 值 (0x01000000) 。

## <a name="color-channels"></a>色彩頻道

像素格式的色彩通道會定義點陣圖影像資料內每個色彩的記憶體配置。 現今的數位影像中有各種不同的色彩通道結構，而 WIC 提供了許多這些不同的支援。

### <a name="rgbbgr-color-model"></a>RGB/BGR 色彩模型

RGB 和 BGR 格式描述加法色模型中的色彩。 描述影像最常見的方法是使用三個不同的色頻，代表紅色 (R) 、綠色 (G) 和藍色 (B) 。 WIC 以紅-綠-藍 (RGB) 或藍綠-紅色 (BGR) 順序提供這三個通道的支援。 這是每個顏色通道在連續位串流內出現的順序。 例如，在 GUID \_ WICPixelFormat32bppRGB 格式中，每個圖元都是32位寬。 紅色通道是記憶體中的第一個 (最小的) 位元組，後面接著綠色，再加上藍色。 相反地，在 GUID \_ WICPixelFormat32bppBGR 格式中，色彩通道的順序是相反的。 WIC 支援一些 RGB/BGR 格式，包括特殊的封裝位格式，例如 GUID \_ WICPixelFormat16bppBGR555。

> [!Note]  
> 特殊 BGR 壓縮位格式的色彩通道不是8的倍數，像是一般像素格式的色頻。 這表示通道值不是位元組對齊。 讀取封裝的位顏色通道時必須小心。

 

除了 RGB 和 BGR 格式之外，WIC 也提供支援 Alpha () 通道的 RGB 和 BGR 像素格式。 Alpha 通道提供圖元的不透明度資料。 若為具有已新增 Alpha 色板的格式，Alpha 色板通常會最後以色頻順序表示。 例如，在像素格式 GUID WICPixelFormat32bppBGRA 中 \_ ，位元組順序是藍色、綠色和紅色，後面接著 Alpha 色板。

WIC 也支援前置 (P) Alpha RGB 像素格式。 在典型的 RGBA 像素格式中，紅色、綠色和藍色色彩值是影像的實際色彩值。 若要製作標準 RGBA 格式的複合影像，必須先將前景影像的 Alpha 值乘以紅色、綠色和藍色通道，再將其新增至背景影像的色彩。 在預乘的 Alpha RGB 像素格式中，每個色頻已經乘以 Alpha 值。 這可提供更有效率的影像組合方法與 Alpha 通道資料。 若要使用 PRGBA/PBGRA 像素格式來取得每個通道的真實色彩值，必須將色彩值除以 Alpha 值，以反轉 Alpha 通道的乘法。

### <a name="cmyk-color-model"></a>CMYK 色彩模型

CMYK 是用於列印的 subtractive 色彩模型。 CMYK 模型所產生的色彩是由未吸收但反映的光線所產生。 CMYK 為青色 (C) 、洋紅 (M) 、黃色 (Y) 和黑色 (K) 的四種通道模型。 當四色通道都是最大值時，結果會是黑色。 如同 RGB/BGR 色彩模型，順序位資料流程內的位元組順序是由像素格式的名稱所指定。 例如，在像素格式 GUID WICPixelFormat32bppCMYK 中 \_ ，每個圖元都是由32位所組成。 第一個位元組包含青色值，後面接著紅色、黃色和黑色。 WIC 提供圖元的像素格式，在32和64位的每個圖元 (bpp) 。

除了標準的 CMYK 色彩模型之外，WIC 也提供使用 Alpha 的 CMYK。 這可讓 CMYK 影像具有類似 RGB/BGR 色彩模型的 Alpha 混色資料。 Alpha 色板會緊接在點陣圖的連續位串流中的黑色之後。

### <a name="n-channel-color-model"></a>n 聲道色模型

為了提供彈性，WIC 也提供沒有預先定義通道順序的像素格式。 WIC 提供的像素格式可支援三至八個連續影像資料通道（以8和16為單位）。 不同于 RGB/BGR 和 CMYK 像素格式，n 通道格式不會指定通道順序，而是可以使用的色彩通道數目。 例如，在像素格式 GUID WICPixelFormat32bpp4Channels 中 \_ ，每個圖元都是由32位所組成，每個通道的每個都佔用單一位元組。

WIC 也提供具有 Alpha 之 n 通道的像素格式。 這可讓 n 個通道影像具有類似 RGB/BGR 和 CMYK 色彩模型的 Alpha 混色資料。 Alpha 色板位於點陣圖的連續位資料流程中的最後一個色頻之後。

### <a name="indexed-and-grayscale-color-models"></a>索引和灰階色彩模型

*索引* 格式會使用色彩表，稱為「 *調色板*」。 此調色板會儲存在外部，或是以隱含的方式儲存于圖元資料。 影像中每個圖元的值都是在調色板中的索引。 使用已編制索引的格式時，每圖元的位數數目會與調色板中的專案數直接相關。 這可大幅減少代表影像所需的資料量，但也會限制影像可用的色彩數目。 WIC 支援使用1、2、4或 8 bpp 的索引格式。

針對單色 (灰階) 格式，WIC 支援1、2、4、8、16和32位的每個圖元。 若是1、8、16和32的位深度，色彩資料會儲存在單一通道中。 若位深度為2或4，圖元為灰階調色板的索引。

### <a name="ycbcr-color-model"></a>Y'CbCr 色彩模型

WIC 新增 JPEG JFIF Y'CbCr 色彩模型的支援。 將不同的色彩 Y'CbCr 為 luma 元件 (Y ' ) 和兩個色度元件 (Cb 和 Cr) 。 許多 JPEG 檔案以原生方式使用 Y'CbCr 色彩模型儲存影像資料。

人類的視覺效果系統對色度中的變更較不敏感，而不是 luma，而且 Y'CbCr 格式可以藉由減少相對於 luma 所儲存的色度資料量，來利用這種降低的敏感度。 它們的達成方式是將色度和 luma 儲存至不同的平面，並將每個元件平面調整為不同的解析度。 這種作法稱為「色度次取樣」。

因為會個別儲存色度和 luma 資料，而且可能是不同的解析度，所以 WIC 會定義個別的 luma 和色度像素格式。 WIC 支援每個通道8個位的資料。

## <a name="wic-pixel-format"></a>WIC 像素格式

WIC 中的像素格式是使用 Guid 來定義，以避免與 Ihv 發生衝突。 WIC 提供一個易記的名稱來參考原生像素格式的 GUID。 WIC 像素格式的命名慣例如下：

**\[GUID \_ WICPixelFormat \] \[ 位每圖元 \] \[ 通道順序 \] \[ 儲存體類型\]**

| 格式元件         | Description                                                                                                                                                                                                                                                                                                  |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **GUID \_ WICPixelFormat** | 所有 WIC 像素格式的描述性識別。 所有 WIC 圖元的易記名稱都是以這個字串開頭。                                                                                                                                                                                       |
| **位元/像素**       | 用於像素格式的每個圖元 (bpp) 位數。                                                                                                                                                                                                                                                |
| **頻道順序**        | 格式的每個通道的色彩通道模型和順序。                                                                                                                                                                                                                                            |
| **儲存體類型**         | 用於像素格式的數值編碼。 預設編碼是不帶正負號的整數。 如果沒有任何色彩模型資訊，則會隱含不帶正負號的整數 (UINT) 。 FixedPoint 和 Float 用來識別分別使用固定點和浮點數編碼的像素格式。 |



 

> [!Note]  
> 針對 n 通道格式， \[ 通道順序不 \] 會指定色彩順序，而是可以使用的通道數目。 例如，GUID \_ WICPixelFormat24bpp3Channels 會提供3個色頻，其中 "3Channels" 是 \[ 通道順序 \] 專案，但只表示通道數目，而不是訂單的數目。

 

例如，易記名稱 GUID \_ WICPixelFormat24bppRGB 表示像素格式會使用每圖元24位和 RGB 色彩模型。 因為此名稱不會明確識別儲存體類型，所以隱含不帶正負號的整數。

WIC 支援數個像素格式。 下表依色彩結構將類似的像素格式分組，並提供其他資訊，例如位深度、每圖元的位數，以及數值編碼。 每個資料表都包含下列資訊：

-   **易記名稱**。 像素格式的易記名稱。
-   **通道計數**。 色彩頻道的數目。
-   **每個通道的位數**。 每個通道的位數 (位深度) 。
-   **每圖元的位數**。 每圖元的位數，包括任何填補位。
-   **儲存體類型**。 影像資料的數值編碼。 這個值可以是不帶正負號的整數 (UINT) 、 (FixedPoint) 的固定點數位，或是浮點數 (浮點數) 。

> [!Note]  
> 為了清楚起見，本檔只會根據易記名稱來參考像素格式。 您可以在 wincodec .h/idl 檔案中找到像素格式的實際十六進位值。

 

### <a name="undefined-pixel-formats"></a>未定義的像素格式

下列清單顯示當像素格式未定義或對影像作業不重要時，所使用的一般像素格式。

-   GUID \_ WICPixelFormatUndefined
-   GUID \_ WICPixelFormatDontCare

### <a name="indexed-pixel-formats"></a>索引像素格式

下表列出 WIC 提供的索引像素格式。 在這些格式中，每個圖元的值都是色彩選擇區中的索引。



| 易記名稱                   | 頻道計數 | 位元/像素 | 儲存類型 |
|---------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat1bppIndexed | 1             | 1              | UINT         |
| GUID \_ WICPixelFormat2bppIndexed | 1             | 2              | UINT         |
| GUID \_ WICPixelFormat4bppIndexed | 1             | 4              | UINT         |
| GUID \_ WICPixelFormat8bppIndexed | 1             | 8              | UINT         |



 

### <a name="packed-bit-pixel-formats"></a>封裝的位像素格式

下表列出 WIC 提供的封裝位格式。 在這些格式中，色彩通道資料不會以位元組對齊。



| 易記名稱                          | 頻道計數 | 每個通道的位數       | 位元/像素 | 儲存類型 |
|-------------------------------------------|---------------|------------------------|----------------|--------------|
| GUID \_ WICPixelFormat16bppBGR555           | 3             | 5                      | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGR565           | 3             | 5 (B) /6 (G) /5 (R)          | 16             | UINT         |
| GUID \_ WICPixelFormat16bppBGRA555          | 4             | 5 (B) /5 (G) /5 (R) /1 ()     | 16             | UINT         |
| GUID \_ WICPixelFormat32bppBGR101010        | 3             | 10                     | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102      | 4             | 10 (R) /10 (G) /10 (B) /2 ()  | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA1010102XR    | 4             | 10 (R) /10 (G) /10 (B) /2 ()  | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2      | 4             | 10 (R) /10 (G) /10 (B) /2 ()  | 32             | UINT         |
| GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 | 4             | 10 (R) /10 (G) /10 (B) /2 ()  | 32             | UINT         |

針對 GUID \_ WICPixelFormat32bppBGR101010 和 guid \_ WICPixelFormat32bppRGBA1010102 格式，紅色通道會儲存在最不重要的位。 針對 GUID \_ WICPixelFormat32bppR10G10B10A2 和 guid \_ WICPixelFormat32bppR10G10B10A2HDR10 格式，紅色通道是以最有效的位定義，與 [DXGI_FORMAT_R10G10B10A2_UNORM](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)的版面配置相同。

GUID \_ WICPixelFormat32bppR10G10B10A2HDR10 格式是 HDR10 (BT. 2020 color space 和 SMPTE 2084 EOTF) 的10位像素格式。

### <a name="grayscale-pixel-formats"></a>灰階像素格式

下表列出 WIC 提供的灰階格式。 在這些格式中，色彩資料代表灰色陰影。



| 易記名稱                           | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|-----------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormatBlackWhite          | 1             | 1                | 1              | UINT         |
| GUID \_ WICPixelFormat2bppGray            | 1             | 2                | 2              | UINT         |
| GUID \_ WICPixelFormat4bppGray            | 1             | 4                | 4              | UINT         |
| GUID \_ WICPixelFormat8bppGray            | 1             | 8                | 8              | UINT         |
| GUID \_ WICPixelFormat16bppGray           | 1             | 16               | 16             | UINT         |
| GUID \_ WICPixelFormat16bppGrayFixedPoint | 1             | 16               | 16             | FixedPoint   |
| GUID \_ WICPixelFormat16bppGrayHalf       | 1             | 16               | 16             | 浮點數        |
| GUID \_ WICPixelFormat32bppGrayFloat      | 1             | 32               | 32             | 浮點數        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint | 1             | 32               | 32             | FixedPoint   |



 

### <a name="rgbbgr-pixel-formats"></a>RGB/BGR 像素格式

下表列出 WIC 提供的 RGB/BGR 格式。 這些格式會將主要色彩資料分成紅色 (R) 、綠色 (G) 和藍色 (B) 通道。 另外還有一個 Alpha () 頻道，以提供某些格式的不透明度資訊。



| 易記名稱                            | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bppRGB             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat24bppBGR             | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat32bppBGR             | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppBGRA            | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppRGBE\*          | 4             | 8                | 32             | 浮點數        |
| GUID \_ WICPixelFormat32bppPRGBA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat32bppPBGRA           | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat48bppRGB             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppBGR             | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | 3             | 16               | 48             | 固定式        |
| GUID \_ WICPixelFormat48bppBGRFixedPoint   | 3             | 16               | 48             | 固定式        |
| GUID \_ WICPixelFormat48bppRGBHalf         | 3             | 16               | 48             | 浮點數        |
| GUID \_ WICPixelFormat64bppRGBA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppBGRA            | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPRGBA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppPBGRA           | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | 3             | 16               | 64             | 固定式        |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | 4             | 16               | 64             | 固定式        |
| GUID \_ WICPixelFormat64bppBGRAFixedPoint  | 4             | 16               | 64             | 固定式        |
| GUID \_ WICPixelFormat64bppRGBHalf         | 3             | 16               | 64             | 浮點數        |
| GUID \_ WICPixelFormat64bppRGBAHalf        | 4             | 16               | 64             | 浮點數        |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | 3             | 32               | 96             | 固定式        |
| GUID \_ WICPixelFormat128bppRGBFloat       | 3             | 32               | 128            | 浮點數        |
| GUID \_ WICPixelFormat128bppRGBAFloat      | 4             | 32               | 128            | 浮點數        |
| GUID \_ WICPixelFormat128bppPRGBAFloat     | 4             | 32               | 128            | 浮點數        |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | 3             | 32               | 128            | 固定式        |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | 4             | 32               | 128            | 固定式        |



 

> [!Note]  
> \*GUID \_ WICPixelFormat32bppRGBE 格式會以4個位元組編碼 3 16 位浮點值，如下所示： R、G 和 B 通道的三個不帶正負號的8位尾數，加上共用的8位指數。 此格式會以較小的圖元標記法提供16位浮點精確度。

 

從 Windows 8 和[Windows 7 的平臺更新](/windows/desktop/direct3darticles/platform-update-for-windows-7)開始，WIC 會提供其他格式，如下表所示。



| 易記名稱                      | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppRGB       | 3             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppRGB       | 3             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat96bppRGBFloat  | 3             | 32               | 96             | FLOAT        |
| GUID \_ WICPixelFormat64bppPRGBAHalf | 4             | 16               | 64             | FLOAT        |



 

### <a name="cmyk-pixel-formats"></a>CMYK 像素格式

下表列出 WIC 提供的 CMYK 格式。 這些格式會將主要色彩資料分隔為青色 (C) 、洋紅 (M) 、黃色 (Y) 和黑色 (K) 通道。



| 易記名稱                      | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat32bppCMYK      | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bppCMYK      | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bppCMYKAlpha | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bppCMYKAlpha | 5             | 16               | 80             | UINT         |



 

### <a name="n-channel-pixel-formats"></a>n 聲道像素格式

下表列出 WIC 提供的 n 通道格式。 這些格式會提供一些未定義的色彩通道來儲存影像資料。



| 易記名稱                            | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|------------------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat24bpp3Channels       | 3             | 8                | 24             | UINT         |
| GUID \_ WICPixelFormat48bpp3Channels       | 3             | 16               | 48             | UINT         |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat32bpp4Channels       | 4             | 8                | 32             | UINT         |
| GUID \_ WICPixelFormat64bpp4Channels       | 4             | 16               | 64             | UINT         |
| GUID \_ WICPixelFormat40bpp4ChannelsAlpha  | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat40bpp5Channels       | 5             | 8                | 40             | UINT         |
| GUID \_ WICPixelFormat80bpp5Channels       | 5             | 16               | 80             | UINT         |
| GUID \_ WICPixelFormat48bpp5ChannelsAlpha  | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat48bpp6Channels       | 6             | 8                | 48             | UINT         |
| GUID \_ WICPixelFormat96bpp6Channels       | 6             | 16               | 96             | UINT         |
| GUID \_ WICPixelFormat56bpp6ChannelsAlpha  | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat56bpp7Channels       | 7             | 8                | 56             | UINT         |
| GUID \_ WICPixelFormat112bpp7Channels      | 7             | 16               | 112            | UINT         |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat64bpp8Channels       | 8             | 8                | 64             | UINT         |
| GUID \_ WICPixelFormat128bpp8Channels      | 8             | 16               | 128            | UINT         |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | 9             | 8                | 72             | UINT         |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | 9             | 16               | 144            | UINT         |



 

### <a name="alpha-only-pixel-formats"></a>僅限 Alpha 像素格式

下表列出 WIC 提供的 Alpha 格式。 此格式只包含 Alpha 資訊。



| 易記名稱                 | 頻道計數 | 每個通道的位數 | 位元/像素 | 儲存類型 |
|-------------------------------|---------------|------------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppAlpha | 1             | 8                | 32             | UINT         |



 

### <a name="ycbcr-pixel-formats"></a>Y'CbCr 像素格式

下表列出 WIC 提供的 Y'CbCr 格式。 這些格式會將主要色彩資料分成 luma (Y) 、blue 色度差異 (Cb) 和 red choma 差異 (Cr) 。 請注意，這些格式是設計用來儲存 JPEG JFIF Y'CbCr 圖元資料。



| 易記名稱                 | 頻道計數 | 位元/像素 | 儲存類型 |
|-------------------------------|---------------|----------------|--------------|
| GUID \_ WICPixelFormat8bppY     | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCb    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat8bppCr    | 1             | 8              | UINT         |
| GUID \_ WICPixelFormat16bppCbCr | 2             | 16             | UINT         |



 

## <a name="color-space"></a>色彩空間

像素格式本身沒有色彩空間。 一般而言，色彩空間是圖元值的語義解釋，視點陣圖的內容而定。 某些影像會識別定義影像色彩空間的色彩內容。 只有在沒有色彩內容時，才應該推斷色彩空間。

色彩內容資訊是由 WIC 的 [**IWICColorCoNtext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) 介面所定義。 若要取得影像框架的色彩內容資訊，請使用 **GetColorCoNtext** 方法。

如果影像的色彩空間資訊不存在，色彩空間推斷的一般規則是 UINT RGB 和灰階格式會使用標準的 RGB 色彩空間 (sRGB) ，而固定點和浮點數的 RGB 和灰階格式則使用擴充的 RGB 色彩空間 (scRGB) 。 CMYK 色彩模型使用 RWOP 的色彩空間。

## <a name="native-image-formats"></a>原生映射格式

每個 Windows 提供的 wic 編解碼器都支援 wic 像素格式的子集。 針對每個編解碼器，支援的解碼格式可能會與支援的編碼格式不同。

對影像進行解碼時，如果資料以原生方式儲存為不受解碼器支援的像素格式，則會轉換為支援的格式。 若要判斷輸出像素格式，請呼叫 [**IWICBitmapFrameDecode：： GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)。

對影像進行編碼時，請使用 [**IWICBitmapFrameEncode：： SetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat) 來要求編碼器使用特定的像素格式。 編碼器會傳回最接近支援的像素格式，這可能與所要求的不同。

下表顯示每個 Windows 提供的 WIC 編解碼器所支援的像素格式。

### <a name="bmp-native-codec"></a>BMP 原生編解碼器



| 解碼像素格式                   | 編碼器像素格式                   |
|-----------------------------------------|-----------------------------------------|
| GUID \_ WICPixelFormat1bppIndexed         | GUID \_ WICPixelFormat1bppIndexed         |
| GUID \_ WICPixelFormat4bppIndexed         | GUID \_ WICPixelFormat4bppIndexed         |
| GUID \_ WICPixelFormat8bppIndexed         | GUID \_ WICPixelFormat8bppIndexed         |
| GUID \_ WICPixelFormat16bppBGR555         | GUID \_ WICPixelFormat16bppBGR555         |
| GUID \_ WICPixelFormat16bppBGR565         | GUID \_ WICPixelFormat16bppBGR565         |
| GUID \_ WICPixelFormat24bppBGR            | GUID \_ WICPixelFormat24bppBGR            |
| GUID \_ WICPixelFormat32bppBGR            | GUID \_ WICPixelFormat32bppBGR            |
| GUID \_ WICPixelFormat32bppBGRA\*         | GUID \_ WICPixelFormat32bppBGRA\*         |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint | GUID \_ WICPixelFormat32bppPBGRA          |
|                                         | GUID \_ WICPixelFormat64bppRGBAFixedPoint |
|                                         | GUID \_ WICPixelFormat64bppBGRAFixedPoint |



 

> [!Note]  
> \_只有 Windows 8、 [Windows 7 的平臺更新](/windows/desktop/direct3darticles/platform-update-for-windows-7)和更新版本才支援 GUID WICPixelFormat32bppBGRA。
>
> -   若要編碼為此格式，請使用 **EnableV5Header32bppBGRA** 編碼器選項。 BMP 將會以 BITMAPV5HEADER 標頭來撰寫。
> -   如果檔案有 BITMAPV5HEADER，則會解碼為 GUID \_ WICPixelFormat32bppBGRA。

 

### <a name="gif-native-codec"></a>GIF 原生編解碼器



| 解碼像素格式           | 編碼器像素格式           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |



 

### <a name="ico-native-codec"></a>.ICO 原生編解碼器



| 解碼像素格式         | 編碼器像素格式 |
|-------------------------------|-----------------------|
| GUID \_ WICPixelFormat32bppBGRA |                       |



 

### <a name="jpeg-native-codec"></a>JPEG 原生編解碼器



| 解碼像素格式         | 編碼器像素格式         |
|-------------------------------|-------------------------------|
| GUID \_ WICPixelFormat8bppGray  | GUID \_ WICPixelFormat8bppGray  |
| GUID \_ WICPixelFormat24bppBGR  | GUID \_ WICPixelFormat24bppBGR  |
| GUID \_ WICPixelFormat32bppCMYK | GUID \_ WICPixelFormat32bppCMYK |



 

### <a name="png-native-codec"></a>PNG 原生編解碼器



| 解碼像素格式           | 編碼器像素格式           |
|---------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat2bppIndexed | GUID \_ WICPixelFormat2bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite  | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat2bppGray    | GUID \_ WICPixelFormat2bppGray    |
| GUID \_ WICPixelFormat4bppGray    | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray    | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray   | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat24bppBGR    | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat32bppBGRA   | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat48bppRGB    | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat64bppRGBA   | GUID \_ WICPixelFormat48bppBGR    |
|                                 | GUID \_ WICPixelFormat64bppRGBA   |
|                                 | GUID \_ WICPixelFormat64bppBGRA   |



 

### <a name="tiff-native-codec"></a>TIFF 原生編解碼器



| 解碼像素格式                | 編碼器像素格式           |
|--------------------------------------|---------------------------------|
| GUID \_ WICPixelFormat1bppIndexed      | GUID \_ WICPixelFormat1bppIndexed |
| GUID \_ WICPixelFormat4bppIndexed      | GUID \_ WICPixelFormat4bppIndexed |
| GUID \_ WICPixelFormat8bppIndexed      | GUID \_ WICPixelFormat8bppIndexed |
| GUID \_ WICPixelFormatBlackWhite       | GUID \_ WICPixelFormatBlackWhite  |
| GUID \_ WICPixelFormat4bppGray         | GUID \_ WICPixelFormat4bppGray    |
| GUID \_ WICPixelFormat8bppGray         | GUID \_ WICPixelFormat8bppGray    |
| GUID \_ WICPixelFormat16bppGray        | GUID \_ WICPixelFormat16bppGray   |
| GUID \_ WICPixelFormat32bppGrayFloat   | GUID \_ WICPixelFormat24bppBGR    |
| GUID \_ WICPixelFormat24bppBGR         | GUID \_ WICPixelFormat32bppBGRA   |
| GUID \_ WICPixelFormat32bppBGRA        | GUID \_ WICPixelFormat32bppCMYK   |
| GUID \_ WICPixelFormat32bppPBGRA       | GUID \_ WICPixelFormat48bppRGB    |
| GUID \_ WICPixelFormat48bppRGB         | GUID \_ WICPixelFormat64bppRGBA   |
| GUID \_ WICPixelFormat32bppCMYK        |                                 |
| GUID \_ WICPixelFormat40bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat64bppRGBA        |                                 |
| GUID \_ WICPixelFormat64bppPRGBA       |                                 |
| GUID \_ WICPixelFormat64bppCMYK        |                                 |
| GUID \_ WICPixelFormat80bppCMYKAlpha   |                                 |
| GUID \_ WICPixelFormat96bppRGBFloat\*  |                                 |
| GUID \_ WICPixelFormat128bppRGBAFloat  |                                 |
| GUID \_ WICPixelFormat128bppPRGBAFloat |                                 |



 

> [!Note]  
> \_只有 Windows 8、 [Windows 7 的平臺更新](/windows/desktop/direct3darticles/platform-update-for-windows-7)和更新版本才支援 GUID WICPixelFormat96bppRGBFloat。

 

### <a name="jpeg-xr-native-codec"></a>JPEG XR 原生編解碼器



| 解碼像素格式                    | 編碼器像素格式                    |
|------------------------------------------|------------------------------------------|
| GUID \_ WICPixelFormatBlackWhite           | GUID \_ WICPixelFormatBlackWhite           |
| GUID \_ WICPixelFormat8bppGray             | GUID \_ WICPixelFormat8bppGray             |
| GUID \_ WICPixelFormat16bppBGR555          | GUID \_ WICPixelFormat16bppBGR555          |
| GUID \_ WICPixelFormat16bppGray            | GUID \_ WICPixelFormat16bppGray            |
| GUID \_ WICPixelFormat24bppBGR             | GUID \_ WICPixelFormat24bppBGR             |
| GUID \_ WICPixelFormat24bppRGB             | GUID \_ WICPixelFormat24bppRGB             |
| GUID \_ WICPixelFormat32bppBGR             | GUID \_ WICPixelFormat32bppBGR             |
| GUID \_ WICPixelFormat32bppBGRA            | GUID \_ WICPixelFormat32bppBGRA            |
| GUID \_ WICPixelFormat48bppRGBFixedPoint   | GUID \_ WICPixelFormat48bppRGBFixedPoint   |
| GUID \_ WICPixelFormat16bppGrayFixedPoint  | GUID \_ WICPixelFormat16bppGrayFixedPoint  |
| GUID \_ WICPixelFormat32bppBGR101010       | GUID \_ WICPixelFormat32bppBGR101010       |
| GUID \_ WICPixelFormat48bppRGB             | GUID \_ WICPixelFormat48bppRGB             |
| GUID \_ WICPixelFormat64bppRGBA            | GUID \_ WICPixelFormat64bppRGBA            |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat96bppRGBFixedPoint   |
| GUID \_ WICPixelFormat96bppRGBFixedPoint   | GUID \_ WICPixelFormat128bppRGBAFloat      |
| GUID \_ WICPixelFormat128bppRGBFloat       | GUID \_ WICPixelFormat128bppRGBFloat       |
| GUID \_ WICPixelFormat32bppCMYK            | GUID \_ WICPixelFormat32bppCMYK            |
| GUID \_ WICPixelFormat64bppRGBAFixedPoint  | GUID \_ WICPixelFormat64bppRGBAFixedPoint  |
| GUID \_ WICPixelFormat128bppRGBAFixedPoint | GUID \_ WICPixelFormat128bppRGBAFixedPoint |
| GUID \_ WICPixelFormat64bppCMYK            | GUID \_ WICPixelFormat64bppCMYK            |
| GUID \_ WICPixelFormat24bpp3Channels       | GUID \_ WICPixelFormat24bpp3Channels       |
| GUID \_ WICPixelFormat32bpp4Channels       | GUID \_ WICPixelFormat32bpp4Channels       |
| GUID \_ WICPixelFormat40bpp5Channels       | GUID \_ WICPixelFormat40bpp5Channels       |
| GUID \_ WICPixelFormat48bpp6Channels       | GUID \_ WICPixelFormat48bpp6Channels       |
| GUID \_ WICPixelFormat56bpp7Channels       | GUID \_ WICPixelFormat56bpp7Channels       |
| GUID \_ WICPixelFormat64bpp8Channels       | GUID \_ WICPixelFormat64bpp8Channels       |
| GUID \_ WICPixelFormat48bpp3Channels       | GUID \_ WICPixelFormat48bpp3Channels       |
| GUID \_ WICPixelFormat64bpp4Channels       | GUID \_ WICPixelFormat64bpp4Channels       |
| GUID \_ WICPixelFormat80bpp5Channels       | GUID \_ WICPixelFormat80bpp5Channels       |
| GUID \_ WICPixelFormat96bpp6Channels       | GUID \_ WICPixelFormat96bpp6Channels       |
| GUID \_ WICPixelFormat112bpp7Channels      | GUID \_ WICPixelFormat112bpp7Channels      |
| GUID \_ WICPixelFormat128bpp8Channels      | GUID \_ WICPixelFormat128bpp8Channels      |
| GUID \_ WICPixelFormat40bppCMYKAlpha       | GUID \_ WICPixelFormat40bppCMYKAlpha       |
| GUID \_ WICPixelFormat80bppCMYKAlpha       | GUID \_ WICPixelFormat80bppCMYKAlpha       |
| GUID \_ WICPixelFormat32bpp3ChannelsAlpha  | GUID \_ WICPixelFormat32bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp7ChannelsAlpha  | GUID \_ WICPixelFormat40bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat72bpp8ChannelsAlpha  | GUID \_ WICPixelFormat48bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bpp3ChannelsAlpha  | GUID \_ WICPixelFormat56bpp6ChannelsAlpha  |
| GUID \_ WICPixelFormat80bpp4ChannelsAlpha  | GUID \_ WICPixelFormat64bpp7ChannelsAlpha  |
| GUID \_ WICPixelFormat96bpp5ChannelsAlpha  | GUID \_ WICPixelFormat72bpp8ChannelsAlpha  |
| GUID \_ WICPixelFormat112bpp6ChannelsAlpha | GUID \_ WICPixelFormat64bpp3ChannelsAlpha  |
| GUID \_ WICPixelFormat128bpp7ChannelsAlpha | GUID \_ WICPixelFormat80bpp4ChannelsAlpha  |
| GUID \_ WICPixelFormat144bpp8ChannelsAlpha | GUID \_ WICPixelFormat96bpp5ChannelsAlpha  |
| GUID \_ WICPixelFormat64bppRGBAHalf        | GUID \_ WICPixelFormat112bpp6ChannelsAlpha |
| GUID \_ WICPixelFormat48bppRGBHalf         | GUID \_ WICPixelFormat128bpp7ChannelsAlpha |
| GUID \_ WICPixelFormat32bppRGBE            | GUID \_ WICPixelFormat144bpp8ChannelsAlpha |
| GUID \_ WICPixelFormat16bppGrayHalf        | GUID \_ WICPixelFormat64bppRGBAHalf        |
| GUID \_ WICPixelFormat32bppGrayFixedPoint  | GUID \_ WICPixelFormat48bppRGBHalf         |
| GUID \_ WICPixelFormat64bppRGBFixedPoint   | GUID \_ WICPixelFormat32bppRGBE            |
| GUID \_ WICPixelFormat128bppRGBFixedPoint  | GUID \_ WICPixelFormat16bppGrayHalf        |
| GUID \_ WICPixelFormat64bppRGBHalf         | GUID \_ WICPixelFormatBlackWhite           |



 

## <a name="dds-native-codec"></a>DDS 原生編解碼器



| 解碼像素格式          | 編碼器像素格式          |
|--------------------------------|--------------------------------|
| GUID \_ WICPixelFormat32bppBGRA  | GUID \_ WICPixelFormat32bppBGRA  |
| GUID \_ WICPixelFormat32bppPBGRA | GUID \_ WICPixelFormat32bppPBGRA |



 

> [!Note]  
> dds Windows 提供的編解碼器支援使用下列 DXGI 格式值編碼的 dds 檔案 \_ ：

 

-   DXGI \_ 格式 \_ BC1 \_ UNORM
-   DXGI \_ 格式 \_ BC2 \_ UNORM
-   DXGI \_ 格式 \_ BC3 \_ UNORM

這些會以 GUID \_ WICPixelFormat32bppBGRA 或 guid WICPixelFormat32bppPBGRA 的形式進行解碼和編碼 \_ 。 如需詳細資訊，請參閱 [DDS 格式總覽](dds-format-overview.md)。

## <a name="pixel-format-extensibility"></a>像素格式延伸

自訂影像格式可以使用 WIC 原本不提供的像素格式，例如 YCbCr (YUV) 和 YCCK (Y/Cb/Cr/K) 。 WIC 提供一個擴充性模型，可讓內建和增益集的像素格式在相同的影像處理管線內運作。 若要將這些像素格式與 WIC 影像處理管線整合，您必須建立像素格式轉換器，以將增益集像素格式轉換成一或多個原生像素格式。 建立格式轉換器的主要介面為 [**IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC Guid 和 Clsid](-wic-guids-clsids.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[HD 相片規格1。0](https://www.microsoft.com/whdc/xps/wmphoto.mspx)
</dt> </dl>

 

 

---
description: 擴充的色彩資訊
ms.assetid: 05ca73c6-d105-47bc-96bc-b784f669febe
title: 擴充的色彩資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ffce83acccd2004156d55c0711836271d9ad5cfe7a6ac395e0d9fcbb418142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466368"
---
# <a name="extended-color-information"></a>擴充的色彩資訊

如果您知道 RGB 色彩的任何相關資訊，您就知道 (255、255、255) 是 *白色* 色彩的8位 RGB 三位數。 但是，這三種方法所定義的實際 *色彩* 為何？

答案可能會令人驚訝：沒有一些額外的資訊，這三種情況不會定義任何特定的色彩！ 任何 RGB 值的意義取決於 *色彩空間*。 如果我們不知道色彩空間，請嚴格說，我們不知道色彩。

色彩空間會定義指定色彩值的數值標記法如何以實體光線的形式重現。 當影片編碼于一個色彩空間中，但顯示于另一個色彩空間時，除非影片經過色彩校正，否則會產生失真的色彩。 因此，若要達到精確的色彩精確度，請務必知道來源影片的色彩空間。 之前，Windows 中的影片管線並未包含預期色彩空間的相關資訊。 從 Windows Vista 開始，DirectShow 和媒體基礎都支援媒體類型中的擴充色彩資訊。 這項資訊也適用于 DirectX Video 加速 (DXVA) 。

以數學方式描述色彩空間的標準方式是使用 CIE 的 XYZ 色彩空間，其定義依據照明的國際委員會 (CIE) 。 在影片中直接使用 CIE XYZ 值並不實用，但 CIE XYZ 色彩空間可做為在色彩空間之間轉換時的中繼標記法。

若要精確地重現色彩，需要下列資訊：

-   色彩主要複本。 色彩主要複本定義 CIE XYZ tristimulus 值如何以 RGB 元件表示。 實際上，色彩主要複本會定義指定 RGB 值的「意義」。
-   Transfer 函數。 傳送函式是將線性 RGB 值轉換成非線性 R'G'B 值的函式。 這個函式也稱為 *gamma 校正*。
-   轉移矩陣。 傳送矩陣會定義 R'G'B ' 轉換成 Y'PbPr 的方式。
-   色度取樣。 在 luma 的色度元件中，大部分的 YUV 影片都會以較少的解析度進行傳輸。 以影片格式的 FOURCC 表示色度取樣。 例如，YUY2 是4:2:2 格式，這表示會以2的因數水準取樣色度樣本。
-   色度地點。 取樣色度時，與 luma 樣本相關的色度樣本位置會決定如何插入遺漏的樣本。
-   名義範圍。 名義範圍定義如何將 Y'PbPr 值調整為 Y'CbCr。

## <a name="color-space-in-media-types"></a>媒體類型中的色彩空間

DirectShow、媒體基礎和 DirectX Video 加速 (DXVA) 全部都有不同的方式來表示影片格式。 幸運的是，由於相關列舉相同，因此很容易就能將色彩空間資訊從一個轉換成另一個。

-   DXVA 1.0： [**DXVA \_ ExtendedFormat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) 結構中提供了色彩空間資訊。
-   DXVA 2.0： [**DXVA2 \_ ExtendedFormat**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_extendedformat) 結構結構中提供了色彩空間資訊。 此結構與 DXVA 1.0 結構相同，而且欄位的意義相同。
-   DirectShow： [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)結構中提供色彩空間資訊。 這項資訊會儲存在 **dwControlFlags** 欄位的最高24位。 如果有色彩空間資訊，請在 **dwControlFlags** 中設定 **AMCONTROL \_ COLORINFO \_ 目前** 旗標。 當設定這個旗標時， **dwControlFlags** 欄位應該被解釋為 [**DXVA \_ ExtendedFormat**](/windows-hardware/drivers/ddi/dxva/ns-dxva-_dxva_extendedformat) 結構，但結構的較低8個位會保留給 **AMCONTROL \_ xxx** 旗標。
-   影片捕獲驅動程式：在 [**KS \_ VIDEOINFOHEADER2**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-tagks_videoinfoheader2) 結構中提供色彩空間資訊。 此結構與 [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) 結構相同，而且欄位的意義相同。
-   媒體基礎：色彩空間資訊會以屬性的形式儲存在媒體類型中：

    

    | 色彩資訊  | 屬性                                                                                                                                                   |
    |--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 色彩主要複本    | [**MF \_ MT \_ 影片 \_ 主要複本**](mf-mt-video-primaries-attribute.md)                                                                                         |
    | Transfer 函數  | [**MF \_ MT \_ 傳送函式 \_**](mf-mt-transfer-function-attribute.md)                                                                                     |
    | 轉移矩陣    | [**MF \_ MT \_ YUV \_ 矩陣**](mf-mt-yuv-matrix-attribute.md)                                                                                                   |
    | 色度次取樣 | [**MF \_ MT \_ 子類型**](mf-mt-subtype-attribute.md)<br/> FOURCC 所指定的 (，會儲存在子類型 GUID 的第一個 **DWORD** 中 ) <br/> |
    | 色度地點      | [**MF \_ MT \_ 視頻 \_ 色度 \_ 地點**](mf-mt-video-chroma-siting-attribute.md)                                                                                |
    | 名義範圍      | [**MF \_ MT \_ 影片 \_ 名義 \_ 範圍**](mf-mt-video-nominal-range-attribute.md)                                                                                |

    

     

## <a name="color-space-conversion"></a>色彩空間轉換

從一個 Y'CbCr 空間轉換成另一個空間需要執行下列步驟。

1.  反向量化：使用來源名義範圍將 Y'CbCr 表示轉換成 Y'PbPr 標記法。
2.  Upsampling：插上色度值以將取樣的色度值轉換為4:4:4。
3.  YUV 至 RGB 轉換：使用來源傳輸矩陣從 Y'PbPr 轉換成非線性 R'G'B。
4.  反向傳送函式：使用傳送函式的反向轉換非線性 R'G'B ' 轉換為線性 RGB。
5.  RGB 色彩空間轉換：使用色彩主要複本從來源 RGB 空間轉換成目標 RGB 空間。
6.  傳送函式：使用目標傳送函式，將線性 RGB 轉換成非線性 R'G'B。

7.  RGB 至 YUV 轉換：使用目標傳輸矩陣將 R'G'B ' 轉換為 Y'PbPr。
8.  縮減取樣：篩選色度值以將4:4:4 轉換為4:2:2、4:2:0 或4:1:1。
9.  量化：使用目標名義範圍將 Y'PbPr 轉換為 Y'CbCr。

步驟1–4發生于來源色彩空間，而步驟6–9則出現在目標色彩空間中。 在實際的執行中，中間步驟可以是近似值，而且可以合併連續的步驟。 一般來說，精確度和計算成本之間會有取捨。

例如，若要從 RT. 601 轉換為 RT. 709 需要下列階段：

-   反向量化： Y'CbCr (601) 至 Y'PbPr (601) 
-   Upsampling： Y'PbPr (601) 
-   YUV 至 RGB： Y'PbPr (601) 至 R'G'B ' (601) 
-   反向傳送函式： R'G'B ' (601) 至 RGB (601) 
-   RGB 色彩空間轉換： RGB (601) 至 RGB (709) 
-   傳送函式： RGB (709) R'G'B ' (709) 
-   RGB 至 YUV： R'G'B ' (709) 至 Y'PbPr (709) 
-   縮減取樣： Y'PbPr (709) 

-   量化： Y'PbPr (709) 至 Y'CbCr (709) 

## <a name="using-extended-color-information"></a>使用擴充的色彩資訊

若要在整個管線中保持色彩精確度，必須在來源或解碼器導入色彩空間資訊，並透過管線將所有方法傳達給接收器。

### <a name="video-capture-devices"></a>影片捕獲裝置

大部分的類比捕獲裝置會在捕獲影片時使用妥善定義的色彩空間。 Capture 驅動程式應該提供包含色彩資訊之 **KS \_ VIDEOINFOHEADER2** 格式區塊的格式。 為了回溯相容性，驅動程式應該接受不包含色彩資訊的格式。 這可讓驅動程式使用不接受擴充色彩資訊的元件。

### <a name="file-based-sources"></a>以檔案為基礎的來源

剖析影片檔案時，DirectShow) 中的媒體來源 (或剖析器篩選器可能會提供一些色彩資訊。 例如，DVD 導覽器可以根據 DVD 內容來決定色彩空間。 其他色彩資訊可能可用於此解碼器。 例如，MPEG-2 基本影片串流會在序列顯示延伸模組欄位中提供色彩資訊 \_ \_ 。 如果色彩資訊未在來源中明確描述，則可能由內容類型隱含定義。 例如，NTSC 和 PAL 的 DV 影片各使用不同的色彩空間。 最後，該解碼器可以使用從來源的媒體類型取得的任何色彩資訊。

### <a name="other-components"></a>其他元件

其他元件可能需要在媒體類型中使用色彩空間資訊：

-   選取轉換演算法時，軟體色彩空間轉換器應該使用色彩空間資訊。
-   影片 mixers （例如增強的影片轉譯器 (EVR) 混音器）應該在混合不同內容類型的影片串流時使用色彩資訊。
-   DXVA 影片處理 Api 和 DDIs 可讓呼叫者指定色彩空間資訊資訊。 GPU 應該在執行模擬器的影片混合時使用此資訊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[DirectX Video 加速2。0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 

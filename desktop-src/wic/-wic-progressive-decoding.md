---
description: 本主題介紹漸進式解碼，以及如何在應用程式中使用漸進式解碼。
ms.assetid: d22c2c59-0fa1-4452-93f1-dbf151033714
title: 漸進式解碼總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf005dfb5b4cf5a69ca45020776fee9f0641eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194120"
---
# <a name="progressive-decoding-overview"></a>漸進式解碼總覽

本主題介紹漸進式解碼，以及如何在應用程式中使用漸進式解碼。 它也會提供建立支援漸進解碼之編解碼器的指導方針。

本主題包含下列各節。

-   [簡介](#introduction)
-   [什麼是漸進式解碼？](#what-is-progressive-decoding)
-   [Windows 7 中的漸進解碼支援](#progressive-decoding-support-in-windows-7)
-   [JPEG 漸進式解碼](#jpeg-progressive-decoding)
-   [PNG/GIF 漸進式解碼](#pnggif-progressive-decoding)
    -   [PNG 漸進式解碼](#png-progressive-decoding)
    -   [GIF 漸進式解碼](#gif-progressive-decoding)
-   [應用程式中的漸進式解碼](#progressive-decoding-in-applications)
-   [漸進式解碼的自訂編解碼器支援](#custom-codec-support-for-progressive-decoding)
-   [相關主題](#related-topics)

## <a name="introduction"></a>簡介

漸進式解碼能讓您在整個影像下載完成之前，以累加方式解碼和轉譯部分影像。 這項功能可大幅改善使用者在從網際網路觀看影像時的體驗，因為使用者不需要等待整個映射下載，就可以開始進行解碼。 在下載整個影像之前，使用者可以看到有可用資料的影像預覽。 這項功能對於任何用來從網際網路或受限頻寬的資料來源來查看影像的應用程式而言是不可或缺的。

Windows 7 中的 Windows 影像處理元件 (WIC) 支援像是 JPEG、PNG 和 GIF 等常用影像格式的漸進式解碼。 WIC 也支援任何已啟用 WIC 的非 Microsoft 編解碼器，可執行漸進式解碼。 目前的 WIC 版本不支援漸進式編碼。 本主題概要說明 Windows 7 中的漸進解碼，以及在您的應用程式中啟用漸進式解碼的程式。

## <a name="what-is-progressive-decoding"></a>什麼是漸進式解碼？

漸進式解碼是能夠以累加方式將影像的部分從不完整的影像檔解碼。 傳統解碼需要完整的影像檔案，才能開始進行解碼。 漸進式解碼會在影像的漸進式層級下載完成之後開始。 此解碼器會對影像的目前漸進式層級執行解碼傳遞。 然後，它會在每一個漸進層級下載時，對影像執行多個解碼傳遞。 每次解碼行程都會顯示更多影像，直到映射完全下載和解碼為止。 解碼完整映射所需的行程數目取決於影像檔案格式，以及用來建立映射的編碼程式。

影像必須經過明確編碼，才能執行漸進式解碼，但並非所有影像格式都支援它。 下列清單摘要說明使用漸進式解碼的需求。

-   影像檔必須支援漸進式解碼。 大部分的影像格式都不支援漸進式解碼，雖然常用的影像格式是 JPEG、PNG 和 GIF。
-   影像檔案必須編碼為漸進式影像。 使用漸進式影像編碼所建立的影像檔無法執行漸進式解碼，即使檔案格式也會支援它。
-   支援漸進式解碼的編解碼器必須可用。 如果編解碼器不支援漸進式解碼，則以漸進式影像編碼的影像將會解碼為傳統影像。

## <a name="progressive-decoding-support-in-windows-7"></a>Windows 7 中的漸進解碼支援

Windows 7 提供內建的編解碼器，可支援 JPEG、PNG 和 GIF 影像格式的漸進式解碼。 上述每個 Windows 7 編解碼器都會在映射上執行多個解碼傳遞。 每個傳遞都會對應至特定層級和已解碼的影像部分，最後會到達完整解碼的影像。

每個影像格式都會以不同的方式處理漸進解碼。 下表提供有關漸進層級數目的資訊，以及 Windows 7 漸進解碼格式所支援的解碼方法的相關資訊。 

| 映像格式 | 支援的漸進層級數目 | 漸進式解碼方法 |
|--------------|----------------------------------------|-----------------------------|
| JPEG         | 由影像定義                       | 增加解析度       |
| PNG          | 7                                      | 交錯                 |
| GIF          | 4                                      | 交錯                 |



 

此外，您可以藉由提供漸進式介面和方法的支援，在編解碼器中實作為漸進解碼。 如果編解碼器不支援漸進解碼，則在呼叫這些方法時，應該會傳回適當的錯誤訊息。

## <a name="jpeg-progressive-decoding"></a>JPEG 漸進式解碼

JPEG 漸進式解碼會以更高的解析度呈現每個層級的影像資料，直到可以使用完整解析度的影像為止。 影像的每個層級都會設定為提供不同的解決層級。 由於有更多漸進層級可供使用，因此影像會以較高的解析度顯示，直到解析完整解析度的影像為止。

可用層級數目和每個層級所設定的解析度，完全取決於編碼的 JPEG。 下列兩個影像顯示在兩個漸進層級的 JPEG 漸進式解碼範例。

![jpeg 漸進式解碼範例](graphics/Progressive_JPEG_Comparison.jpg)

左邊的影像會在累進層級0進行解碼。 右邊的影像會在五個漸進式層級之後完整解碼。

## <a name="pnggif-progressive-decoding"></a>PNG/GIF 漸進式解碼

PNG 和 GIF 漸進式解碼都使用交錯式漸進式解碼方法。 這兩種格式的解碼程式都非常類似。

### <a name="png-progressive-decoding"></a>PNG 漸進式解碼

PNG 影像檔提供七個漸進式層級進行解碼，如 PNG 規格中所述。 藉由在每次的解碼器行程上解碼指定的圖元模式來實作為 PNG 漸進解碼。 下表中的 PNG 規格的模式是在整個影像上進行複寫。 每個數位代表要將對應的圖元解碼的漸進式層級。



|     |     |     |     |     |     |     |     |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 1   | 6   | 4   | 6   | 2   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 3   | 6   | 4   | 6   | 3   | 6   | 4   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |
| 5   | 6   | 5   | 6   | 5   | 6   | 5   | 6   |
| 7   | 7   | 7   | 7   | 7   | 7   | 7   | 7   |



 

從上表中，您可以判斷每次傳遞的解碼器都會解碼的圖元。 與 Windows 7 GIF 編解碼器不同的是，Windows 7 PNG 編解碼器會將掃描行上最左邊的可用圖元複製到空的圖元。

下列影像顯示三個漸進式層級的 Windows 7 PNG 漸進解碼編解碼器範例。

![png 漸進式解碼範例](graphics/PNG_Progressive_Comparison.jpg)

左上方的影像會顯示在漸進式層級0解碼的 PNG 影像。 右上方的影像會顯示在漸進式層級3解碼的相同 PNG 影像。 下圖顯示在7個漸進式層級之後完整解碼的相同影像。

### <a name="gif-progressive-decoding"></a>GIF 漸進式解碼

GIF 影像檔提供四個漸進式層級進行解碼，如 GIF 規格中所述。 每個階段都會填入影像內的特定資料列，並在第四次通過之後產生完整的影像。 下列來自 GIF 規格的表格會顯示每次傳遞的解碼時，所解碼的掃描行。 

| 層級編號/傳遞編號 | 已填入掃描行   | 啟動掃描行 |
|---------------------------|------------------------|--------------------|
| 1                         | 每八個掃描行 | 0                  |
| 2                         | 每八個掃描行 | 4                  |
| 3                         | 每四次掃描行 | 2                  |
| 4                         | 每秒掃描行 | 1                  |



 

雖然編解碼器可以在任何特定層級指定空白圖元的內容，但是 Windows GIF 編解碼器會將填入的掃描行複寫到空白掃描行上方，以填入空的掃描行。

## <a name="progressive-decoding-in-applications"></a>應用程式中的漸進式解碼

主要漸進式解碼介面是 [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) 介面。 若要取得介面的參考，請查詢影像框架 ([**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)) 以進行 **IWICProgressiveLevelControl**。 然後可以從介面存取漸進式方法。

下列程式碼提供在應用程式中使用漸進式解碼的範例。


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
               if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```



上述程式碼提供在大部分的應用程式中執行漸進式解碼所需的基本功能。 使用程式碼時，可以在影像圖元資料變成可用時存取漸進式層級。 [**SetCurrentLevel**](/windows/desktop/api/Wincodec/nf-wincodec-iwicprogressivelevelcontrol-setcurrentlevel)函式會封鎖執行，直到要求的層級可用為止。

## <a name="custom-codec-support-for-progressive-decoding"></a>漸進式解碼的自訂編解碼器支援

如果客戶的影像格式支援漸進式解碼，則編解碼器開發人員可能會選擇執行 [**IWICProgressiveLevelControl**](/windows/desktop/api/Wincodec/nn-wincodec-iwicprogressivelevelcontrol) 。 對漸進式解碼的支援不是 WIC 探索和仲裁的需求。 不過，漸進式解碼可大幅增強使用者體驗，並應盡可能考慮執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows 影像處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[Continuous-Tone 的數位壓縮和編碼仍然是影像-需求和指導方針](https://www.w3.org/Graphics/JPEG/itu-t81.pdf)
</dt> <dt>

[JPEG 檔案交換格式](https://www.w3.org/Graphics/JPEG/jfif3.pdf)
</dt> <dt>

[GIF89a 規格](https://www.w3.org/Graphics/GIF/spec-gif89a.txt)
</dt> <dt>

[可移植網狀圖形 (PNG) 規格和延伸模組](http://www.libpng.org/pub/png/spec/)
</dt> </dl>

 

 




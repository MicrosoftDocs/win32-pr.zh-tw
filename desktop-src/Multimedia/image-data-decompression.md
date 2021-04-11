---
title: Image-Data 解壓縮
description: Image-Data 解壓縮
ms.assetid: 4bff02be-dac8-41f4-a3af-2da6a2693ffe
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、映射資料解壓縮
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，映射-資料解壓縮
- ICDecompressEx 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25614f157436056f7f24c340f6cc6f4dbc62d9ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314869"
---
# <a name="image-data-decompression"></a>Image-Data 解壓縮

您的應用程式會使用一系列的 [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) 函式來控制解壓縮程式。 這些函式可協助您執行下列工作：

-   選取解壓縮。
-   準備解壓縮解壓縮。
-   將資料解壓縮。
-   結束解壓縮。

您的應用程式處理壓縮的方式類似于處理壓縮的方式，不同之處在于輸入格式是壓縮格式，而且輸出格式是可顯示的格式。 解壓縮的輸入格式通常是從資料流程標頭取得。 判斷輸入格式之後，您的應用程式可以使用 [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) 或 [**ICOpen**](/windows/desktop/api/Vfw/nf-vfw-icopen) 函式來尋找可以處理它的解壓縮程式。

[**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex)函式和宏是 [**ICDecompress**](/windows/desktop/api/Vfw/nf-vfw-icdecompress)函式群組的超集合，並提供更多功能。 **ICDecompressEx**、 [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)、 [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend)和 [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)的功能取代 **ICDecompress**、 [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin)、 [**ICDecompressEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressend)和 [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery)函式的功能。 使用 **ICDecompressEx** 函式和宏取代 **ICDecompress** 對應專案。

## <a name="decompressor-and-decompression-format-selection"></a>解壓縮和解壓縮格式選取專案

如果您想要解壓縮資料，而您的應用程式需要特定的輸出格式，您可以使用 [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery) 函數來查詢解壓縮程式，以判斷它是否支援輸入和輸出格式。

如果輸出格式在您的應用程式中並不重要，您只需要尋找可以處理輸入格式的解壓縮程式。 若要判斷解壓縮程式是否可以處理輸入格式，請使用 [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)並為 *LpbiDst* 參數指定 **Null** 。 您的應用程式可以藉由傳送 [**ICM \_ 解壓縮 \_ 取得 \_ 格式**](icm-decompress-get-format.md) 訊息 (或使用 [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) 宏) ，判斷指定解壓縮格式的資料所需的緩衝區大小。 您也可以傳送 **ICM \_ 解壓縮 \_ 取得 \_ 格式** (或 [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) 宏) 來取出格式資料。 解壓縮解壓縮會在 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構中傳回其建議的格式。 此格式通常會在解壓縮期間保留大部分的資訊。 您的應用程式應該在解壓縮資訊之前，確保解壓縮程式會成功傳回。

因為您的應用程式會配置解壓縮所需的記憶體，所以必須判斷解壓縮程式針對輸出格式所能要求的最大記憶體。 **ICM \_ 解壓縮 \_ 取得 \_ 格式** 訊息會取得解壓縮程式針對預設格式使用的位元組數目。

如果您的應用程式使用 [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)來定義它自己的格式，它也必須取得點陣圖的調色板。 **ICDecompressExQuery** 不提供調色板定義。  (大部分的應用程式都使用標準格式，且不需要取得調色板。 ) 您的應用程式可以傳送 [**ICM \_ 解壓縮 \_ GET \_**](icm-decompress-get-palette.md) 選擇區訊息來取得調色板， (或使用 [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) 宏) 。

## <a name="decompressor-initialization"></a>解壓縮初始化

當您的應用程式選取的解壓縮程式可處理所需的輸入和輸出格式時，您可以使用 [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin) 函式來初始化解壓縮程式。 此函式需要解壓縮控制碼以及輸入和輸出格式。

## <a name="data-decompression"></a>資料解壓縮

您可以使用 [**ICDecompressEx**](/windows/desktop/api/Vfw/nf-vfw-icdecompressex) 函式來解壓縮框架。 您的應用程式必須重複使用這個函式，直到序列中的所有框架都已解壓縮為止。

如果您的影片串流在播放期間落後其他元件 (例如音訊) ，您的應用程式可以指定 **ICDECOMPRESS \_ HURRYUP** 旗標來加速解壓縮。 若要這樣做，解壓縮可能只會解壓縮下一個框架所需的資訊，而不會完全解壓縮目前的畫面格。 因此，當您的應用程式使用這個旗標時，不應該嘗試繪製解壓縮的資料。

當您的應用程式將資料解壓縮之後，它就可以傳送 [**ICM \_ DECOMPRESSEX \_ END**](icm-decompressex-end.md) Message (或使用 [**ICDecompressExEnd**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexend) 宏) 通知解壓縮程式已完成。 如果您想要在使用此函式之後重新開機解壓縮，您的應用程式必須使用 [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)重新初始化解壓縮程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[BC-VCM-LVM-HYPERV 服務](vcm-services.md)
</dt> </dl>

 

 
---
title: Image-Data 壓縮
description: Image-Data 壓縮
ms.assetid: 689cf403-cbb5-4ccb-a05b-0caa617430ed
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) 、影像資料壓縮
- BC-VCM-LVM-HYPERV (視訊壓縮管理員) 、影像資料壓縮
- ICCompress 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8f59a163a9b5a74d2d2fe984417069985fa86a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375080"
---
# <a name="image-data-compression"></a>Image-Data 壓縮

您的應用程式可以使用一系列的 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式和宏來壓縮資料。 函式和宏可協助您執行下列工作：

-   判斷要用於指定之輸入格式的壓縮格式。
-   準備壓縮。
-   壓縮資料。
-   結束壓縮。

您的應用程式可以使用 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式和宏，來加強對壓縮進程的控制權。 這組函式和宏會處理個別的畫面，而不是整個序列。 例如，您的應用程式可以使用 **ICCompress** 函式來識別要壓縮為主要畫面格的畫面格。

壓縮程式會以一種格式接收資料、壓縮資料，並使用指定的格式傳回壓縮的資料版本。 一般輸入格式會使用 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) 結構來指定 dib。 一般輸出格式會指定壓縮的 Dib，同時也會使用 **BITMAPINFO** 結構。

> [!Note]  
> 若要將播放期間的影像和音訊降低效能降至最低，請避免壓縮 AVI 檔案一次以上。 在編輯系統中結合未壓縮的部分影片，然後壓縮最終產品。

 

## <a name="compressor-and-compression-format-selection"></a>壓縮和壓縮格式選取專案

如果您想要壓縮資料，而您的應用程式需要特定的輸出格式，請將 [**ICM \_ 壓縮 \_ 查詢**](icm-compress-query.md) 訊息 (，或使用 [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) 宏) 來查詢壓縮程式，以判斷它是否支援輸入和輸出格式。

如果輸出格式對您的應用程式而言並不重要，您只需要尋找可以處理輸入格式的壓縮程式。 若要判斷壓縮程式是否可以處理輸入格式，您可以傳送 **ICM \_ 壓縮 \_ 查詢**，為 *lParam* 參數指定 **Null** 。 此訊息不會將輸出格式傳回給您的應用程式。 您的應用程式可以藉由傳送 [**ICM \_ 壓縮 \_ 取得 \_ 格式**](icm-compress-get-format.md) 訊息 (或使用 [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) 宏) ，判斷指定壓縮格式的資料所需的緩衝區大小。 您也可以藉由傳送 ICM \_ 壓縮 \_ 取得 \_ 格式 (或 [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) 宏) 來取得格式資料。

如果您想要判斷壓縮程式可能需要壓縮的最大緩衝區，請傳送 [**ICM \_ 壓縮 \_ 取得 \_ 大小**](icm-compress-get-size.md) 訊息 (或使用 [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) 宏) 。 您可以使用 [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) 函式所傳回的位元組數目，為後續的影像壓縮配置緩衝區。

## <a name="compressor-initialization"></a>壓縮的初始化

當您的應用程式選取可以處理其所需之輸入和輸出格式的壓縮程式之後，您可以使用 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息 (，或使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏) 來初始化壓縮程式。 此訊息需要壓縮的控制碼以及輸入和輸出格式。

## <a name="data-compression"></a>資料壓縮

您可以使用 [**ICCompress**](/windows/desktop/api/Vfw/nf-vfw-iccompress) 函式來壓縮框架。 您的應用程式必須重複使用這個函式，直到序列中的所有框架都經過壓縮為止。 您的應用程式也必須追蹤和遞增以 **ICCompress** 壓縮的每個畫面格的數目。 壓縮程式會使用此值來檢查是否在快速時態壓縮期間依序傳送框架， (儲存後續畫面格) 之間的差異。 如果您的應用程式此舉將框架，則應該使用與第一次壓縮框架時相同的框架編號。 如果您的應用程式會壓縮仍框架的影像，則可以將畫面格編號指定為零。

您的應用程式可以使用 ICCOMPRESS 的主要畫面格旗標，藉由 [**ICCOMPRESS**](/windows/desktop/api/Vfw/nf-vfw-iccompress)主要畫面格來將框架壓縮。 **\_**

當 BC-VCM-LVM-HYPERV 在壓縮框架之後將控制權傳回給您的應用程式時，BC-VCM-LVM-HYPERV 會將壓縮的資料儲存在 *lpbiOutput* 和 *lpData* 參數所參考的結構中。 如果您的應用程式需要移動壓縮的資料，它會在 *lpbiOutput* 中指定之 [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)結構的 *biSizeImage* 成員中找到其大小。

> [!Note]  
> 您的應用程式必須配置儲存未壓縮和壓縮資料的結構和緩衝區。 如果壓縮程式支援時態壓縮，則您的應用程式也必須配置結構和緩衝區，以保存先前資訊框架的格式和資料。

 

## <a name="ending-compression"></a>結束壓縮

當您的應用程式壓縮資料之後，它就可以使用 [**ICCompressEnd**](/windows/desktop/api/Vfw/nf-vfw-iccompressend) 宏通知壓縮程式已完成。 如果您想要在使用此函式之後重新開機壓縮，您的應用程式必須透過傳送 [**ICM \_ 壓縮 \_ 開始**](icm-compress-begin.md) 訊息 (或使用 [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) 宏) 來重新初始化壓縮程式。

 

 
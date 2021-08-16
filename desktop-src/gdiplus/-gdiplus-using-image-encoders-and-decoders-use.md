---
description: Windows GDI+ 提供 Image 類別和 Bitmap 類別，可將影像儲存在記憶體中，並在記憶體中處理影像。
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: 使用影像編碼器和解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c3509b8fc48ff8c9ef2c52093a6fd06a4349602c6e904df24cf7e528e9f8e34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977278"
---
# <a name="using-image-encoders-and-decoders"></a>使用影像編碼器和解碼器

Windows GDI+ 提供 [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別和 [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別，可將影像儲存在記憶體中，並在記憶體中處理影像。 GDI+ 透過映射編碼器的協助，將映射寫入磁片檔案，並從磁片檔案載入映射，並提供映射解碼器的協助。 編碼器會將 **影像** 或 **點陣圖** 物件中的資料轉譯為指定的磁片檔案格式。 解碼器會將磁片檔中的資料轉譯成 **影像** 和 **點陣圖** 物件所需的格式。 GDI+ 具有支援下列檔案類型的內建編碼器和解碼器：

-   BMP
-   GIF
-   JPEG
-   PNG
-   TIFF

GDI+ 也有內建的支援下列檔案類型的解碼器：

-   WMF
-   EMF
-   圖示

下列主題會更詳細地討論編碼器和解碼器：

-   [列出已安裝的編碼器](-gdiplus-listing-installed-encoders-use.md)
-   [列出已安裝的解碼器](-gdiplus-listing-installed-decoders-use.md)
-   [正在抓取編碼器的類別識別碼](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [判斷編碼器所支援的參數](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [將 BMP 影像轉換為 PNG 影像](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [設定 JPEG 壓縮等級](-gdiplus-setting-jpeg-compression-level-use.md)
-   [轉換 JPEG 影像而不遺失資訊](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [建立和儲存多框架影像](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [從 Multiple-Frame 影像複製個別的框架](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 




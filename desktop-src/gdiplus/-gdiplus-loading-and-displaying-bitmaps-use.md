---
description: 若要在螢幕上顯示 (點陣圖) 的點陣影像，您需要影像物件和繪圖物件。
ms.assetid: 8c1a26d9-b640-4f38-8276-10c4464525f2
title: 載入和顯示點陣圖
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: ab2405462db5017215893d50d93dc0b228633cfb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/20/2021
ms.locfileid: "104974793"
---
# <a name="loading-and-displaying-bitmaps"></a>載入和顯示點陣圖

另請參閱 [WIC 檢視器 GDI + 範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)。

若要在螢幕上顯示 (點陣圖) 的點陣影像，您需要 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件和 [**圖形**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) 物件。 將檔案的名稱 (或) 的資料流程指標傳遞至 **影像** 的函式。 建立 **影像** 物件之後，將該 **影像** 物件的位址傳遞給 **圖形** 物件的 **DrawImage** 方法。

下列範例會從 JPEG 檔案建立 [**影像**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) 物件，然後在 (60，10) 的左上角繪製影像：

```cpp
Image image(L"Grapes.jpg");
graphics.DrawImage(&image, 60, 10);
```

下圖顯示在指定位置繪製的影像。

![包含影像之視窗的螢幕擷取畫面，其中包含原始點的標注 ](images/imageposition1.png)

[**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image)類別提供載入和顯示點陣影像和向量影像的基本方法。 [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap)類別是繼承自 **Image** 類別，可提供更特製化的方法來載入、顯示及操作點陣影像。 例如，您可以從圖示控制碼 (HICON) 來建立 **點陣圖** 物件。

下列範例會取得圖示的控制碼，然後使用該控制碼來建立 [**點陣圖**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) 物件。 程式碼會將 **Bitmap** 物件的位址傳遞至 [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics)物件的 **DrawImage** 方法，以顯示圖示。

```cpp
HICON hIcon = LoadIcon(NULL, IDI_APPLICATION);
Bitmap bitmap(hIcon);
graphics.DrawImage(&bitmap, 10, 10);
```

## <a name="see-also"></a>另請參閱

[WIC 檢視器 GDI + 範例應用程式](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/wic/wicviewergdiplus)

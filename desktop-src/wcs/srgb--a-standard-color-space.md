---
title: sRGB 標準色彩空間
description: 由於網際網路頻寬的考慮，Hewlett-Packard 和 Microsoft 已建議採用標準的預先定義色彩空間，稱為 sRGB (IEC 61966-2-1) ，因此可讓您以極少的資料負擔進行精確的色彩對應。
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS) 、sRGB 色彩空間
- WCS (Windows 色彩系統) 、sRGB 色彩空間
- 影像色彩管理、sRGB 色彩空間
- 色彩管理、sRGB 色彩空間
- 色彩、sRGB 色彩空間
- sRGB 色彩空間
- 色彩空間、sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/30/2021
ms.locfileid: "107000340"
---
# <a name="srgb-a-standard-color-space"></a>sRGB：標準色彩空間

由於網際網路頻寬的考慮，Hewlett-Packard 和 Microsoft 已建議採用標準的預先定義 [色彩空間](c.md) ，稱為 *sRGB* (IEC 61966-2-1) ，因此可讓您以極少的資料負擔進行精確的 [色彩對應](c.md) 。

您可以在 WCS 1.0 程式設計人員參考的 [說明] 資料夾中，找到可討論 sRGB （sRGB）技術詳細資料的白皮書說明文件版本 \\ 。

不同的檔案格式可能會使用或新增旗標，以指定影像位於 sRGB 色彩空間中。 在與 Windows 裝置無關的點陣圖中 (DIB) 格式，將 [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md)結構的 **bV5CSType** 成員設定為 **LCS \_ sRGB** ，會指定 DIB 色彩位於 sRGB 色彩空間中。

WCS 1.0 提供 sRGB 的原生支援。 有兩種方式可以使用 WCS 1.0 來轉譯定義于 sRGB 色彩空間中的影像：

**在裝置內容中呈現影像**

1.  在顯示裝置上 (DC) 建立裝置內容。
2.  使用 [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) 函數設定色彩管理。
3.  使用 [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) 函式，將 DIB 傳送至 DC。 只要 Dib [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md)結構的 **bV5CSMType** 成員設定為 **LCS \_ sRGB**，系統就會執行適當的色彩管理。

**若要在裝置內容外部呈現影像**

1.  使用 [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw)建立轉換。 *PLogColorSpace* 參數所指向之 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)結構的 **LcsCSType** 成員應設定為 **LCS \_ sRGB**。 *HDestProfile* 參數會指出顯示裝置的色彩空間。
2.  在裝置上顯示影像之前，請先使用已建立的色彩轉換來將影像色彩符合。

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>輸入色彩空間和輸出設定檔的 WCS 1.0 預設值

未指定任何輸入色彩空間時，根據預設，WCS 1.0 會使用 sRGB 色彩空間作為 [色彩對應](c.md)的輸入色彩空間。

如果未指定輸出設定檔，但指定了預設裝置，則 WCS 1.0 會選取預設的輸出設定檔。 如果預設裝置沒有相關聯的設定檔，則 WCS 1.0 會使用 sRGB 色彩空間作為輸出設定檔。

下表顯示當預設裝置無法使用時，所產生的色彩轉換。



|                                 | 指定的輸出設定檔                              | 未指定輸出設定檔                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| 指定的輸入色彩空間     | 轉換會使用指定的設定檔。                | 轉換會從已知的輸入色彩空間轉換成 sRGB。 |
| 未指定輸入色彩空間 | 轉換會從 sRGB 轉換成已知的輸出設定檔。 | 假設是從 sRGB 轉換成 sRGB，未完成任何動作。 |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB 和 Embedded 設定檔

從 ICM 版本2.0 開始，利用 WCS 的應用程式可以將設定檔內嵌于映射中。 內嵌設定檔可協助使用者的應用程式維持一致的色彩外觀，即使影像是經由網際網路傳輸亦同。

使用 sRGB 色彩空間的影像不需要內嵌色彩設定檔。 因為它們沒有內嵌的設定檔，所以在頻寬有限的資料通道之間，以 sRGB 為基礎的映射較小且更容易轉移。

應用程式應在影像的點陣圖標頭中設定 **LCS \_ sRGB** ，以指出影像使用 sRGB 色彩空間。 如需詳細資訊，請參閱 [Windows 點陣圖標頭結構](using-structures-in-wcs-1-0.md) 和 [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)。

 

 
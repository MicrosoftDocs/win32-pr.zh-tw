---
description: Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。
ms.assetid: a05b496a-bd4c-4065-8060-df0f8930cde7
title: Windows 影像處理元件總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764260dd9375f1372c1936c7dbd776295eb34433
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193140"
---
# <a name="windows-imaging-component-overview"></a>Windows 影像處理元件總覽

Windows 影像處理元件 (WIC) 提供可延伸的架構，可用於處理影像和影像中繼資料。 WIC 可讓獨立軟體廠商 (Isv) 和獨立硬體廠商 (Ihv) 開發自己的映射編解碼器，並取得與標準影像格式相同的平臺支援，例如 TIFF、JPEG、PNG、GIF、BMP 和 HDPhoto (。 不論影像格式為何，都使用單一、一致的介面集來處理所有圖像，因此任何使用 WIC 的應用程式都會在安裝編解碼器時，自動支援新的映射格式。 可延伸的中繼資料架構可讓應用程式將自己的專屬中繼資料直接讀取和寫入影像檔案，因此中繼資料永遠不會遺失或與影像分開。

本主題包含下列各節。

-   [Windows 影像處理元件功能](#windows-imaging-component-features)
-   [原生編解碼器](#native-codecs)
-   [相關主題](#related-topics)

## <a name="windows-imaging-component-features"></a>Windows 影像處理元件功能

WIC 的主要功能包括：

-   可讓應用程式開發人員透過單一、一致的通用介面集，以任何影像格式執行影像處理作業，而不需要事先知道特定影像格式。
-   為影像編解碼器、像素格式和中繼資料提供可延伸的「隨插即用」架構，並自動執行新格式的執行時間探索。
-   支援在影像檔案中讀取和寫入任意中繼資料，並能夠在編輯期間保留無法辨識的中繼資料。
-   在整個影像處理管線中保留高位深度的影像資料，最多可達32位的每個通道。
-   針對最熱門的影像格式、像素格式和中繼資料架構，提供內建支援。

## <a name="native-codecs"></a>原生編解碼器

WIC 包含數個內建編解碼器。 平臺提供下列標準編解碼器。 

| 轉碼器                                                                                             | Mime 類型                       | 解碼器 | 編碼器 |
|---------------------------------------------------------------------------------------------------|----------------------------------|----------|----------|
| BMP (Windows 點陣圖格式) 、BMP 規格 v5。                                                | image/bmp                        | 是      | 是      |
| GIF (圖形交換格式 89a) 、GIF 規格 89a/89m                                  | image/gif                        | 是      | 是      |
| .ICO (圖示格式)                                                                                  | 影像/.ico                        | 是      | 否       |
| JPEG (聯合攝影專家群組) 、JFIF 規格1.02                                  | image/jpeg、image/jpe、image/jpg | 是      | 是      |
| PNG (可攜的網狀圖形) ，PNG 規格1。2                                            | image/png                        | 是      | 是      |
| TIFF (標記的影像檔案格式) ，TIFF 規格6。0                                           | 影像/tiff、影像/.tif            | 是      | 是      |
| Windows Media 相片、 [HD 相片規格 1.0](https://www.microsoft.com/whdc/xps/wmphoto.mspx) | image/vnd.openxmlformats-officedocument.spreadsheetml.sheet. ms-phot                | 是      | 是      |
| DDS (DirectDraw 介面)                                                                           | image/vnd.openxmlformats-officedocument.spreadsheetml.sheet. ms-dds                 | 是      | 是      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[WIC 中繼資料總覽](-wic-about-metadata.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> <dt>

[AITCodec 範例編解碼器](/previous-versions/dotnet/netframework-3.0/ms771770(v=vs.85))
</dt> </dl>

 

 

---
description: Windows 影像處理元件 (WIC) 提供元件物件模型 (以 COM) 為基礎的 API，以用於 c 和 c + +。
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: WIC API 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d6cb8669bc04a031ec147d6642f5c2f5413f896534ddd580f27e4a00f42bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668867"
---
# <a name="wic-api-overview"></a>WIC API 總覽

Windows 影像處理元件 (WIC) 提供元件物件模型 (以 COM) 為基礎的 API，以用於 c 和 c + +。 WIC API 會公開各種與影像相關的功能，包括：

-   標準 web 映射格式的內建編解碼器。
-   標準元資料格式的內建支援。
-   範圍廣泛的像素格式支援。
-   高彩支援;包含30位的延伸範圍、30位高精確度，以及48位高精確度和寬範圍像素格式。
-   映射編解碼器、像素格式和元資料格式的可擴充架構。

本主題包含下列主題。

-   [WIC 標頭檔](#wic-header-files)
-   [程式庫檔案](#library-files)
-   [Class factory](#class-factories)
-   [影像處理元件](#imaging-components)
-   [另請參閱](#see-also)

## <a name="wic-header-files"></a>WIC 標頭檔

WIC Api 定義于下列標頭和介面定義語言 (IDL) 檔：



| 檔案              | 描述                                          |
|-------------------|------------------------------------------------------|
| wincodec。h        | 定義主要 WIC Api 的 C 和 c + + 版本。  |
| wincodec .idl      | 定義主要 WIC 介面。                  |
| wincodecsdk。h     | 定義 C 和 c + + 版本的中繼資料 WIC Api。 |
| wincodecsdk .idl   | 定義 WIC 中繼資料介面。                 |
| wincodec \_ proxy。h | 定義 WIC proxy 匯出。                       |



 

若要使用 WIC，您的應用程式必須包含 wincodec 和/或 wincodecsdk，視您應用程式所需的 API 而定。

## <a name="library-files"></a>程式庫檔案

WIC 程式庫檔案：



| 檔案              | 描述                                                            |
|-------------------|------------------------------------------------------------------------|
| windowscodecs .lib | Windows 軟體開發套件 (SDK) 提供的匯入程式庫。 |
| windowscodecs.dll | 由作業系統提供的庫存執行程式庫。         |



 

若要連結到 WIC Api，您的應用程式必須包含 windowscodec，做為額外的連結器相依性。

## <a name="class-factories"></a>Class factory

下表描述 WIC Api 針對建立 WIC 元件所提供的兩個 COM class factory。



| Factory 介面                                               | 描述                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | 使用 WIC 元件開發應用程式的主要 class factory。 此 factory 會建立映射解碼器、編碼器和資料流程等元件。   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | 以 WIC 元件開發人員為目標的 Class factory。 從這個 factory 建立的元件主要用於編解碼器和元資料處理程式開發。 |



 

若要建立任一個 class factory，請使用 [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) COM 函數。 下列範例示範如何建立 WIC 映射處理站。


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>影像處理元件

WIC Api 提供數種類型的影像處理元件。 下表說明一些常見的 WIC 元件。 如需可用元件的完整清單，請參閱 [WIC 介面](-wic-codec-ifaces.md)。



| 元件類型                                                      | 描述                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**點陣圖**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | 表示 [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)的可寫入記憶體中標記法。 |
| [**解碼 器**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | 用來將資料流程中的影像資料解碼成適用于影像處理的格式。                    |
| [**編碼**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | 將影像資料寫入資料流程。                                                                                |
| [**串流**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | 用來讀取和寫入檔案、網路資源、記憶體區塊等的資料。                      |
| [**格式轉換器**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | 用來從一個像素格式轉換成另一個圖元。                                                             |
| [**中繼資料查詢讀取器**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | 用來讀取影像或影像框架的中繼資料。                                                             |
| [**中繼資料查詢寫入器**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | 用來將中繼資料寫入影像或影像框架。                                                            |



 

## <a name="see-also"></a>另請參閱

[參考](-wic-codec-reference.md)


[範例和程式碼範例](-wic-samples.md)


 

 

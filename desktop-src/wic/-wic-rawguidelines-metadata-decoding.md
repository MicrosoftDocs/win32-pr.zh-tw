---
description: 解碼
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: 解碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bfef7fe219ae7ff05227bfba48b69188844dc2373bd1c3099737224758fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667325"
---
# <a name="decoding"></a>解碼

為了適當地支援中繼資料，解碼器作者必須執行下列動作：

-   執行 [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) 和 [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) 介面。
-   在框架解碼上執行 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 。 如果編解碼器支援容器層級的中繼資料，則必須在容器層級的解碼器以及框架解碼器上，執行此介面。
-   解碼影像資料流程時，請呼叫 [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)：：[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) ，以具現化每個中繼資料區塊的中繼資料讀取器。  (編解碼器所實行的任何新中繼資料讀取器都必須向 WIC 註冊。 ) 

    此解碼器不應自行建立中繼資料讀取器，而是使用 WIC 根據資料流程中的中繼資料區塊來建立它們。 此解碼器必須在找到的所有區塊上進行這項作業，即使它們不是 docoder 的原生已知，因為未來的中繼資料讀取器可能會安裝在系統上，以瞭解如何處理這些中繼資料區塊。

-   如果沒有區塊的元資料處理程式，請使用中繼資料建立選項具現化未知的中繼資料讀取器。
-   透過 [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) 介面公開中繼資料讀取器的集合。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[Windows映射處理元件總覽](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[相機原始影像格式的 WIC 指導方針](-wic-rawguidelines.md)
</dt> <dt>

[如何撰寫 WIC-Enabled 編解碼器](-wic-howtowriteacodec.md)
</dt> </dl>

 

 




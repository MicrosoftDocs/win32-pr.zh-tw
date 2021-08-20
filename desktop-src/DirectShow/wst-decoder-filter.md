---
description: WST 解碼篩選
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61da0540c683e8c4646074715b0518717b4e1958beea5b8ca2ae41fb4629790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290768"
---
# <a name="wst-decoder-filter"></a>WST 解碼篩選

此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可用於 Windows XP 和 Windows Server 2003 作業系統。

> [!Note]  
> 從 Windows Vista 開始，DirectShow 不會提供篩選準則來解碼全球標準 Teletext (WST) 。

 

wst 解碼器是一種核心模式篩選器，接受來自[WST 編解碼器](wst-codec-filter.md)的已解碼全球標準 Teletext 資料，並使用 Microsoft 提供的字型，在重迭[Mixer](overlay-mixer-filter.md)上將點陣圖傳遞給釘選2。 目前只支援西歐語言;目前未提供任何 Unicode 字型。

您可以藉由呼叫 [**ICaptureGraphBuilder2：： RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)，使用 WST 編解碼器的輸出 pin 來自動將此篩選新增至圖形。



| 標籤 | 值 |
|------------------------------------------|---------------------------------------------------------------|
| 篩選介面                        | ISpecifyPropertyPages、 [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder) |
| 輸入 Pin 媒體類型                    | 媒體 \_ VBI、MEDIASUBTYPE \_ TELETEXT                        |
| 輸入 Pin 介面                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| 輸出 Pin 媒體類型                   | 媒體 \_ 媒體                                              |
| 輸出 Pin 介面                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| 篩選 CLSID                             | CLSID \_ WSTDecoder                                             |
| 屬性頁 CLSID                      | CLSID \_ WstDecoderPropertyPage                                 |
| 可執行檔                               | Wstdecod.DLL                                                  |
| [優點](merit.md)                       | 一般的業績 \_                                                 |
| [篩選準則分類](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectShow過濾 器](directshow-filters.md)
</dt> <dt>

[觀賞全球標準 Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 




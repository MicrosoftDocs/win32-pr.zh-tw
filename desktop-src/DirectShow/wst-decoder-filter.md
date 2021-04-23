---
description: WST 解碼篩選
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: WST 解碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908476"
---
# <a name="wst-decoder-filter"></a>WST 解碼篩選

此元件已從 Windows Vista 和更新版本的作業系統中移除。 它可在 Windows XP 和 Windows Server 2003 作業系統中使用。

> [!Note]  
> 從 Windows Vista 開始，DirectShow 未提供篩選來解碼全球標準 Teletext (WST) 。

 

WST 解碼器是一種核心模式篩選器，接受來自 [WST 編解碼器](wst-codec-filter.md) 的已解碼全球標準 Teletext 資料，並使用 Microsoft 提供的字型，將重迭 [混音](overlay-mixer-filter.md) 器上的點陣圖傳遞給釘選2。 目前只支援西歐語言;目前未提供任何 Unicode 字型。

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

[DirectShow 篩選](directshow-filters.md)
</dt> <dt>

[觀賞全球標準 Teletext](viewing-world-standard-teletext.md)
</dt> </dl>

 

 




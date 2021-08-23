---
description: EVR 媒體類型的協商
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: EVR 媒體類型的協商
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974487"
---
# <a name="evr-media-type-negotiation"></a>EVR 媒體類型的協商

本主題說明增強型影片轉譯器 (EVR) 如何驗證媒體類型。

-   針對 DirectShow EVR 篩選準則，當篩選的釘選連線時，就會發生型別協商。

-   針對 EVR 媒體接收器，媒體類型是透過資料流程接收上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面進行設定。 拓撲載入器通常會協商媒體類型，但應用程式也可以直接設定媒體類型。

EVR 不會報告任何慣用的媒體類型。 用戶端必須測試媒體類型，直到找到可接受的類型。 您必須先設定參考資料流的媒體類型，才能在任何子串流上設定類型。

針對參考資料流，EVR 混音器會取得相容的 DirectX 影片加速清單， (DXVA) 轉譯目標格式。 EVR 展示者會使用此清單來選取 Direct3D 交換鏈的格式。 如果找不到相容的轉譯目標格式，EVR 會拒絕媒體類型。

針對子串流，EVR 混音器會查詢 DXVA 裝置是否支援該子資料流程格式與針對參考資料流所選取的呈現目標格式。 因此，可用的子資料流程格式可能會根據參考資料流而變更。

以下是更詳細的流程。 這些詳細資料對大部分的應用程式而言並不重要，但如果您要撰寫自訂的混音器或簡報者，可能會很有説明。

參考資料流的協商會如下所示：

1.  EVR 會在混音器上呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 。

2.  混音器會使用 [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) 結構，將媒體類型轉換成 DXVA 2.0 描述。

3.  混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) 來取得影片處理器 guid 清單。

4.  針對每個視頻處理器 GUID，混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) 來取得支援的轉譯目標格式。

5.  EVR 會使用 MFVP MESSAGE INVALIDATEMEDIATYPE 訊息來呼叫展示者上的 [**IMFVideoPresenter：:P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) \_ \_ 。 這則訊息會讓展示者選取新的格式。

6.  展示者會呼叫 [**IMFTransform：： GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) ，以從混音器取得可用輸出格式的清單。 混音器會從步驟4中取得的格式產生這份清單。

7.  展示者會選取一種格式，並在混音器上呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) 。

針對子串流，此程式較簡單：

1.  EVR 會在混音器上呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) 。

2.  混音器會呼叫 [**IDirectXVideoProcessorService：： GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) 來取得可用的子串流格式清單。

3.  如果建議的格式包含在此清單中，EVR 會接受輸入類型。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[增強的影片轉譯器](enhanced-video-renderer.md)
</dt> </dl>

 

 




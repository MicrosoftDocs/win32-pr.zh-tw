---
description: 媒體來源物件模型
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: 媒體來源物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321588"
---
# <a name="media-source-object-model"></a>媒體來源物件模型

本主題說明 Microsoft 媒體基礎中媒體來源的物件模型。 媒體來源必須執行兩個物件：

-   表示來源內容的簡報描述項，包括資料流程的數目和每個資料流程的格式。 如需簡報描述項的詳細資訊，請參閱 [展示描述](presentation-descriptors.md)項。
-   產生來源資料的一或多個媒體資料流程。

在播放開始之前，來源不會建立資料流程。

## <a name="media-source-interfaces"></a>媒體來源介面

媒體來源必須透過 **QueryInterface** 公開下列介面。



| 介面                                                | 描述                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | 所有媒體來源都需要。                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | 所有媒體來源都需要。 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)介面會繼承這個介面。 |



 

（選擇性）媒體來源可以執行 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) 介面，並將下列任何介面實作為服務：



| 服務介面                                  | Description                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | 控制播放速率。                                       |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | 報告支援的播放率範圍。           |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | 可讓品質管制員調整音訊或影片品質。 |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | 提供中繼資料。                                                |



 

如果媒體來源可 (1.0) 的速率來播放，則應該公開速率控制服務 ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) 和 [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)) 。 否則，假設來源僅支援以正常速度播放。 如需詳細資訊，請參閱 [執行速率控制](implementing-rate-control.md)。

如需服務介面和 [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)的詳細資訊，請參閱 [服務介面](service-interfaces.md)。

## <a name="media-stream-interfaces"></a>媒體資料流程介面

媒體資料流程必須執行下列介面。



| 介面                                                | 描述                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | 所有媒體資料流程都需要。                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | 所有媒體資料流程都需要。 [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)介面會繼承這個介面。 |



 

目前沒有針對媒體資料流程定義任何服務介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體來源](media-sources.md)
</dt> </dl>

 

 




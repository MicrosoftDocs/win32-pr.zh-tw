---
title: 使用未壓縮的音訊和影片串流
description: 使用未壓縮的音訊和影片串流
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- 串流，設定未壓縮的音訊和影片串流
- 編解碼器，設定未壓縮的音訊和影片串流
- 影片串流，未壓縮
- 音訊串流，未壓縮
- 未壓縮的音訊和影片串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106966842"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>使用未壓縮的音訊和影片串流

在大部分的情況下，未壓縮的媒體具有極大的儲存和傳遞需求，但在某些本機播放案例中，品質層級必須足以保證不使用壓縮。

未壓縮媒體資料流程的設定應該會反映來源媒體的設定。 設定未壓縮的資料流程時，您必須計算媒體的位元速率，然後藉由呼叫 [**IWMStreamConfig：： SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)來適當地設定資料流程。 因為未壓縮的資料流程無法用於串流處理，所以您應該一律呼叫 [**IWMStreamConfig：： SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow)，將未壓縮媒體資料流程的緩衝區視窗設定為零。

未壓縮的影片資料流程支援下列像素格式：

-   WMMEDIASUBTYPE \_ RGB555
-   WMMEDIASUBTYPE \_ RGB24
-   WMMEDIASUBTYPE \_ RGB32
-   WMMEDIASUBTYPE \_ I420
-   WMMEDIASUBTYPE \_ IYUV
-   WMMEDIASUBTYPE \_ YV12
-   WMMEDIASUBTYPE \_ YUY2
-   WMMEDIASUBTYPE \_ UYVY
-   WMMEDIASUBTYPE \_ YVYU

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**所有資料流程通用的設定**](configuration-common-to-all-streams.md)
</dt> <dt>

[**設定音訊串流**](configuring-audio-streams.md)
</dt> <dt>

[**設定資料流程**](configuring-streams.md)
</dt> <dt>

[**設定影片串流**](configuring-video-streams.md)
</dt> </dl>

 

 





---
description: 如何控制簡報狀態
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: 如何控制簡報狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2148410527ecf966b10e605bbe4d6beb0ac3d515acd6895e4fc03e73564a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942418"
---
# <a name="how-to-control-presentation-states"></a>如何控制簡報狀態

媒體會話可提供傳輸控制項，例如變更呈現狀態 (播放、暫停和停止播放播放清單的播放案例) 。 本主題說明應用程式應該呼叫以變更播放狀態的媒體會話方法。

下表顯示有效的呈現狀態轉換。



| 狀態轉換 | 描述                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| 播放 > 暫停 | 呈現頻率會凍結。                                                            |
| Play > 停止  | 呈現時鐘已重設。                                                           |
| 暫停-> 播放 | 簡報時鐘會從它在播放期間旁邊的時間繼續進行，以暫停轉換。 |
| 暫停-> 停止 | 呈現時鐘已重設。                                                           |
| 停止 > 播放  | 簡報時鐘從簡報的開頭開始。                      |
| 停止 > 暫停 | 不允許。                                                                               |



 

## <a name="to-change-presentation-states"></a>變更展示狀態

-   呼叫 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) 方法以暫停播放。

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    在呼叫這個方法之前，應用程式必須呼叫 [**IMFMediaSession：： GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) 方法，以找出媒體來源是否支援暫停狀態。 如果有的話，這個方法會傳回 *pdwCaps* 參數中的 **MFSESSIONCAP \_ PAUSE** 。

    暫停：暫時停止媒體會話、簡報時鐘，以及目前簡報的資料流程接收。 在呼叫成功完成之後，應用程式會收到 [MESessionPaused](mesessionpaused.md) 事件。

-   呼叫 [**IMFMediaSession：： stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) 方法以停止播放。

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    這個方法會停止媒體來源、對應的時鐘和串流接收器，藉以停止媒體會話。 如果媒體會話控制 [Sequencer 來源](sequencer-source.md)，則會由 sequencer 來源停止基礎原生來源。 停止媒體會話之後，應用程式會收到 [MESessionStopped](mesessionstopped.md) 事件。

-   呼叫 [**IMFMediaSession：： start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法以開始播放或搜尋至新位置。

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    這個方法會從暫停和停止狀態啟動媒體會話。 媒體會話負責設定管線中的資料流程。 此方法會指示媒體會話啟動簡報時鐘。 在這個呼叫之後，媒體會話會將 [MESessionStarted](mesessionstarted.md) 事件傳送至應用程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體會話](media-session.md)
</dt> </dl>

 

 




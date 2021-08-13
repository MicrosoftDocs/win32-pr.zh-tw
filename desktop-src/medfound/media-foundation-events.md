---
description: 媒體基礎事件
ms.assetid: d925f63d-3359-4ba1-802f-0c2b11a3f973
title: 媒體基礎事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a922127941bd94103eac9cfb02ef33d1c0b789eb632f2689a3adc81494c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119268818"
---
# <a name="media-foundation-events"></a>媒體基礎事件



| 事件                                                                                        | 描述                                                                                                                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)                               | 已移除音訊裝置。                                                                                                                            |
| [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)                                 | 音訊會話與 Windows 終端機服務會話中斷連線                                                                              |
| [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)               | 音訊會話已由獨佔模式連接佔用。                                                                                         |
| [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)                               | 音訊裝置的預設音訊格式已變更。                                                                                                   |
| [MEAudioSessionGroupingParamChanged](meaudiosessiongroupingparamchanged.md)                 | 已變更音訊會話的群組參數。                                                                                                   |
| [MEAudioSessionIconChanged](meaudiosessioniconchanged.md)                                   | 音訊會話圖示已變更。                                                                                                                          |
| [MEAudioSessionNameChanged](meaudiosessionnamechanged.md)                                   | 音訊會話的顯示名稱已變更。                                                                                                                  |
| [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)                             | Windows 的音訊伺服器系統已關閉。                                                                                                           |
| [MEAudioSessionVolumeChanged](meaudiosessionvolumechanged.md)                               | 音訊會話的音量或靜音狀態已變更                                                                                                    |
| [MEBufferingStarted](mebufferingstarted.md)                                                 | 媒體來源已開始緩衝資料。                                                                                                                   |
| [MEBufferingStopped](mebufferingstopped.md)                                                 | 媒體來源已停止緩衝資料。                                                                                                                   |
| [MECaptureAudioSessionDeviceRemoved](mecaptureaudiosessiondeviceremoved.md)                 | 裝置已移除。                                                                                                                                  |
| [MECaptureAudioSessionDisconnected](mecaptureaudiosessiondisconnected.md)                   | 因為使用者登出 Windows 終端機服務 (WTS) 會話，所以音訊會話已中斷連線。                                            |
| [MECaptureAudioSessionExclusiveModeOverride](mecaptureaudiosessionexclusivemodeoverride.md) | 使用者以獨佔模式開啟音訊串流。                                                                                                       |
| [MECaptureAudioSessionFormatChanged](mecaptureaudiosessionformatchanged.md)                 | 音訊格式已變更。                                                                                                                                |
| [MECaptureAudioSessionServerShutdown](mecaptureaudiosessionservershutdown.md)               | 音訊會話伺服器關機。                                                                                                                       |
| [MECaptureAudioSessionVolumeChanged](mecaptureaudiosessionvolumechanged.md)                 | 磁片區已變更。                                                                                                                                      |
| [MEConnectEnd](meconnectend.md)                                                             | 網路來源已完成開啟 URL。                                                                                                               |
| [MEConnectStart](meconnectstart.md)                                                         | 網路來源已開始開啟 URL。                                                                                                                |
| [MEContentProtectionMessage](mecontentprotectionmessage.md)                                 | 輸出保護設定的設定已變更。                                                                                               |
| [MEEnablerCompleted](meenablercompleted.md)                                                 | 內容啟用程式物件的動作已完成。                                                                                                           |
| [MEEnablerProgress](meenablerprogress.md)                                                   | 通知內容啟用物件的進度。                                                                                                        |
| [MEEndOfPresentation](meendofpresentation.md)                                               | 在簡報結束時由媒體來源引發。                                                                                                       |
| [MEEndOfPresentationSegment](meendofpresentationsegment.md)                                 | 當區段已完成，且後面接著另一個區段時，由 sequencer 來源引發。                                                           |
| [MEEndOfStream](meendofstream.md)                                                           | 當資料流程結束時由媒體資料流程引發。                                                                                                           |
| [MEError](meerror.md)                                                                       | 發出嚴重錯誤的信號。                                                                                                                                 |
| [MEExtendedType](meextendedtype.md)                                                         | 自訂事件種類。                                                                                                                                       |
| [MEIndividualizationCompleted](meindividualizationcompleted.md)                             | 已完成的個人化。                                                                                                                           |
| [MEIndividualizationStart](meindividualizationstart.md)                                     | 正在開始進行的個人化。                                                                                                                     |
| [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md)                           | 授權取得已完成。                                                                                                                         |
| [MELicenseAcquisitionStart](melicenseacquisitionstart.md)                                   | 即將開始取得授權。                                                                                                                   |
| [MEMediaSample](memediasample.md)                                                           | 當媒體資料流程提供新的範例時引發。                                                                                                        |
| [MENewPresentation](menewpresentation.md)                                                   | 由媒體來源引發新的簡報已準備就緒。                                                                                                    |
| [MENewStream](menewstream.md)                                                               | 當媒體來源啟動新的資料流程時引發。                                                                                                    |
| [MENonFatalError](menonfatalerror.md)                                                       | 進行串流時發生非嚴重錯誤。                                                                                                             |
| [MEPolicyChanged](mepolicychanged.md)                                                       | 資料流程的輸出原則已變更。                                                                                                                  |
| [MEPolicyError](mepolicyerror.md)                                                           | 如果強制執行輸出原則時發生錯誤，則由受信任的輸出引發。                                                                         |
| [MEPolicyReport](mepolicyreport.md)                                                         | 包含有關強制執行輸出原則的狀態資訊。                                                                                   |
| [MEPolicySet](mepolicyset.md)                                                               | [**IMFOutputTrustAuthority：： SetPolicy**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputtrustauthority-setpolicy)方法已完成。                                                    |
| [MEQualityNotify](mequalitynotify.md)                                                       | 提供有關播放品質給品質管制員的意見反應。                                                                                         |
| [MEReconnectEnd](mereconnectend.md)                                                         | 在重新連接嘗試結束時由媒體來源引發。                                                                                           |
| [MEReconnectStart](mereconnectstart.md)                                                     | 在重新連接嘗試開始時由媒體來源引發。                                                                                         |
| [MERendererEvent](merendererevent.md)                                                       | 由增強的影片轉譯器所引發 (EVR 從展示者收到使用者事件時) 。                                                            |
| [MESequencerSourceTopologyUpdated](mesequencersourcetopologyupdated.md)                     | 當 [**IMFSequencerSource：： UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) 方法以非同步方式完成時，由 sequencer 來源引發。 |
| [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md)                             | 當會話功能變更時由媒體會話引發。                                                                                        |
| [MESessionClosed](mesessionclosed.md)                                                       | 當 [**IMFMediaSession：： Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) 方法以非同步方式完成時引發。                                                 |
| [MESessionEnded](mesessionended.md)                                                         | 當媒體會話完成播放佇列中的最後一個簡報時引發。                                                    |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)                       | 當新的簡報開始時，由媒體會話引發。                                                                                              |
| [MESessionPaused](mesessionpaused.md)                                                       | 當 [**IMFMediaSession：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) 方法以非同步方式完成時引發。                                                 |
| [MESessionRateChanged](mesessionratechanged.md)                                             | 當播放速率變更時由媒體會話引發。                                                                                              |
| [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md)                             | 當媒體會話完成清除要求時引發。                                                                                       |
| [MESessionStarted](mesessionstarted.md)                                                     | 當 [**IMFMediaSession：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) 方法以非同步方式完成時引發。                                                 |
| [MESessionStopped](mesessionstopped.md)                                                     | 當 [**IMFMediaSession：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) 方法以非同步方式完成時引發。                                                   |
| [MESessionStreamSinkFormatChanged](mesessionstreamsinkformatchanged.md)                     | 當媒體接收器的格式變更時，由媒體會話引發。                                                                                     |
| [MESessionTopologiesCleared](mesessiontopologiescleared.md)                                 | 當 [**IMFMediaSession：： ClearTopologies**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-cleartopologies) 方法以非同步方式完成時，由媒體會話引發。        |
| [MESessionTopologySet](mesessiontopologyset.md)                                             | 在 [**IMFMediaSession：： SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) 方法以非同步方式完成之後引發                                     |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                                       | 當拓撲的狀態變更時，由媒體會話引發。                                                                                       |
| [MESinkInvalidated](mesinkinvalidated.md)                                                   | 當媒體接收變成無效時引發。                                                                                                                |
| [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md)                         | 當來源的特性變更時由媒體來源引發。                                                                                       |
| [MESourceMetadataChanged](mesourcemetadatachanged.md)                                       | 當媒體來源更新其中繼資料時引發。                                                                                                   |
| [MESourcePaused](mesourcepaused.md)                                                         | 當 [**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) 方法以非同步方式完成時，由媒體來源引發。                                 |
| [MESourceRateChanged](mesourceratechanged.md)                                               | 當播放速率變更時由媒體來源引發。                                                                                                 |
| [MESourceRateChangeRequested](mesourceratechangerequested.md)                               | 由媒體來源引發，以要求新的播放速率。                                                                                                 |
| [MESourceSeeked](mesourceseeked.md)                                                         | 當媒體來源搜尋至新位置時引發。                                                                                                      |
| [MESourceStarted](mesourcestarted.md)                                                       | 媒體來源啟動但未搜尋時引發。                                                                                                       |
| [MESourceStopped](mesourcestopped.md)                                                       | 當 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法以非同步方式完成時，由媒體來源引發。                                   |
| [MEStreamFormatChanged](mestreamformatchanged.md)                                           | 當資料流程的媒體類型變更時，由媒體資料流程引發。                                                                                      |
| [MEStreamPaused](mestreampaused.md)                                                         | 當 [**IMFMediaSource：:P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) 方法以非同步方式完成時，由媒體資料流程引發。                                 |
| [MEStreamSeeked](mestreamseeked.md)                                                         | 在呼叫 [**IMFMediaSource：： Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) 之後由媒體資料流程引發，會在資料流程中進行搜尋。                              |
| [MEStreamSinkDeviceChanged](mestreamsinkdevicechanged.md)                                   | 如果影片裝置變更，則由 EVR 的串流接收器引發。                                                                                       |
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)                                   | 當接收的媒體類型不再有效時，由資料流程接收器引發。                                                                                   |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                                                 | 在呼叫 [**IMFStreamSink：:P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) 方法之後，由資料流程接收器引發。                                      |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                                                 | 當資料流程接收完成轉換為暫停狀態時引發。                                                                            |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                                           | 資料流程接收到足夠的預先產生資料以開始轉譯時，由資料流程接收器引發。                                                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                                       | 當速率變更時由資料流程接收器引發。                                                                                                       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)                                   | 由資料流程接收器引發，以從管線要求新的媒體範例。                                                                                 |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md)                       | 當資料流程接收完成清除要求時引發。                                                                                           |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                                               | 當資料流程接收完成轉換到執行中狀態時引發。                                                                           |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                                               | 當資料流程接收完成轉換至已停止狀態時引發。                                                                           |
| [MEStreamStarted](mestreamstarted.md)                                                       | 當來源啟動但未搜尋時，由媒體資料流程引發。                                                                                         |
| [MEStreamStopped](mestreamstopped.md)                                                       | 當 [**IMFMediaSource：： Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) 方法以非同步方式完成時，由媒體資料流程引發。                                   |
| [MEStreamThinMode](mestreamthinmode.md)                                                     | 由媒體資料流程啟動或停止 thinning 資料流程時引發。                                                                                    |
| [MEStreamTick](mestreamtick.md)                                                             | 表示媒體資料流程沒有可在指定時間提供資料的信號。                                                                            |
| [METransformDrainComplete](metransformdraincomplete.md)                                     | 當清空作業完成時，由非同步媒體基礎轉換 (MFT) 傳送。                                                             |
| [METransformHaveOutput](metransformhaveoutput.md)                                           | 當可從 MFT 取得新的輸出資料時，由非同步 MFT 傳送。                                                                              |
| [METransformMarker](metransformmarker.md)                                                   | 由非同步 MFT 傳送以回應 [**MFT \_ 訊息 \_ 命令 \_ 標記**](mft-message-command-marker.md) 訊息。                               |
| [METransformNeedInput](metransformneedinput.md)                                             | 由非同步 MFT 傳送以要求新的輸入範例。                                                                                               |
| [MEUnknown](meunknown.md)                                                                   | 未知的事件種類。                                                                                                                                      |
| [MEUpdatedStream](meupdatedstream.md)                                                       | 當媒體來源重新開機或搜尋已在使用中的資料流程時引發。                                                                      |
| [MEVideoCaptureDevicePreempted](mevideocapturedevicepreempted.md)                           | 裝置已被佔用。                                                                                                                           |
| [MEVideoCaptureDeviceRemoved](mevideocapturedeviceremoved.md)                               | 裝置已移除。                                                                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎程式設計參考](media-foundation-programming-reference.md)
</dt> <dt>

[媒體事件產生器](media-event-generators.md)
</dt> <dt>

[**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




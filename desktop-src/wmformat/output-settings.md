---
title: 輸出設定
description: 輸出設定
ms.assetid: effe6c07-e6df-45b0-b865-2a025c466d6f
keywords:
- Windows媒體格式 SDK，全域常數
- Advanced Systems Format (ASF) 、global 常數
- ASF (Advanced Systems Format) ，global 常數
- 全域常數，清單
- Windows媒體格式 SDK，常數
- Advanced Systems Format (ASF) ，常數
- ASF (Advanced Systems Format) ，常數
- 常數，清單
- Windows媒體格式 SDK，輸出設定
- Advanced Systems Format (ASF) ，輸出設定
- ASF (Advanced Systems Format) ，輸出設定
- 輸出設定
- 同步讀取器，輸出設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966cd350d379170f9f19c44967ef932bf41a15cb1910b865432ce499b006161e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929938"
---
# <a name="output-settings"></a>輸出設定

下列全域常數用來識別讀取器和同步讀取器物件的輸出設定。



| 全域常數                | WMT \_ ATTR \_ 資料類型  | *PValue* 的描述                                                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszAllowInterlacedOutput    | **WMT \_ 類型 \_ BOOL**  | 若為 True，則讀取器會提供交錯的框架（如果輸出支援的話）。                                                                                                                                                                                                                                            |
| g \_ wszDedicatedDeliveryThread  | **WMT \_ 類型 \_ BOOL**  | 若為 True，則此輸出將會建立專用線程來傳遞其範例。 在同步讀取器上不支援。                                                                                                                                                                                            |
| g \_ wszDeliverOnReceive         | **WMT \_ 類型 \_ BOOL**  | 若為 True，此輸出的範例將會在從讀取器中提供時立即傳遞。 這可能會導致此輸出中的範例依序傳遞，以及來自其他輸出的對應樣本。                                                                                            |
| g \_ wszDynamicRangeControl      | **WMT \_ 類型 \_ DWORD** | 指定要用於輸出的動態範圍控制項層級。 設定為0到2的值，其中0表示不 (預設) 的動態範圍控制項，而2是動態範圍控制項 (最小動態範圍) 的最大層級。                                                                                |
| g \_ wszEarlyDataDelivery        | **WMT \_ 類型 \_ DWORD** | 時間，以毫秒為單位，指定傳遞範例之前的頻率。 如果大於零，則會取出此輸出中的範例，並將其解碼，以便比其他輸出的範例更早傳遞範例。 讀取器通常會依簡報時間的順序來傳遞範例。         |
| g \_ wszEnableDiscreteOutput     | **WMT \_ 類型 \_ BOOL**  | 若為 True，則讀取器會啟用高定義、多頻道音訊輸出。 這項設定僅適用于以 Windows Media 音訊 9 Professional 編解碼器編碼的音訊串流。 如果此設定設為 true，您也必須藉由設定 g wszSpeakerConfig 來指定用戶端電腦的說話者設定 \_ 。 |
| g \_ wszEnableFrameInterpolation | **WMT \_ 類型 \_ BOOL**  | 若為 True，則編解碼器會以更高的 [*畫面播放速率*](wmformat-glossary.md)傳遞影片串流，並將畫面格演算法。                                                                                                                                                          |
| g \_ wszJustInTimeDecode         | **WMT \_ 類型 \_ BOOL**  | 若為 True，則資料必須盡可能地解碼為最晚。 在同步讀取器中不支援。                                                                                                                                                                                                                            |
| g \_ wszNeedsPreviousSample      | **WMT \_ 類型 \_ BOOL**  | 若為 true，則範例需要解壓縮先前的範例。 這項設定只適用于壓縮影片中的差異框架，而且是唯讀的。                                                                                                                                                                       |
| g \_ wszScrambledAudio           | **WMT \_ 類型 \_ BOOL**  | 若為 True，則此輸出將使用未編碼的音訊錯誤 concealment 配置。 這只是音訊輸出的有效設定。                                                                                                                                                                                                |
| g \_ wszSingleOutputBuffer       | **WMT \_ 類型 \_ BOOL**  | 若為 True，就必須使用單一輸出緩衝區 (例如，DirectDraw®的影片緩衝區) 。 在同步讀取器中不支援。                                                                                                                                                                                           |
| g \_ wszSoftwareScaling          | **WMT \_ 類型 \_ BOOL**  | 若為 False，則不會調整影片的規模。  (的解決方式不能變更。 )                                                                                                                                                                                                                                                 |
| g \_ wszSpeakerConfig            | **WMT \_ 類型 \_ DWORD** | 如果透過設定 g wszEnableDiscreteOutput 來啟用多頻道音訊解碼 \_ ，此設定會指定用戶端電腦的說話者設定。 設定為其中一個 DirectSound 喇叭設定常數。                                                                                                   |
| g \_ wszStreamLanguage           | **WMT \_ 類型 \_ 文字**  | 要針對此輸出傳遞之語言的語言清單中的索引。 用於表示依語言相互排斥的資料流程輸出。                                                                                                                                                                      |
| g \_ wszVideoSampleDurations     | **WMT \_ 類型 \_ BOOL**  | 若為 True，則讀取器會提供精確的取樣持續時間。                                                                                                                                                                                                                                                                |
| g \_ wszEnableWMAProSPDIFOutput  | **WMT \_ 類型 \_ BOOL**  | 若為 True，則讀取器會在列舉輸出類型中包含索尼/梅花數位介面格式 (S/PDIF) 。                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReaderAdvanced2::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getoutputsetting)
</dt> <dt>

[**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**IWMSyncReader::GetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputsetting)
</dt> <dt>

[**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting)
</dt> </dl>

 

 





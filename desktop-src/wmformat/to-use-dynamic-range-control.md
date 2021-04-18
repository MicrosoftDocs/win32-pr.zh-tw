---
title: 若要使用動態範圍控制項
description: 若要使用動態範圍控制項
ms.assetid: 719658c1-952f-4e8f-a3ea-bdf89a0a7268
keywords:
- Windows Media Format SDK，動態範圍控制項
- Windows Media Format SDK，Windows Media 音訊 9 Professional 編解碼器
- Windows Media 格式 SDK，Windows Media 音訊9無失真編解碼器
- Advanced Systems Format (ASF) 、Windows Media 音訊 9 Professional 編解碼器
- ASF (Advanced Systems Format) 、Windows Media 音訊 9 Professional 編解碼器
- Advanced Systems Format (ASF) 、Windows Media 音訊9無失真編解碼器
- ASF (Advanced Systems Format) ，Windows Media 音訊9無失真編解碼器
- Advanced Systems Format (ASF) 、動態範圍控制
- ASF (Advanced 系統格式) 、動態範圍控制
- 動態範圍控制項
- 編解碼器，Windows Media 音訊9無失真編解碼器
- 編解碼器，Windows Media 音訊 9 Professional 編解碼器
- Windows Media 音訊9無失真編解碼器，動態範圍控制
- Windows Media 音訊 9 Professional 編解碼器，動態範圍控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 077ebc0052d0154aec395f371a5c2dc3ffd46c67
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965414"
---
# <a name="to-use-dynamic-range-control"></a>若要使用動態範圍控制項

一段音訊內容的動態範圍基本上是最低磁片區與最大磁片區之間的差異。 如果內容的動態範圍太高，使用者可能會在播放期間重複調整音量。 例如，電影通常會有很高的動態範圍。 通常，當調整磁片區，以便在無訊息的場景期間瞭解對話時，電影的其他部分會有音樂或音效效果，而不是所需的部分。

Windows Media 音訊 9 Professional 和 Windows Media 音訊9無失真編解碼器支援稱為動態範圍控制的功能。 編碼時，編解碼器會計算內容中的尖峰和平均波幅值，而寫入器物件會在編碼完成時，將這些值儲存在資料流程的中繼資料中。 或者，應用程式也可以撰寫「目標」值做為中繼資料，讓播放機應用程式和解碼器在播放檔案時可以用來做為提示。 在播放期間，應用程式可以指定要套用到音訊資料流程的動態範圍控制層級。

Windows Media Player 將動態範圍控制項實作為無訊息模式功能。

## <a name="when-to-use-dynamic-range-control"></a>使用動態範圍控制的時機

動態範圍控制項可以改變內容的音效。 基於這個理由，您不應該將應用程式設定為自動使用動態範圍控制。 相反地，請提供使用者視需要開啟或關閉動態範圍控制的能力。

## <a name="using-dynamic-range-control"></a>使用動態範圍控制項

在播放時，會使用輸出設定 g wszDynamicRangeControl 來啟用動態範圍控制項 \_ 。 使用 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) 來設定設定。 值為零 (預設) 表示不應更改動態範圍。 1或2的值表示要執行動態範圍控制的編解碼器，其中1是動態範圍壓縮的中等層級，而2則是高層級的動態範圍壓縮。

在編碼時間或播放時間，您可以分別設定 [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md) 和 [**wm/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md) 屬性，為尖峰和平均層級提供編解碼器目標 PCM 值。 這些值會儲存為中繼資料屬性，而且應該使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的方法來存取。 當您使用 professional 或無失真編解碼器編碼音訊串流時，會自動將 [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md) 和 [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md) 屬性設定為原始內容的尖峰和平均層級。 根據預設，目標值會設定為與參考相同的值。

在播放時，解碼器會根據選取的動態範圍控制項層級以及目標值 (（如果有指定) ）來計算動態範圍。 下表顯示可能的範圍。



| 設定                                                                | 傳遞的音訊範圍                                                                                                     |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDynamicRangeControl = 0 (任何目標值)                        | 與原始內容相同的範圍。                                                                                          |
| g \_ wszDynamicRangeControl = 1 (目標值等於參考值)  | 平均層級會維持不變，且尖峰限制為平均 + 12 資料庫。                                                    |
| g \_ wszDynamicRangeControl = 2 (目標值等於參考值)  | 平均層級會維持不變，且尖峰限制為平均 + 6 資料庫。                                                     |
| g \_ wszDynamicRangeControl = 1 (指定的目標值)                  | 平均層級設定為目標平均值，且尖峰限制為目標尖峰值。                                   |
| g \_ wszDynamicRangeControl = 2 (指定的目標值)                  | 平均層級設定為目標平均值，尖峰限制為目標平均和目標尖峰值的中位數。 |



 

請注意，動態範圍控制項是僅解碼的功能，而且只存在於檔案本身的中繼資料中。 這些設定不會影響儲存在檔案中的內容，除非您特別指示解碼器使用它們。 Windows Media Format SDK 不提供任何方法，可在編碼時間修改音訊資料的動態範圍。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Advanced 主題**](advanced-topics.md)
</dt> </dl>

 

 





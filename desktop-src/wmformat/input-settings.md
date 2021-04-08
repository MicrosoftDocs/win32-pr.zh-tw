---
title: 輸入設定
description: 輸入設定
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media Format SDK，全域常數
- Advanced Systems Format (ASF) 、global 常數
- ASF (Advanced Systems Format) ，global 常數
- 全域常數，清單
- Windows Media Format SDK，常數
- Advanced Systems Format (ASF) ，常數
- ASF (Advanced Systems Format) ，常數
- 常數，清單
- Windows Media Format SDK，輸入設定
- Advanced Systems Format (ASF) ，輸入設定
- ASF (Advanced Systems Format) ，輸入設定
- 輸入設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023009"
---
# <a name="input-settings"></a>輸入設定

下列全域常數用來識別寫入器的輸入設定。



| 全域常數                        | WMT \_ ATTR \_ 資料類型                                                                                                                       | *PValue* 的描述                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_在 \_** 主題中，將 [DWORD] 類型設定為 [模式] 資料表中的其中一個值 [，以將影片進行逐行掃描](to-deinterlace-video.md)。            | 設定時，指定輸入的交錯內容類型。 如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。                                                                                                                            |
| g \_ wszFixedFrameRate                   | **WMT \_ 類型 \_ BOOL**                                                                                                                       | 當設為 True 時，會指示編解碼器不要在編碼期間卸載任何框架。 這會導致輸出影片資料流程的 [*畫面播放速率*](wmformat-glossary.md) 是常數。 輸入資料流程的畫面播放速率不需要是常數。 |
| g \_ wszInitialPatternForInverseTelecine | **WMT \_在 \_** 主題中，將 [DWORD] 類型設定為 [初始模式] 資料表中的其中一個值 [，以將影片進行逐行掃描](to-deinterlace-video.md)。 | 當 [交錯模式] 設定為 [WM \_ DM \_ 交錯] INVERSETELECINE 時，您 \_ 可以將此設定為指定 [*電影*](wmformat-glossary.md) 輸入的模式。 如需詳細資訊，請參閱 [將影片進行逐行掃描](to-deinterlace-video.md)。        |
| g \_ wszInterlacedCoding                 | **WMT \_ 類型 \_ BOOL**                                                                                                                       | 設定為 True 時，會指定編解碼器應該將資料流程編碼為交錯式內容。 如需詳細資訊，請參閱 [使用交錯式影片](to-use-interlaced-video.md)。                                                                                       |
| g \_ wszJPEGCompressionQuality           | **WMT \_ 類型 \_ DWORD**                                                                                                                      | 指定要用於輸入的 JPEG 品質層級 (從1到 100) 。                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **WMT \_ 類型 \_ GUID**                                                                                                                       | 值設定為浮水印 GUID。                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **WMT \_ 類型 \_ 字串**                                                                                                                     | 值設定為水位線設定。 此值會視浮水印的值而異。 如需詳細資訊，請參閱浮水印系統的檔。                                                                                   |



 

> [!Note]  
> 針對資料流程設定的輸入設定不會保存在寫入的檔案中。 如果您想要讓自訂讀取器擁有這些編碼參數的存取權，您必須建立自訂屬性，以將它們儲存在檔案標頭中。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 





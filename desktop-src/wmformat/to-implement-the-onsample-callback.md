---
title: 若要執行 OnSample 回呼
description: 若要執行 OnSample 回呼
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- 先進的系統格式 (ASF) ，實 OnStatus 回呼
- ASF (Advanced Systems Format) ，執行 OnStatus 回呼
- Advanced Systems Format (ASF) 、OnStatus 回呼
- ASF (Advanced Systems Format) 、OnStatus 回呼
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- 非同步讀取器，執行 OnStatus 回呼
- OnStatus 回呼方法，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00523ae28ec14feefb8249ff86a2b1600629c84cb245eb627b59b619a28a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027286"
---
# <a name="to-implement-the-onsample-callback"></a>若要執行 OnSample 回呼

非同步讀取器會呼叫 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 回呼方法，以展示時間順序提供範例給控制應用程式。 當您使用非同步讀取器來建立應用程式時，您必須執行 **OnSample** 來處理未壓縮的範例。 通常會從 **OnSample** 中呼叫為了轉譯內容而建立的函式或方法。

**OnSample** 回呼的一般實作為包含下列步驟。

1.  藉由在傳遞為 *pSample* 的緩衝區上呼叫 [**INSSBuffer：： GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) ，以抓取包含範例的緩衝區位置和大小。
2.  根據輸出編號來分支您的邏輯。 輸出編號會以 *dwOutputNumber* 的形式傳遞至 **OnSample** 。
3.  針對您想要支援的每個輸出編號，包含轉譯邏輯。 如果您要從多個輸出呈現範例，您可能需要同步處理您的轉譯。

從 ASF 檔案傳遞壓縮範例的應用程式需要執行 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼方法。 **OnStreamSample** 函式幾乎與 **OnSample** 相同，不同之處在于它會依串流號碼接收壓縮的樣本，而不是依輸出編號來取得未壓縮的樣本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReaderCallback 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[**IWMReaderCallbackAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**使用回呼方法**](using-the-callback-methods.md)
</dt> </dl>

 

 





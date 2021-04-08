---
title: 使用非同步讀取器傳遞壓縮的範例
description: 使用非同步讀取器傳遞壓縮的範例
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- 先進的系統格式 (ASF) ，傳遞壓縮的範例
- ASF (Advanced Systems Format) ，傳遞壓縮的範例
- Advanced Systems Format (ASF) 、非同步讀取器
- ASF (Advanced 系統格式) 、非同步讀取器
- Advanced Systems Format (ASF) 、壓縮的範例
- ASF (Advanced Systems Format) ，壓縮的範例
- 非同步讀取器，傳遞壓縮的範例
- 非同步讀取器，壓縮的範例
- 壓縮的範例，傳遞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681418"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>使用非同步讀取器傳遞壓縮的範例

非同步讀取器可以從 ASF 檔案中的串流傳遞壓縮的範例。 應用程式通常會在將資料流程從一個檔案複製到另一個檔案時，提供壓縮的範例。 建議您重新壓縮已從壓縮的資料流程重建的資料，因為編碼程式中的資料會遺失。 已壓縮超過一次的數位媒體將會明顯降低品質。

Windows Media Format SDK 不提供任何方法，可在資料從 ASF 檔案解壓縮之後進行解碼。 如果您收到壓縮的範例，之後想要將它們解壓縮，您必須提供自己的程式碼來進行。 解決這項限制的其中一種方法是將壓縮的範例寫入至新的 ASF 檔案，然後將它們重新讀取為一般、未壓縮的範例。

若要使用非同步讀取器來接收壓縮的範例，請執行下列步驟。

1.  執行 [**IWMReaderCallbackAdvanced：： OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) 回呼。 此回呼基本上與 [**IWMReaderCallback：： OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) 的函式相同，不同之處在于它會依串流號碼提供範例，且範例仍會進行壓縮。
2.  開始播放之前，請藉由呼叫 **IWMReader：： QueryInterface** 來取得讀取器物件之 [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)介面的指標。
3.  藉由呼叫 [**IWMReaderAdvanced：： SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)，設定讀取器以傳遞所需資料流程的壓縮範例。
4.  針對需要壓縮範例傳遞的每個資料流程重複步驟3。

> [!Note]  
> 影像串流對壓縮的資料流程傳遞而言無效。 如果您將影像串流從某個檔案複製到另一個檔案，它就無法在新的檔案中使用。 若要從檔案複製影像串流至檔案，請依輸出號碼抓取影像串流範例，並將它們包含在新的檔案中，如同包含新的影像串流一樣。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMReaderCallbackAdvanced 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**使用非同步讀取器讀取檔案**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 





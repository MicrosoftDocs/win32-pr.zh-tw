---
title: 使用同步讀取器取出媒體範例
description: 使用同步讀取器取出媒體範例
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Advanced Systems Format (ASF) ，正在抓取媒體範例
- ASF (Advanced 系統格式) ，正在抓取媒體範例
- Advanced Systems Format (ASF) 、同步讀取器
- ASF (Advanced Systems Format) ，同步讀取器
- 同步讀取器，正在抓取媒體範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1ec4fc7e8a894de304ea828cef9d8e019f4cdedfd2fbd851a427382ba741a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807428"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>使用同步讀取器取出媒體範例

您必須從同步讀取器一次要求一個範例。 這可讓您更充分掌控所收到的範例，以及接收這些樣本的時間。

使用 [**IWMSyncReader：： GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) 方法來取出範例。 您必須將大部分的指標傳遞給變數，這些變數將會填入抓取為參數之範例的相關資訊。 唯一的輸入參數是 *wStreamNum*。 如果您傳遞串流號碼， **GetNextSample** 將會使用指定的資料流程號碼來取得下一個樣本。 如果您傳遞零給 *wStreamNum*，則會抓取在檔案中時間先後出現的下一個範例。

根據預設，同步讀取器會依時間順序從檔案的輸出中抓取所有範例。 如果您呼叫 **GetNextSample** ，而且沒有其他要取得的範例，它會傳回 NS \_ E \_ no \_ 其他 \_ 範例，也就是失敗的錯誤碼。 因此，在撰寫程式碼時，您可以只對範例執行迴圈，直到方法失敗為止。

> [!Note]  
> 若要確保同步讀取器能為影片串流提供正確的取樣持續時間，您必須先設定資料流程輸出。 呼叫 [**IWMSyncReader：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) 方法，將 g \_ wszVideoSampleDurations 設定設定為 **TRUE**。

 

範例程式碼

下列範例程式碼示範如何使用 **GetNextSample** 來取出檔案中的所有範例。


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IWMSyncReader 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**使用同步讀取器讀取檔案**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 





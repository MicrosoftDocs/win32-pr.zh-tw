---
description: CVideoTransformFilter 類別主要是用來做為 AVI 解壓縮程式篩選準則的基類。
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: a1e1a1b717aeb2814b469fc34a9e038052abb6720dde0ed75982f27716978de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907001"
---
# <a name="cvideotransformfilter-class"></a>CVideoTransformFilter 類別

![cvideotransformfilter 類別階層](images/vtsip01.png)

`CVideoTransformFilter`類別主要是用來做為 AVI 解壓縮程式篩選準則的基類。 此類別會將品質控制的支援新增至 [**CTransformFilter**](ctransformfilter.md) 類別。 篩選器的 **Receive** 方法可以決定要根據轉譯器中的品質訊息和篩選器在串流處理時所收集的效能測量，來卸載畫面格。

如果篩選器卸載框架，則會繼續卸載框架，直到到達下一個主要畫面格為止。 針對 MPEG 資料流程，篩選不會區分 B 框架和 P 框架。



| 受保護的成員變數                                                      | Description                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | 指出篩選是否已卸載框架。                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | 指出篩選目前是否正在卸載框架。                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | 用來解碼框架的平均時間長度。                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | 表示樣本到達轉譯器的延遲。                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | 自最後一個主要畫面格之後，篩選所收到的框架數目。                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | 主要畫面格之間的最大觀察間隔。                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | 要卸載之 delta 框架的目前最大數目。                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | 解碼最新範例所花費的時間長度。                                  |
| 保護方法                                                               | Description                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | 用來發出串流錯誤的信號。                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | 通知篩選準則要求品質變更。                                        |
| [**收到**](cvideotransformfilter-receive.md)                                | 接收媒體範例、處理它，然後將輸出範例傳遞給下游篩選器。 |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | 判斷篩選是否應卸載指定的範例。                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | 當篩選參數切換為暫停狀態時呼叫。                                           |
| 公用方法                                                                  | Description                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | 函式方法。                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | 結束清除操作。                                                                        |



 

 

 




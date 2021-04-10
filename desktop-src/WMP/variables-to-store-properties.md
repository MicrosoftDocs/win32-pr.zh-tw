---
title: 用來儲存屬性的變數
description: 用來儲存屬性的變數
ms.assetid: a90a6e21-00fb-46f8-96c8-654d8f205905
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，屬性
- Echo DSP 外掛程式範例，用於儲存屬性的變數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d252962116ba9c72464273f9c4ea1688b151898
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183670"
---
# <a name="variables-to-store-properties"></a>用來儲存屬性的變數

首先，您將需要一個變數來儲存延遲時間。 Windows Media Player 外掛程式 Wizard 建立的預設範例會提供名為 m fScaleFactor 的變數 \_ ，以儲存它用來處理的縮放乘數。 此範例不再需要這個變數，因此您可以變更其名稱和類型來儲存延遲時間值。

1.  以 m dwDelayTime 取代 Echo 中的每個 m \_ fScaleFactor 實例和回應。 \_
2.  變更 m fScaleFactor 的資料類型 \_ (現在 m \_ dwDelayTime) 從 DOUBLE 到 DWORD 的 Echo. h。
3.  在 CEcho 的函式中，將預設的延遲時間值變更為1000。
    ```C++
    m_dwDelayTime = 1000;   // Default to a delay time of 1000 ms.
    
    ```

    

接下來，宣告兩個新的成員變數，以儲存效果信號的百分比，以及要在最終輸出緩衝區中混合的來源信號百分比。 「濕」一詞是指效果，而「幹」一詞是指來源信號。 將下列宣告新增至 Echo：


```C++
double  m_fWetMix;    // percentage of effect
double  m_fDryMix;    // percentage of dry signal

```



這些值會儲存為百分比的十進位標記法，因此可以輕鬆地當做比例因數使用。 例如，50% 效果和50% 來源信號的組合會以每個變數的0.50 值表示。 M \_ fWetMix 和 m fDryMix 值的總和不得超過 \_ 1.0 (100%) 。 最後，這些值將可作為屬性來存取。

將下列程式碼新增至 CEcho 的函式，以將預設值設定為50%：


```C++
m_fWetMix = 0.50;  // default to 50 percent wet
m_fDryMix = 0.50;  // default to 50 percent dry

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例屬性**](echo-sample-properties.md)
</dt> </dl>

 

 





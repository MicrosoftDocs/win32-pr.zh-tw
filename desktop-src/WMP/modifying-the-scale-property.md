---
title: 修改尺規屬性
description: 修改尺規屬性
ms.assetid: 32ebaa54-ed13-4b10-8876-bf8e188d7317
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性
- 外掛程式，Echo 範例屬性
- 數位信號處理外掛程式，Echo 範例屬性
- DSP 外掛程式，Echo 範例屬性
- Echo DSP 外掛程式範例，小數位數屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10073e01213469dcb6a85ddffd378421fddb6ae8f2fd432b9822c3a5046fdd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574615"
---
# <a name="modifying-the-scale-property"></a>修改尺規屬性

預設的 wizard 執行會公開 scale 屬性。 您可以變更現有的實作為，改為公開 [延遲時間] 屬性。

首先，使用下列範例來變更 \_ 在 Echo 中取得尺規和 put 縮放的函式原型 \_ 。 變更方法的名稱和參數的資料類型：


```C++
// IEcho methods
STDMETHOD(get_delay)(DWORD *pVal);
STDMETHOD(put_delay)(DWORD newVal);

```



接下來， \_ 在 Echo 中變更取得規模和 put \_ 調整方法的執行。 使程式碼符合下列範例：


```C++
// Formerly get_scale
STDMETHODIMP CEcho::get_delay(DWORD *pVal)
{
    if ( NULL == pVal )
    {
        return E_POINTER;
    }

    *pVal = m_dwDelayTime;

    return S_OK;
}

// Formerly put_scale
STDMETHODIMP CEcho::put_delay(DWORD newVal)
{
    m_dwDelayTime = newVal;

    return S_OK;
}

```



上述範例程式碼會變更方法名稱和參數資料類型。 成員變數名稱先前應該已經變更。 也請記得變更引進每個方法的批註。

現在，變更介面定義。 下列程式碼會取代 Echo 中 IEcho 介面宣告中的程式碼：


```C++
HRESULT get_delay([out] DWORD *pVal);
HRESULT put_delay([in] DWORD newVal);

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Echo 範例屬性**](echo-sample-properties.md)
</dt> </dl>

 

 





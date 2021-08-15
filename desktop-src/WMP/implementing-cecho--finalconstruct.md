---
title: 執行 CEcho FinalConstruct
description: 執行 CEcho FinalConstruct
ms.assetid: 149e99c5-9f57-4447-b520-39a6dd39fc86
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEcho FinalConstruct 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbeceeb9c0a7622ada62e98000ad4bfbc2e3faf08c22439039160810771cde8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748143"
---
# <a name="implementing-cechofinalconstruct"></a>執行 CEcho：： FinalConstruct

CEcho：： FinalConstruct 方法是在 Echo 中實作為。 它包含的程式碼可在 Windows Media Player 具現化 DSP 外掛程式物件時，從登錄讀取屬性值。 這點很重要，因為它可讓使用者設定在物件的實例之間以及會話之間保存。 外掛程式 wizard 範例程式碼提供從登錄讀取單一屬性的執行。 您可以修改此程式碼以處理 [延遲時間] 屬性，然後加入程式碼以讀取 [潮濕混合] 屬性值。

下列程式碼範例會從登錄讀取每個屬性值，並將每個屬性值儲存在正確的成員變數中：


```CSharp
CRegKey key;
LONG    lResult;
DWORD   dwValue;

lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
if (ERROR_SUCCESS == lResult)
{
    // Read the delay time from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
    if (ERROR_SUCCESS == lResult)
    {
        m_dwDelayTime = dwValue;
    }

    // Read the wet mix value from the registry. 
    lResult = key.QueryValue(dwValue, kszPrefsWetmix );
    if (ERROR_SUCCESS == lResult)
    {
        // Convert the DWORD to a double.
        m_fWetMix = (double)dwValue / 100;
        // Calculate the dry mix value.
        m_fDryMix = 1.0 - m_fWetMix;
    }

}

return S_OK;
```



請注意，濕混合的 DWORD 值會轉換成浮點值。 另請注意，程式碼會計算 m fDryMix 的正確值 \_ 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





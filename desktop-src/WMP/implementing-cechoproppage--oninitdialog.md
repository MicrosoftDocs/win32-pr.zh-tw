---
title: 執行 CEchoPropPage OnInitDialog
description: 執行 CEchoPropPage OnInitDialog
ms.assetid: 568989b0-bc07-480f-8b5c-41bbada713f8
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEchoPropPage OnInitDialog 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0874c750914b5caecf86ffa61a0c42d38bb1c02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967610"
---
# <a name="implementing-cechoproppageoninitdialog"></a>執行 CEchoPropPage：： OnInitDialog

**CEchoPropPage：： OnInitDialog** 方法是在 EchoPropPage 中執行。 它會在叫用 [屬性頁] 對話方塊時執行。 此方法中的程式碼需要取出目前的屬性值，並將它們顯示在正確的編輯方塊中。 外掛程式 wizard 範例程式碼會為單一屬性提供實作為。 您可以針對其中一個 Echo 範例屬性修改此程式碼，然後加入程式碼以取得第二個屬性值。

## <a name="declaring-the-oninitdialog-method-variables"></a>宣告 OnInitDialog 方法變數

首先，您必須移除 fScaleFactor 的宣告，並將其取代為下列變數聲明：


```
DWORD  dwDelayTime = 1000;    // Default delay time.
DWORD  dwWetmix = 50;         // Default wet mix DWORD.
double fWetmix =  0.50;       // Default wet mix double.
```



## <a name="retrieving-the-current-values-from-the-plug-in"></a>從外掛程式中取出目前的值

接著，程式碼應該會嘗試從回應外掛程式取得目前的屬性值。 下列範例會嘗試取得每個屬性：


```
if (m_spEcho)
{
    m_spEcho->get_delay(&dwDelayTime);
    m_spEcho->get_wetmix(&fWetmix);
    // Convert wet mix from double to DWORD.
    dwWetmix = (DWORD)(fWetmix * 100);
}
```



此對話方塊會將效果層級值顯示為整數，但外掛程式會將值儲存為浮點數。 因此，程式碼會將浮點值轉換為 **DWORD** 值。

## <a name="retrieving-the-current-values-from-the-registry"></a>從登錄中取出目前的值

如果屬性頁無法從外掛程式取得目前的值，它必須嘗試從登錄讀取它們。 下列程式碼會讀取每個屬性值：


```
else // Otherwise, read values from registry
{
    CRegKey key;
    LONG    lResult;

    lResult = key.Open(HKEY_CURRENT_USER, kszPrefsRegKey, KEY_READ);
    if (ERROR_SUCCESS == lResult)
    {
        DWORD   dwValue = 0;

        // Read the delay time.
        lResult = key.QueryValue(dwValue, kszPrefsDelayTime );
        if (ERROR_SUCCESS == lResult)
        {
            dwDelayTime = dwValue;
        }

        // Read the wet mix value.
        lResult = key.QueryValue(dwValue, kszPrefsWetmix );
        if (ERROR_SUCCESS == lResult)
        {
            dwWetmix = dwValue;
        }
    }
}
```



請注意您先前建立的登錄常數的使用。

## <a name="displaying-the-values-to-the-user"></a>向使用者顯示值

最後，屬性頁必須在正確的編輯方塊控制項中顯示值。 下列範例程式碼示範：


```
 TCHAR   szStr[MAXSTRING];

// Display the delay time.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwDelayTime);
SetDlgItemText(IDC_DELAYTIME, szStr);

// Display the effect level.
_stprintf_s(szStr, MAXSTRING, _T("%u"), dwWetmix);
SetDlgItemText(IDC_WETMIX, szStr);
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





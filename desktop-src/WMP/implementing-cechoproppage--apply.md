---
title: 實施 CEchoPropPage 適用
description: 實施 CEchoPropPage 適用
ms.assetid: e887b851-e623-4ec4-8d8b-165e4b21e116
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，CEchoPropPage Apply 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bdca8a771d3e3e26923567f25bf7d19e968595e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840199"
---
# <a name="implementing-cechoproppageapply"></a>執行 CEchoPropPage：： Apply

CEchoPropPage：： Apply 方法是在 EchoPropPage 中執行。 當使用者在 Windows Media Player 的 [屬性頁] 對話方塊 **中按一下 [** 套用] 時，就會執行此動作。 外掛程式 wizard 範例程式碼會提供處理單一屬性的執行。 您可以針對其中一個 Echo 範例屬性修改此程式碼，然後加入程式碼以儲存其他屬性值。

## <a name="declaring-the-apply-method-variables"></a>宣告 Apply 方法變數

首先，您必須移除 fScaleFactor 的宣告。 然後，新增您將需要的變數宣告。 下列範例顯示已完成的變數宣告：


```
TCHAR   szStr[MAXSTRING] = { 0 };
DWORD   dwDelayTime = 1000;  // Initialize the delay time.
DWORD   dwWetmix = 50;       // Initialize a DWORD for effect level.
double  fWetmix = 0.50;      // Initialize a double for effect level.
```



## <a name="retrieving-the-values-from-the-property-page"></a>從屬性頁中取出值

您必須執行程式碼，以取出並驗證使用者輸入。 下列程式碼範例會從 IDC \_ DELAYTIME 編輯方塊中抓取延遲時間值，然後確認值是否在指定的範圍內：


```
// Get the delay time value from the dialog box.
GetDlgItemText(IDC_DELAYTIME, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwDelayTime = atoi(szStr);

// Make sure delay time is valid.
if ((dwDelayTime < 10) || (dwDelayTime > 2000))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_DELAYRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



如果使用者輸入不在指定的範圍內，則程式碼會顯示訊息方塊。 請注意您稍早為錯誤訊息所建立的字串資源使用。

下列範例會從 IDC \_ WETMIX 編輯方塊中抓取效果等級，然後驗證值是否在指定的範圍內：


```
// Get the effects level value from the dialog box.
GetDlgItemText(IDC_WETMIX, szStr, sizeof(szStr) / sizeof(szStr[0]));

dwWetmix = atoi(szStr);

// Make sure wet mix value is valid.
if ((dwWetmix < 0) || (dwWetmix > 100))
{
    if (::LoadString(_Module.GetResourceInstance(), IDS_MIXRANGEERROR, szStr, sizeof(szStr) / sizeof(szStr[0])))
    {
        MessageBox(szStr);
    }

    return E_FAIL;
}
```



## <a name="storing-the-property-values-in-the-registry"></a>將屬性值儲存在登錄中

接下來，您的程式碼必須將新的屬性值保存到登錄中。 下列程式碼會儲存這兩個屬性值：


```
// update the registry
CRegKey key;
LONG    lResult;

// Write the delay time value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwDelayTime , kszPrefsDelayTime );
}

// Write the wet mix value to the registry.
lResult = key.Create(HKEY_CURRENT_USER, kszPrefsRegKey);
if (ERROR_SUCCESS == lResult)
{
    lResult = key.SetValue( dwWetmix , kszPrefsWetmix );
}
```



## <a name="updating-the-echo-plug-in-property-values"></a>更新 Echo 外掛程式屬性值

**Apply** 方法必須通知回應外掛程式屬性值已變更。 下列程式碼會使用在 CEchoPropPage：： SetObjects 中抓取的介面指標，呼叫每個屬性的屬性 put 方法：


```
// update the plug-in
if (m_spEcho)
{
    m_spEcho->put_delay(dwDelayTime);

    // Convert the wet mix value from DWORD to double.
    fWetmix = (double)dwWetmix / 100;
    m_spEcho->put_wetmix(fWetmix);
}
```



請注意，濕混合值會在傳遞至外掛程式之前轉換成浮點數。

## <a name="disabling-the-apply-button"></a>停用 [套用] 按鈕

在最後一個步驟中，您的程式碼應該會在 [屬性頁] 對話方塊中停用 [套用]，以通知使用者值已成功更新。 這需要下列一行程式碼：


```
m_bDirty = FALSE; // Tell the property page to disable Apply.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





---
description: 同步處理 DVD 命令
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: 同步處理 DVD 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38696425892618f1b66544e69a4a567d0f539234d991cb96792eda4f6f1509d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964808"
---
# <a name="synchronizing-dvd-commands"></a>同步處理 DVD 命令

DVD 命令不一定會立即完成。 基於這個理由， [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 中的某些方法是非同步。 這些包括播放方法（例如 **PlayTitle**）和功能表導覽方法（例如 **ShowMenu** 和 **ReturnFromSubmenu**）。 非同步方法會立即傳回，而不會等候命令完成。 在方法傳回之後，即使方法成功，其他事件也可能會導致命令無法完成。 DirectShow 提供數個選項來同步處理命令，範圍從無同步處理到使用篩選圖形事件的完整同步處理。

所有的非同步方法都有 *dwFlags* 參數和 *ppCmd* 參數。 *DwFlags* 參數會指定同步處理行為，而 *ppCmd* 參數會傳回選擇性同步處理物件的指標。 根據您提供給這些參數的值而定，會有不同的行為結果。

**無同步處理**

若是基本的 DVD 播放應用程式，最好的選擇就是忽略同步處理問題。 有時命令可能會失敗，或 UI 在更新時可能會稍微延遲一點，但這些錯誤會依秒數的順序排列。

若要發出無同步處理的命令，請 \_ \_ 在 dwFlags 參數中設定 DVD CMD 旗標 \_ None 旗標，並將 *PpCmd* 參數設定為 **Null**：


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**封鎖**

如果您 \_ \_ \_ 在 dwFlags 參數中設定 EC DVD CMD 旗標 \_ 封鎖旗標，方法會封鎖，直到命令完成為止： 


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



實際上，這個旗標會將非同步方法變成同步方法。 缺點是當您從應用程式執行緒呼叫方法時，您的 UI 會封鎖。

**同步處理物件**

所有的非同步方法都可以傳回同步處理物件，您可以用它來等候命令開始或結束。 若要取得此物件，請在 *ppCmd* 參數中傳遞 [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd)指標的位址：


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



如果方法成功，它會傳回新的 **IDvdCmd** 物件。 [**IDvdCmd：： WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart)方法會封鎖，直到命令開始，而 [**IDvdCmd：： WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend)方法會封鎖，直到命令結束為止。 傳回值指出命令的狀態。

下列程式碼在功能上等同于設定 EC \_ DVD \_ CMD \_ 旗標 \_ 封鎖旗標，如先前所示。


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



在此情況下， **PlayTitle** 方法不會封鎖，而是藉由呼叫 **WaitForEnd** 來封鎖應用程式。

**命令狀態事件**

如果您 \_ \_ 在 dwFlags 參數中設定 dvd cmd 旗標 \_ SendEvents 旗標，則當命令開始時，dvd 瀏覽器會傳送 [**ec \_ dvd \_ cmd \_ START**](ec-dvd-cmd-start.md)事件，而當命令結束時，則會傳送 [**ec \_ dvd \_ cmd \_ END**](ec-dvd-cmd-end.md)事件。 

事件的 *lParam2* 參數是命令的 HRESULT 傳回值。 事件的 *lParam1* 參數提供取得命令之同步處理物件的方式。 如果您將 *lParam1* 傳遞至 [**IDvdInfo2：： GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) 方法，則方法會傳回同步處理物件 **IDvdCmd** 介面的指標。 您可以使用此介面來等候命令完成（如先前所述）。 但是，如果您針對原始 **IDvdControl2** 方法中的 *PpCmd* 參數傳遞 **Null** ，則 DVD 導覽器不會建立同步處理物件，且 **GetCmdFromEvent** 會傳回 E \_ FAIL。

下列程式碼顯示如何使用沒有同步處理物件的命令狀態事件。


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



請注意，如果沒有同步處理物件，您就無法分辨哪一個命令與事件相關聯。 下列程式碼示範如何使用事件與同步處理物件。 其概念是將同步處理物件儲存在清單中，然後在您取得 [**EC \_ dvd \_ Cmd \_ START**](ec-dvd-cmd-start.md) 或 [**EC \_ dvd \_ cmd \_ 結束**](ec-dvd-cmd-end.md) 事件時比較物件指標。


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**清除 DVD Navigator 的緩衝區**

在播放期間，DVD 導覽器會緩衝影片資料。 緩衝的資料量會有所不同。 當 DVD 導覽器切換至新的影片時，已在管線中的資料不會遺失，因此轉換會順暢。 根據預設，當 DVD 導覽器發出命令時，它不會排清已在管線中的資料。 如此一來，可能會有一些延遲，您才能看到命令的效果，視緩衝的資料量而定。 若要增加回應能力，您可以設定 DVD CMD 旗標排清旗標來強制讓 DVD Navigator 排清 \_ \_ \_ 。


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



此旗標可以與先前所述的任何旗標結合使用位 OR。 清除的副作用是某些影片可能會遺失，因此，如果您需要保證影片中沒有間距，請不要使用此旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DVD 應用程式](dvd-applications.md)
</dt> </dl>

 

 




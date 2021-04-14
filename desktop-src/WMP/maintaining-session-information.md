---
title: 維護會話資訊
description: 維護會話資訊
ms.assetid: 2ab862dc-62e1-44d6-ac81-7d3c574a779f
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player 線上商店，維護會話資訊
- 線上商店，維護會話資訊
- 輸入2個線上商店，維護會話資訊
- Windows Media Player 線上商店、會話資訊
- 線上商店、會話資訊
- 輸入2個線上商店、會話資訊
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 維護會話資訊
- 會話資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786892afebb26f64a97b300bd1a4bd7c46d44883
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311540"
---
# <a name="maintaining-session-information"></a>維護會話資訊

## <a name="how-the-sample-stores-information"></a>範例如何儲存資訊

範例網頁會使用 cookie 來維護資料。 Cookie 只是網頁瀏覽器可為您儲存的持續性名稱/值配對。

當網頁關閉時，就會執行 **關機** 功能。 **Shutdown** 會呼叫 **SetPendingCookies** 函數。 此函式會透過下載集合清單來迴圈，該清單會儲存在名為 selDLC 的下拉式清單方塊中。 如果下載集合包含未完成的專案，則函式會呼叫 **system.windows.application.setcookie** 方法，並傳遞名稱和值。 名稱字串的判斷方式是將整數值附加至常數值 **WMPDLC**，此值會儲存在名為 g sPreCookie 的變數中 \_ 。 例如，針對第三個暫止的下載集合，cookie 名稱會是 "WMPDLC2"，因為電腦制是以零為基底。 當每個 cookie 建立時，函式會將全域變數 g 暫止， \_ 以保留暫止下載的計數。 為了方便起見，我們會在這裡重現程式碼：


```C++
// Write cookies for pending downloads.
function SetPendingCookies()
{
    g_Pending = 0; // Init the pending count.
    
    for(var i = 0; i < selDLC.length; i++)
    {
        var sCookieName = g_sPreCookie + i.toString(10);
        var sCookieVal = selDLC.options[i].text;
    
        // Write a cookie for each pending download.    
        if(IsDLCComplete(sCookieVal.valueOf()) == false)
        {      
            SetCookie(sCookieName, sCookieVal);
            g_Pending++;
        }        
    }
}

```



**IsDLCComplete** 是 helper 函式，只會在下載集合中的每個下載專案之間進行迴圈，以判斷是否有任何專案擱置。 如果有暫止的專案，函數會傳回 false。

**System.windows.application.setcookie** 是建立 cookie 的函式。

當 **SetPendingCookies** 傳回時， **Shutdown** 會建立計數 cookie，以儲存來引數 g 的值 \_ 。 此值很重要，因為網頁需要一種方式來決定重載時要取出的 cookie 數目。 計數 cookie 名稱會儲存在名為 g sCountCookie 的變數中 \_ 。

## <a name="how-the-sample-retrieves-information"></a>範例如何捕獲資訊

當網頁載入時， **Init** 函式就會執行。 首先，此函式會呼叫 **GetPendingDlCount** 來取得計數 cookie。 接下來，它會將此值儲存在名為 g Pending 的變數中 \_ 。 然後，它會呼叫 **PopulateDLList** 函式，以抓取每個下載會話 cookie，並將其識別碼新增至下拉式清單方塊。 以下是該函式的程式碼：


```C++
// Fill the drop-down list with pending download collection IDs.
function PopulateDlList(iCount)
{
    ClearList(selDLC);
     
    // For each cookie, add the value to the SELECT element.
    // The value represents a download collection ID.  
    for (var j = 0; j < iCount; j++)
    {
        var sCookieName = g_sPreCookie + j.toString(10);        
        var sCookieVal = GetCookie(sCookieName);
        DelCookie(sCookieName); // Don't leave the cookies lying around. 
  
        if(sCookieVal != null)
        {      
            var oOption = document.createElement("OPTION");
            oOption.text = sCookieVal;
            oOption.value = j;
            selDLC.add(oOption); 
        }          
    }
}

```



函數 **ClearList** 會從清單方塊中移除所有專案。

然後，函數會進入迴圈。 每個 cookie 名稱都是以字串的形式建立，然後藉由呼叫 helper 函式 **system.windows.application.getcookie** 來取出 cookie。 一旦抓取之後，cookie 就會藉由呼叫 **DelCookie** 來刪除。 如果 cookie 有值，則會將值加入清單方塊中。 此動作會起始 selDLC 清單的 **onChange** 事件，然後再呼叫名為 **OnSelectDLC** 的處理常式函式。 這是使用者選取下載集合時所執行的相同功能;這是填入 [下載專案] 清單方塊的程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**使用下載管理員**](using-the-download-manager.md)
</dt> </dl>

 

 





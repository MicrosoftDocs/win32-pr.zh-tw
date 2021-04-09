---
title: Server-Side 設計
description: 伺服器端函式會透過 windows 外部物件與用戶端 wizard 進行通訊。 伺服器端腳本會提供這些函式來回應 wizard 事件，以及取得有關 wizard 的資訊。
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- 發佈嚮導，伺服器端設計
- '[外部]、[發行] 嚮導'
- 發佈嚮導，window. 外部
- 發佈嚮導，導覽腳本函式
- 腳本，發佈嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933245"
---
# <a name="server-side-design"></a>Server-Side 設計

伺服器端函式會透過 **windows 外部** 物件與用戶端 wizard 進行通訊。 伺服器端腳本會提供這些函式來回應 wizard 事件，以及取得有關 wizard 的資訊。

本檔涵蓋下列主題。

-   [執行導覽腳本函數](#implementing-navigation-script-functions)
    -   [OnBack () ](#onback)
    -   [OnNext () ](#onnext)
    -   [OnCancel () ](#oncancel)
-   [其他方法和屬性](#other-methods-and-properties)
    -   [方法](#methods)
    -   [屬性](#properties)
-   [相關主題](#related-topics)

## <a name="implementing-navigation-script-functions"></a>執行導覽腳本函數

每個 HTML 頁面中的伺服器端腳本都會透過 **OnBack**、 **OnNext** 和 **OnCancel** 的函式來回應導覽按鈕。 這些函式必須可透過用戶端上的 **IHTMLDocument：： get \_ 腳本** 存取，而且不會使用任何參數。

### <a name="onback"></a>OnBack () 

-   當使用者按一下嚮導中的 [ **返回** ] 時回應。
-   如果目前的伺服器端頁面是第一個伺服器端頁面，請呼叫 **FinalBack** 來指示用戶端流覽至先前的用戶端頁面。
-   如果目前的伺服器端頁面不是第一個伺服器端頁面，請流覽至先前的伺服器端頁面。
-   每個頁面都必須執行此函數。 任何無法這麼做的頁面都會被視為無效，而且會顯示錯誤頁面。

### <a name="onnext"></a>OnNext () 

-   當使用者按一下嚮導中的 **[下一步** ] 時回應。
-   如果目前的伺服器端頁面是最後一個伺服器端頁面，請呼叫 **FinalNext** 來指示用戶端流覽至下一個用戶端頁面，或完成 wizard。
-   如果目前的伺服器端頁面不是最後一個伺服器端頁面，請流覽至下一個伺服器端頁面。

### <a name="oncancel"></a>OnCancel () 

-   當使用者按一下嚮導中的 [ **取消** ] 時回應。
-   您應設計 UI，讓使用者可以隨時取消。
-   一旦處理 **OnCancel** 函式中的任何處理，用戶端就會關閉嚮導。

## <a name="other-methods-and-properties"></a>其他方法和屬性

用戶端執行的函式是透過 **windows** 進行存取，就像是屬性一樣。 可用的服務如下所示：

### <a name="methods"></a>方法

-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a>屬性

-   [**標題**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**屬性**](/windows/desktop/shell/iwebwizardhost-property)

下列程式碼範例會顯示簡單的 wizard 頁面的伺服器端程式碼，其可執行 web 服務的錯誤頁面。


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[用戶端設計](pubwiz-client.md)
</dt> <dt>

[註冊服務](pubwiz-reg.md)
</dt> </dl>

 

 
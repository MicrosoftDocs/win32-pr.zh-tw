---
title: Client-Side 設計
description: 伺服器端 HTML 頁面中的腳本會與裝載的線上列印順序 Wizard 用戶端進行通訊。 這項通訊是透過 window 所存取的方法和屬性來完成。
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- 發佈嚮導，用戶端設計
- '[外部]、[發行] 嚮導'
- 發佈嚮導，window. 外部
- 發佈嚮導，設計考慮
- 發佈嚮導，線上列印訂購嚮導
- 線上列印順序 Wizard、用戶端設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933215"
---
# <a name="client-side-design"></a>Client-Side 設計

伺服器端 HTML 頁面中的腳本會與裝載的線上列印順序 Wizard 用戶端進行通訊。 這項通訊是透過 **window** 所存取的方法和屬性來完成。

本檔涵蓋下列主題。

-   [方法和屬性](#methods-and-properties)
-   [設計考量](#design-considerations)
-   [相關主題](#related-topics)

## <a name="methods-and-properties"></a>方法和屬性

您可以透過 **window. external** 物件取得下列方法和屬性。

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**取消**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**SetHeaderText**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**標題**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**屬性**](/windows/desktop/shell/iwebwizardhost-property)

伺服器端頁面的腳本會呼叫這些方法，在發行程式期間通知用戶端事件。 讓我們看看 [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) 的範例。 當 wizard 顯示第一個伺服器端的 HTML 網頁時，它會在所裝載的 HTML 網頁前面和之後，事先瞭解 wizard 頁面的控制碼。 在我們的範例中，在第一個 HTML 頁面上的使用者，按一下 [上一 **步** ] 按鈕。 Wizard 將此事件的通知傳送至伺服器。 收到此訊息時，伺服器端腳本會參考此事件的 **OnBack** 處理常式，因為這是第一個 HTML 網頁，所以會呼叫 **FinalBack** 方法。 這會讓嚮導先流覽至所顯示的 wizard 頁面，然後再輸入伺服器端 UI。

如需這些方法和屬性的完整討論，請參閱 [**WebWizardHost**](/windows/desktop/shell/webwizardhost) 和 [**NewWDEvents**](/windows/desktop/shell/newwdevents) 物件的檔。

## <a name="design-considerations"></a>設計考量

HTML 組成每個伺服器端頁面，在 [wizard] 窗格中會正常顯示。 設計這些頁面時，請記住，無法調整嚮導視窗的大小。 因此，頁面應該會經過建立和調整大小，如此一來，就可以避免捲軸捲軸，讓使用者透過 wizard 進行順暢的流覽。

每個 HTML 網頁也都必須提供 **OnBack**、 **OnNext** 和 **OnCancel** 事件的處理常式。 **OnNext** 處理常式也會處理 **完成** 事件。 未執行 **OnBack** 函式的頁面會被視為無效，而且會導致顯示錯誤頁面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[伺服器端設計](pubwiz-server.md)
</dt> </dl>

 

 
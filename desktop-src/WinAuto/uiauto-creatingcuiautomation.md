---
title: 建立 CUIAutomation 物件
description: 本節說明如何藉由具現化可執行 IUIAutomation 的物件來開始撰寫 Microsoft 消費者介面自動化用戶端應用程式。
ms.assetid: 9b90da60-0204-48c1-bb16-ff4a843bac67
keywords:
- 用戶端，建立 CUIAutomation 物件
- 用戶端，CUIAutomation 物件
- 消費者介面自動化，CUIAutomation 物件
- 消費者介面自動化，建立 CUIAutomation 物件
- 建立 CUIAutomation 物件
- CUIAutomation 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8162dac5276bbb22d00413276482cca34334fda5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933297"
---
# <a name="creating-the-cuiautomation-object"></a>建立 CUIAutomation 物件

本節說明如何藉由具現化可執行 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)的物件來開始撰寫 Microsoft 消費者介面自動化用戶端應用程式。

本主題包含下列各節。

-   [CUIAutomation 物件](#the-cuiautomation-object)
-   [建立物件](#creating-the-object)
-   [相關主題](#related-topics)

## <a name="the-cuiautomation-object"></a>CUIAutomation 物件

使用消費者介面自動化的第一個步驟是建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 類別的物件。 此物件會公開 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面，也就是用戶端應用程式使用的所有其他物件和介面的閘道。 此外， **IUIAutomation** 可用於下列工作：

-   訂閱事件。
-   建立條件。 條件是用來縮小消費者介面自動化元素搜尋範圍的物件。
-   從桌面 (根項目) ，或從螢幕座標或視窗控點，直接取得消費者介面自動化專案。
-   建立可用於導覽消費者介面自動化專案階層的樹狀瀏覽目錄者物件。
-   轉換資料類型。

## <a name="creating-the-object"></a>建立物件

若要開始在您的應用程式中使用消費者介面自動化，請執行下列步驟：

-   在您的專案標頭中包含 UIAutomation。 UIAutomation 會帶入定義 API 的其他標頭。
-   宣告 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)的指標。
-    (COM) 初始化元件物件模型。
-   建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85)) 的實例，並在您的指標中取出 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) 介面。

下列範例函數會初始化 COM，然後建立 [**CUIAutomation**](/previous-versions/windows/desktop/legacy/ff384838(v=vs.85))物件，並在 *ppAutomation* 指標中抓取 [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)介面。


```C++
#include <uiautomation.h>

// CoInitialize must be called before calling this function, and the  
// caller must release the returned pointer when finished with it.
// 
HRESULT InitializeUIAutomation(IUIAutomation **ppAutomation)
{
    return CoCreateInstance(CLSID_CUIAutomation, NULL,
        CLSCTX_INPROC_SERVER, IID_IUIAutomation, 
        reinterpret_cast<void**>(ppAutomation));
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[UI 自動化事件概觀](uiauto-eventsoverview.md)
</dt> <dt>

[取得 UI 自動化項目](uiauto-obtainingelements.md)
</dt> </dl>

 

 
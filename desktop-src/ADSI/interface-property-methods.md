---
title: 介面屬性方法
description: 許多 ADSI 介面都是設計來支援自動化，因此也是雙重介面，因為它們支援透過 IUnknown 和 IDispatch 介面的用戶端存取。
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- 介面屬性方法
- 說明 ADSI ADSI、參考、屬性方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fa872ea1711b23d850fe7063364712bba19d28d3e1157a81f5289f247944db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017085"
---
# <a name="interface-property-methods"></a>介面屬性方法

許多 ADSI 介面都是設計來支援自動化，因此也是雙重介面，因為它們支援透過 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 和 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面的用戶端存取。 非自動化用戶端（例如以 C/c + + 撰寫的用戶端）會使用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法直接解析方法調用，並直接呼叫方法。 Automation 用戶端（也稱為名稱系結用戶端，例如以 Visual Basic 撰寫的用戶端，或 Visual Basic 腳本撰寫)  (版）必須使用分派 [**介面**](/previous-versions/windows/desktop/automat/dispinterface)方法來間接解析方法調用。

支援 Automation 的 ADSI 介面會定義屬性方法，以抓取和修改執行介面之物件的屬性。 屬性方法的名稱會 \_  \_ 在適當的屬性名稱前面加上 get 和 put，例如， **get \_ User** 和 **put \_ Name**。

每 **個 \_ get** 方法都採用單一參數作為輸出。 這個參數是屬性資料類型之變數的方法配置位址。 傳回時，這個變數會假設所要求屬性的目前值。 當不再需要屬性時，呼叫端必須釋放變數的配置記憶體。

每 **個 \_ put** 方法都採用單一參數作為對應屬性之資料類型的輸入。 參數會保存新的屬性值。

下列程式碼範例顯示內容方法的調用，這些方法會遵循一般程式來呼叫物件的成員函式。


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



下列程式碼範例示範如何在 automation 用戶端中叫用屬性方法，這種方法可能稍有不同。 例如，Visual Basic 會使用點標記法。


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



所有參數和傳回類型都必須屬於 VARIANT 資料類型所定義的參數和傳回型別。 雙重介面上的所有方法都會傳回 HRESULT 值，以表示成功或失敗。

如需有關在 ADSI 物件上取得和設定屬性的詳細資訊，請參閱 [屬性](property-cache-interfaces.md)快取。

 

 
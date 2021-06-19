---
description: 在建立自訂 DirectShow 篩選的篩選屬性頁時，實作為屬性頁。
ms.assetid: ed71f26b-0812-4be8-96a4-b9f5dde45540
title: 步驟 4： 建立屬性頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32cd9eacc98af5f273897a3837390ab5cc75f7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406851"
---
# <a name="step-4-create-the-property-page"></a>步驟 4： 建立屬性頁

此時，篩選器會支援屬性頁面所需的所有專案。 下一步是執行屬性頁本身。 首先從 **CBasePropertyPage** 衍生新的類別。 下列範例會顯示部分宣告，包括稍後將在範例中使用的一些私用成員變數：


```C++
class CGrayProp : public CBasePropertyPage
{
private:
    ISaturation *m_pGray;    // Pointer to the filter's custom interface.
    long        m_lVal       // Store the old value, so we can revert.
    long        m_lNewVal;   // New value.
public:
    /* ... */
};
```



接下來，在資源編輯器中建立對話方塊資源，以及對話方塊標題的字串資源。 字串會出現在屬性頁的索引標籤中。 這兩個資源識別碼是 **CBasePropertyPage** 函式的引數：


```C++
CGrayProp::CGrayProp(IUnknown *pUnk) : 
  CBasePropertyPage(NAME("GrayProp"), pUnk, IDD_PROPPAGE, IDS_PROPPAGE_TITLE),
  m_pGray(0)
{ }
```



下圖顯示 [範例] 屬性頁的對話方塊資源。

![屬性頁對話方塊](images/proppage.png)

現在您已準備好執行屬性頁。 以下是 **CBasePropertyPage** 中要覆寫的方法：

-   當用戶端建立屬性頁時，會呼叫 **OnConnect** 。 它會將 **IUnknown** 指標設定為篩選器。
-   建立對話方塊時，會呼叫 **OnActivate** 。
-   當對話方塊收到視窗訊息時，就會呼叫 **OnReceiveMessage** 。
-   當使用者按一下 [**確定]** **或 [** 套用] 按鈕來認可屬性變更時，就會呼叫 **OnApplyChanges** 。
-   當使用者關閉屬性工作表時，就會呼叫 **OnDisconnect** 。

本教學課程的其餘部分將說明這些方法。

下一 [步：步驟5。將指標儲存至篩選準則](step-5--store-a-pointer-to-the-filter.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立篩選屬性頁](creating-a-filter-property-page.md)
</dt> </dl>

 

 




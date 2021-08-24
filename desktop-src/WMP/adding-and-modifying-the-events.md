---
title: 新增和修改事件
description: 新增和修改事件
ms.assetid: 342b0592-67b7-4c13-bee8-48ac322d3d27
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 464d20b600a5535e3cf2c02be01fa19c10a590e143c7a96375580719b70c274c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865338"
---
# <a name="adding-and-modifying-the-events"></a>新增和修改事件

您必須提供 \_ 當使用者變更屬性頁編輯方塊中的文字時，所發生的 EN 變更事件的事件處理常式。 這些事件處理常式具有只在 [屬性頁] **對話方塊中啟用** [套用] 的簡單執行。

## <a name="modifying-the-scale-factor-event-handler"></a>修改縮放因數事件處理常式

您必須變更外掛程式嚮導為縮放比例編輯方塊提供的現有事件處理常式名稱。 您應該在三個位置中，將名稱從 OnChangeScale 變更為 OnChangeDelay：

1.  在 EchoPropPage 中，變更 message map 宏區段中的名稱。 以下列程式碼取代將縮放比例變更事件對應至 OnChangeScale 方法的程式程式碼：
    ```C++
    COMMAND_HANDLER(IDC_DELAYTIME, EN_CHANGE, OnChangeDelay)
    
    ```

    

2.  在 EchoPropPage 中，變更原型為 OnChangeScale 函式之程式程式碼中的名稱：
    ```C++
    LRESULT (OnChangeDelay)(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled);
    
    ```

    

3.  在 EchoPropPage .cpp 中，變更函式標頭中的名稱：
    ```C++
    LRESULT CEchoPropPage::OnChangeDelay(WORD wNotifyCode, WORD wID, HWND hWndCtl, BOOL& bHandled)
    
    ```

    

## <a name="adding-the-wet-mix-event-handler"></a>新增潮濕混合事件處理常式

您可以輕鬆地加入 \_ 附加至 IDC \_ WETMIX 編輯方塊控制項之 EN 變更事件的事件處理常式。 從對話方塊資源編輯器：

1.  以滑鼠右鍵按一下 IDC \_ WETMIX 編輯方塊，然後選擇 [ **事件**]。 [新增 Windows 訊息和事件處理常式] 對話方塊隨即出現。
2.  在 [ **要處理的類別或物件** ] 方塊中，按一下 [IDC WETMIX] 編輯方塊資源的名稱 \_ 。
3.  在 [**新的 Windows 訊息/事件**] 方塊中，按一下 [EN \_ 變更] 以選取它。
4.  按一下 [ **加入處理常式**]。 [加入成員函數] 對話方塊隨即出現。
5.  在 [ **成員** 函式名稱] 方塊中，輸入名稱 OnChangeWetmix。
6.  按一下 **[確定** ] 以關閉 [加入成員函式] 對話方塊。
7.  按一下 **[確定** ] 返回對話方塊資源編輯器。

Visual C++ 會自動將訊息對應和事件處理常式函式的程式碼加入至 EchoPropPage .h。 它所插入的程式碼會提供 TODO 批註，您可以在其中新增函式標頭中的實作為。 這與 Windows Media Player 外掛程式 Wizard 範例程式碼所使用的樣式稍有不同，但卻是可接受的。

您是否想要在標頭檔中撰寫您的執行，或將其移至 EchoPropPage。 .cpp 由您決定。 無論是哪一種情況，執行都只需要一行額外的程式碼，即可在 [屬性頁] 對話方塊 **中啟用 [** 套用]。 將這行程式碼插入函式傳回的行之前：


```C++
SetDirty(TRUE);  // Enable Apply.

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 





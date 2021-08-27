---
title: 'TVN_ASYNCDRAW (Commctrl 的通知碼) '
description: 當圖示或重迭的繪圖失敗時，由樹狀檢視控制項傳送到其父系。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4d929977e1a14a5ada96232fa054c2689d27f1eaa026b64c974d51f5a2c38c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060098"
---
# <a name="tvn_asyncdraw-notification-code"></a>IZDEBSKI \_ ASYNCDRAW 通知碼

當圖示或重迭的繪圖失敗時，由樹狀檢視控制項傳送到其父系。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVASYNCDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw)結構的指標。 **NMTVASYNCDRAW** 結構包含繪製失敗的原因。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

樹狀檢視控制項必須有 [**tv \_ EX \_ DRAWIMAGEASYNC**](tree-view-control-window-extended-styles.md) 延伸樣式。 請注意，這相當於清單視圖的 LVN \_ ASYNCDRAWN 旗標及其對應的樣式。

此控制項不會以非同步方式繪製。 在樹狀結構中，如果影像無法使用，則會在樹狀檢視控制項不同步將影像解壓縮的內容中使用非同步。  (比方說，如果樹狀檢視控制項使用的是稀疏影像清單，則可能無法使用影像，因為影像可能會被卸載。 ) 相反地，當影像無法使用時，控制項會以 NMTVASYNCDRAW 結構傳送父代 IZDEBSKI ASYNCDRAW 通知，以同步方式要求父項要採取的動作 \_ 。 [](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) 此結構的 **hr** 成員描述控制項繪製失敗的原因。 電子暫止的 **hr** 結果 \_ 表示映射不會出現在所有 (映射需要解壓縮) 。 Success 表示影像存在，但不是必要的影像品質。

父系會設定結構的 **dwRetFlags** 成員，以通知控制項如何繼續。 例如，父代可能會傳回 **iRetImageIndex** 成員中的另一個影像，以便繪製控制項。 在此情況下，父代會將 **dwRetFlags** 成員設定為 ADRF \_ DRAWIMAGE。 如果控制項找不到傳回的影像，但控制項可能會傳送另一個 IZDEBSKI \_ ASYNCDRAW 通知。

如果映射無法使用，則非同步概念是允許父系在背景進行解壓縮，讓解壓縮不會封鎖 UI 執行緒，也就是控制項所在的執行緒。 父系可能會將 ADRF \_ DRAWNOTHING 傳回給控制項，然後啟動背景執行緒以將圖示解壓縮。 一旦解壓縮之後，父系可能會在 treeview 控制項中使用宏 [**treeview \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)來設定圖示。 這會導致樹狀檢視使專案失效，最後使用影像清單中已解壓縮的影像重新繪製它。

下列程式碼範例（可作為較大程式的一部分）會顯示父代如何在控制項中處理此通知中的兩個可能傳回碼，以及決定控制項應採取的動作。 未顯示設定 **dwRetFlags** 。


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






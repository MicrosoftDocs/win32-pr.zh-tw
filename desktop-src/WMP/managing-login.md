---
title: 管理登入
description: 管理登入
ms.assetid: 5cafcd3a-e819-4524-b7a9-580ff36fc4f8
keywords:
- Windows Media Player 線上商店、管理登入
- 線上商店、管理登入
- 輸入1個線上商店，管理登入
- Windows Media Player 線上商店，登入
- 線上商店，登入
- 輸入1個線上商店，登入
- Windows Media Player 線上商店、標準登入程式
- 線上商店、標準登入流程
- 輸入1個線上商店、標準登入流程
- Windows Media Player 線上商店、登出進程
- 線上商店、登出進程
- 輸入1個線上商店、登出進程
- 標準登入進程
- 登出進程
- 登入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 698385f2d5a618899bd4fe440db5a552859c7647ceb2ae11e02b773c96479d52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135171"
---
# <a name="managing-login"></a>管理登入

Windows Media Player 支援各種不同的方法，讓使用者登入類型1線上商店。 播放程式會提供標準的登入對話方塊，但線上商店可以提供作為標準對話方塊替代方案的網頁。

使用者可以藉由與 Windows Media Player 使用者介面互動，或與線上商店所提供的探索頁面互動，來起始登入嘗試。 如果使用者透過與探索頁面互動來起始登入嘗試，[探索] 頁面上的腳本會呼叫 [attemptLogin](external-attemptlogin.md) 方法。

使用者的登入狀態是由線上商店所維護。 當使用者的登入狀態變更，或登入嘗試失敗時，線上商店的外掛程式會藉由呼叫 [IWMPContentPartnerCallback：： Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)、在 *類型* 參數中傳遞 wmpcnLoginStateChange，來通知 Windows Media Player。 播放程式會藉由引發 [OnLoginChange](external-onloginchange-event.md) 事件，將通知傳遞至探索頁面。

對 **OnLoginChange** 的呼叫不一定表示使用者的登入狀態已變更;這可能表示嘗試登入失敗。 若要判斷使用者的登入狀態， **OnLoginChange** 事件處理常式可以檢查 [userLoggedIn](external-userloggedin.md) 屬性。

下列各節說明標準登入程式、替代的登入程式，以及登出進程。

## <a name="standard-log-in"></a>標準登入

標準登入套裝程式含下列步驟：

1.  使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登入嘗試。
2.  Windows Media Player 會顯示一個對話方塊，提示使用者輸入使用者名稱和密碼。
3.  當使用者按一下對話方塊中的 [登 **入**] 按鈕時，Windows Media Player 會呼叫 [IWMPContentPartner：： Login](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)（由線上商店的外掛程式所執行）。
4.  外掛程式會與線上存放區通訊，且成功或無法登入使用者。
5.  如果登入嘗試成功，則外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT TRUE。 如果登入嘗試失敗，外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並在 *pCoNtext* 參數的 **ulVal** 成員中傳遞32位值。 然後，播放程式會將該32位值傳遞給 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) ，以取得可處理失敗之網頁的 URL。

## <a name="alternative-login"></a>替代登入

如果 \_ \_ 已在線上商店外掛程式的 [**功能**] 登錄專案中設定訂用帳戶上限 ALTLOGIN 旗標，Windows Media Player 不會使用 [標準登入] 對話方塊。 相反地，Windows Media Player 會呼叫 **IWMPContentPartner：： GetItemInfo** 來取得執行登入程式之網頁的 URL。 如需 **功能** 登錄專案的詳細資訊，請參閱 [類型1線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-1-online-store.md)。

播放程式會呼叫 **GetItemInfo** 兩次：一次傳遞 g \_ szItemInfo \_ ALTLoginURL 以抓取登入網頁的 URL，以及通過 g \_ szItemInfo \_ ALTLoginCaption 來取得裝載網頁之視窗的標題。 當 **GetItemInfo** 傳回登入網頁的 url 時，可以將下列參數字串附加至 URL，以指定登入視窗的大小：

?DlgX =*width*&DlgY =*height*

在參數字串中， *寬度* 和 *高度* 是視窗的寬度和高度（以圖元為單位）。 例如， **GetItemInfo** 可能會傳回下列字串，以指定要在寬度為800圖元且高度為400圖元的視窗中顯示 AltLogin.htm


```C++
https://proseware.com/AltLogin.htm?DlgX=800&DlgY=400
```



替代的登入套裝程式含下列步驟：

1.  使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登入嘗試。
2.  Windows Media Player 會開啟一個強制回應視窗，以顯示線上商店所提供的登入網頁。
3.  網頁會與線上商店通訊，且成功或無法登入使用者。
4.  如果登入嘗試成功，網頁會呼叫 [sendMessage](external-sendmessage.md)來通知線上商店的外掛程式，這會導致呼叫 [IWMPContentPartner：： sendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)。 線上商店的外掛程式會檢查傳遞給 **IWMPContentPartner：： SendMessage** 的參數，以判斷登入嘗試成功。 這些參數不會由 Windows Media Player 來解讀。它們只有線上商店才有意義。 外掛程式會呼叫 **IWMPContentPartnerCallback：： Notify**，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT TRUE。 如果登入失敗，線上商店必須決定如何協助使用者。 其中一個可能的原因是在裝載替代登入網頁的強制回應視窗中顯示新網頁。

## <a name="log-out"></a>登出

登出進程包含下列步驟。

1.  使用者藉由與 Windows Media Player 使用者介面互動或與探索頁面互動，來起始登出嘗試。
2.  Windows Media Player 會呼叫[IWMPContentPartner：：登出](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)，這是由線上商店的外掛程式所執行。
3.  外掛程式會與線上商店通訊，而且會成功或無法登出使用者。
4.  如果登入嘗試成功，外掛程式會藉由呼叫 **IWMPContentPartnerCallback：： Notify** 來通知 Windows Media Player，並 \_ 在 *pCoNtext* 參數的 **boolVal** 成員中傳遞 VARIANT FALSE。

嘗試登入或登出成功時，線上商店的外掛程式會呼叫 **IWMPContentPartnerCallback：： Notify**，在 *類型* 參數中傳遞 wmpcnLoginStateChange。 外掛程式會使用 *pCoNtext* 參數來指定使用者目前的登入狀態。 如果外掛程式將 *pCoNtext* -> **boolVal** 設定為 VARIANT \_ TRUE，就會將使用者登入。 如果外掛程式將 *pCoNtext* -> **boolVal** 設定為 VARIANT \_ FALSE，則會將使用者登出。請注意， *pCoNtext* 不會指出嘗試成功或失敗;相反地，它會指出使用者目前的登入狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**AttemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**OnLoginChange 事件**](external-onloginchange-event.md)
</dt> <dt>

[**UserLoggedIn**](external-userloggedin.md)
</dt> <dt>

[**IWMPContentPartner：： Login**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[**IWMPContentPartner：：登出**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-logout)
</dt> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 





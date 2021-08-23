---
title: 類型1線上商店的外部物件
description: 類型1線上商店的外部物件
ms.assetid: 5c42e1a9-c5c6-4725-8528-de2839d84e77
keywords:
- Windows Media Player 線上商店、外部物件
- 線上商店、外部物件
- 輸入1個線上商店、外部物件
- 外部物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7d95d2ca332b88edea73da2238374aeffc52e520d7bc0346eab9f4eb7a05f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648998"
---
# <a name="external-object-for-type-1-online-stores"></a>類型1線上商店的外部物件

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**外部** 物件提供由線上商店（裝載于 Windows Media Player）所提供之網頁的功能。

**外部** 物件會公開類型1線上商店的下列屬性。



| 屬性                                                                                  | 描述                                                                                                                              |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [accountType](external-accounttype.md)                                                   | 抓取目前使用者的帳戶類型。                                                                                          |
| [appColorButtonHighlight](external-appcolorbuttonhighlight.md)                           | 抓取 Windows Media Player 使用者介面目前的按鈕反白顯示色彩。                                                |
| [appColorButtonHoverFace](external-appcolorbuttonhoverface.md)                           | 抓取 Windows Media Player 使用者介面目前的按鈕停留色彩。                                                    |
| [appColorButtonShadow](external-appcolorbuttonshadow.md)                                 | 抓取 Windows Media Player 使用者介面目前的按鈕陰影色彩。                                                   |
| [appColorDark](external-appcolordark.md)                                                 | 抓取 Windows Media Player 使用者介面目前的深色陰影色彩。                                                      |
| [appColorLight](external-appcolorlight.md)                                               | 抓取 Windows Media Player 使用者介面目前的淺色陰影色彩。                                                     |
| [appColorMedium](external-appcolormedium.md)                                             | 抓取 Windows Media Player 使用者介面目前的中陰影色彩。                                                    |
| [basketTitle](external-baskettitle.md)                                                   | 在 [清單] 窗格中抓取按鈕的標題 (也稱為 Windows Media Player 中的購物籃) 。                                     |
| [filter](external-filter.md)                                                             | 抓取 Windows Media Player 目前正在使用的搜尋篩選器。                                                                    |
| [ignoreIEHistory](external-ignoreiehistory.md)                                           | 指定 Windows Media Player 是否應忽略 Internet Explorer 歷程記錄。                                                          |
| [libraryLocationID](external-librarylocationid.md)                                       | 抓取目前顯示在播放程式視圖中的特定媒體專案識別碼。                                      |
| [libraryLocationType](external-librarylocationtype.md)                                   | 抓取連結[庫位置常數](library-location-constants.md)，指出 Windows Media Player 中目前視圖的型別。 |
| [pluginRunning](external-pluginrunning.md)                                               | 抓取值，指出線上商店的外掛程式是否正在執行。                                                          |
| [selectedItemID](external-selecteditemid.md)                                             | 抓取 Windows Media Player 中目前選取之媒體專案的識別碼。                                           |
| [selectedItemType](external-selecteditemtype.md)                                         | 抓取 Windows Media Player 中目前選取之媒體專案的類型。                                                 |
| [任務](external-task.md)                                                                 | 抓取目前工作窗格的名稱。                                                                                             |
| [templateBeingDisplayedInLocalLibrary](external-templatebeingdisplayedinlocallibrary.md) | 指出目前的 [探索] 頁面所表示的摘要是否會顯示在 [本機程式庫] 樹狀檢視控制項中。          |
| [userLoggedIn](external-userloggedin.md)                                                 | 抓取值，指出使用者是否已登入線上商店。                                                          |
| [version](external-version.md)                                                           | 抓取 Windows Media Player 的目前版本。                                                                                   |
| [viewParameters](external-viewparameters.md)                                             | 在 Windows Media Player 中，抓取與目前視圖相關聯的參數。                                                           |



 

**外部** 物件會公開類型1線上商店的下列方法。



| 方法                                                            | 描述                                                                                                                  |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [addToBasket](external-addtobasket.md)                           | 在 [清單] 窗格中新增媒體專案 (也稱為 [購物籃]) Windows Media Player。                                          |
| [attemptLogin](external-attemptlogin.md)                         | 顯示對話方塊，讓使用者可以嘗試登入線上商店。                                                 |
| [authenticate](external-authenticate.md)                         | 起始驗證使用者的嘗試。                                                                               |
| [buy](external-buy.md)                                           | 開始購買一組媒體專案。                                                                              |
| [cancelNavigate](external-cancelnavigate.md)                     | 通知 Windows Media Player 它不應該顯示新的 [探索] 頁面，即使播放程式中的視圖已經變更也一樣。 |
| [changeView](external-changeview.md)                             | 變更 Windows Media Player 中的視圖。                                                                                    |
| [changeViewOnlineList](external-changeviewonlinelist.md)         | 在 Windows Media Player 中變更視圖，以顯示線上商店動態產生的清單。                        |
| [download](external-download.md)                                 | 起始一組媒體專案的下載。                                                                              |
| [玩](external-play.md)                                         | 指示 Windows Media Player 播放一組媒體專案。                                                                 |
| [saveCurrentViewToLibrary](external-savecurrentviewtolibrary.md) | 從目前視圖中的媒體專案建立播放清單，並將播放清單儲存至本機文件庫。                     |
| [sendMessage](external-sendmessage.md)                           | 將訊息傳送至線上商店的外掛程式。                                                                               |
| [showPopup](external-showpopup.md)                               | 指示 Windows Media Player 顯示彈出網頁;也就是在另一個視窗中出現的網頁。            |



 

**外部** 物件會公開類型1線上商店的下列事件。



| 事件                                                                         | 描述                                                                             |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [OnChangeViewError](external-onchangeviewerror-event.md)                     | 當 **ChangeView** 方法的呼叫導致錯誤時發生。           |
| [OnChangeViewOnlineListError](external-onchangeviewonlinelisterror-event.md) | 當 **ChangeViewOnlineList** 方法的呼叫導致錯誤時發生。 |
| [OnColorChange](external-oncolorchange-event.md)                             | 當 Windows Media Player 使用者介面的色彩變更時發生。               |
| [OnLoginChange](external-onloginchange-event.md)                             | 當使用者的登入狀態變更或登入嘗試失敗時發生。        |
| [OnSendMessageComplete](external-onsendmessagecomplete-event.md)             | 當線上商店已完成訊息的處理時發生。                         |
| [OnViewChange](external-onviewchange-event.md)                               | 當 Windows Media Player 中的 view 變更時發生。                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型 1 線上商店的參考**](reference-for-type-1-online-stores.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





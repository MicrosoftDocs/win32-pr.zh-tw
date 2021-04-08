---
title: Windows Media Player 線上商店
description: Windows Media Player 線上商店
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Windows Media Player 線上商店，關於
- 線上商店，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103681551"
---
# <a name="windows-media-player-online-stores"></a>Windows Media Player 線上商店

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

Windows Media Player 提供的功能可讓數位媒體內容提供者將其服務與 Windows Media Player 整合。 播放程式與線上數位媒體存放區之間的整合，可為使用者提供更好的全方位體驗，包括尋找內容、下載及管理檔案、播放內容，以及將內容複寫到 Cd 或裝置的能力。

## <a name="contacting-microsoft"></a>聯絡 Microsoft

如果您想要將線上數位媒體存放區與 Windows Media Player 整合，但尚未與 Microsoft 聯繫，您可以透過傳送電子郵件給 Windows Media Player Services 虛擬小組來開始進行。 小組的電子郵件地址為 mpsvctm@microsoft.com 。

## <a name="for-more-information"></a>詳細資訊

如需使用各種 Windows Media Sdk 來建立提供授權數位媒體內容的服務的技術指引，請前往 [Microsoft Windows Media 開發人員中心](https://msdn.microsoft.com/windowsmedia/default.aspx) ，並搜尋「建立 Windows Media Player 10 訂閱線上商店」。

## <a name="online-stores-in-windows-media-player-9-series"></a>Windows Media Player 9 系列的線上商店

Windows Media Player 9 系列引進了線上商店的概念。 在 Windows Media Player 9 系列中，線上商店提供者可以將其服務整合到 Windows Media Player 的 **Premium services** 功能中。

## <a name="online-stores-in-windows-media-player-10"></a>Windows Media Player 10 的線上商店

在 Windows Media Player 10 中，premium 服務已重新命名為線上商店，並新增了下列新功能：

-   Windows Media Player 最多可提供三個工作窗格供線上商店使用。
-   當使用者在播放程式的使用者介面中選擇時，若要查看有關數位媒體內容的詳細資訊，請 Windows Media Player 線上商店上的電話，以提供資訊。
-   當使用者在播放程式的使用者介面中選擇購買媒體專案時，請在線上商店上 Windows Media Player 呼叫來處理購買。
-   線上商店可以提供外掛程式，Windows Media Player 呼叫以取得數位版權管理的協助，以及背景處理的時間。
-   線上商店可以與 Windows Media Player 安裝程式整合。

## <a name="online-stores-in-windows-media-player-11"></a>Windows Media Player 11 的線上商店

Windows Media Player 11 引進了一種新類型的線上音樂商店，更深層整合至玩家的使用者介面。 在 Windows Media Player 11 中，我們新增了下列新功能，以支援這種新類型的線上商店。

-   Windows Media Player 下載線上商店的媒體目錄，讓使用者可以快速流覽線上商店的內容。
-   Windows Media Player 會在 library 樹狀檢視控制項中顯示線上商店的音樂內容。
-   當使用者在播放程式的使用者介面中流覽時，播放程式會在線上商店上呼叫，以提供可增強使用者體驗的網頁。
-   線上商店提供的外掛程式，可處理 Windows Media Player 與線上商店之間通訊的所有層面。 例如，外掛程式會處理登入、授權更新、目錄升級、內容下載以及購買內容。
-   Windows Media Player 可提供線上商店提供的播放程式與網頁之間的增強通訊，並裝載于播放程式中。

## <a name="types-of-online-stores"></a>線上商店的類型

有兩種類型的線上商店：類型1和類型2。

Type 1 store 提供最先進的 Windows Media Player 整合層級。 它提供可下載的音樂類別目錄，並已緊密整合到玩家的使用者介面中。 Windows Media Player 11 和更新版本支援類型1存放區。

Type 2 store （Windows Media Player 9 系列和更新版本支援）有兩個子類別：商務商店和音樂商店。

商務存放區提供最多三個服務工作窗格來顯示商店的網頁，以提供最基本的體驗。

音樂存放區可為使用者提供比商務商店更整合的體驗。 在 [音樂] 存放區中，使用者可以在 [存放) 區] 提供的網頁以外的 Windows Media Player (中，按一下按鈕和連結，以執行像是購買 CD 或 DVD、取得特定媒體專案的詳細資訊，或顯示資訊中心視圖窗格等動作。 在每個案例中，Windows Media Player 會呼叫目前的音樂存放區來處理這些要求。

> [!Note]  
> 有些檔將商務商店稱為「基本商務服務」，並將音樂商店稱為「整合式音樂服務」。

 

下表顯示不同類型的線上商店可用的功能。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>功能</th>
<th>類型2商務商店</th>
<th>類型2音樂存放區</th>
<th>類型1存放區</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>建立服務工作窗格
<blockquote>
[!Note]<br />
Windows Media Player 10 的服務工作窗格最多三個。 Windows Media Player 11 只有一個。
</blockquote>
<br/></td>
<td>是</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="even">
<td>變更按鈕色彩、工作列色彩和按鈕文字等屬性，以變更商店的外觀。</td>
<td>是</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="odd">
<td>將標誌影像新增至 Windows Media Player 線上商店功能表和工作列。</td>
<td>是</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="even">
<td>從 HTMLView 流覽至線上商店。</td>
<td>是</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="odd">
<td>處理 Windows Media Player 購買 CD 或 DVD 的要求。</td>
<td>否</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="even">
<td>處理 Windows Media Player 要求，以提供豐富的專輯資訊。</td>
<td>否</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="odd">
<td>提供資訊中心視圖網頁。</td>
<td>否</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="even">
<td>自訂 Windows Media Player 安裝程式以指定初始線上商店。</td>
<td>否</td>
<td>是</td>
<td>是</td>
</tr>
<tr class="odd">
<td>提供可實行 <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>的外掛程式。
<blockquote>
[!Note]<br />
在 Windows Media Player 10 和更新版本中，此外掛程式也可以執行 <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>。
</blockquote>
<br/></td>
<td>否</td>
<td>是</td>
<td>否</td>
</tr>
<tr class="even">
<td>提供 Windows Media Player 下載的音樂類別目錄</td>
<td>否</td>
<td>否</td>
<td>是</td>
</tr>
<tr class="odd">
<td>根據使用者在播放程式使用者介面中的導覽，提供自訂的網頁和內容功能表。</td>
<td>否</td>
<td>否</td>
<td>是</td>
</tr>
<tr class="even">
<td>提供可實行 <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>的外掛程式。</td>
<td>否</td>
<td>否</td>
<td>是</td>
</tr>
</tbody>
</table>



 

有關線上商店的其餘檔分成下列各節。



| 區段                                                                                                                              | 描述                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [線上商店歡迎套件](online-stores-welcome-kit.md)                                                                           | 包含有關如何將線上數位媒體存放區帶入 Windows Media Player 的資訊。             |
| [輸入1個線上商店](type-1-online-stores.md)                                                                                     | 包含類型1線上商店的 About、Guide 和 Reference 區段。                                             |
| [輸入2個線上商店](type-2-online-stores.md)                                                                                     | 包含類型2線上商店的 About、Guide 和 Reference 區段。                                             |
| [Type 1 和 Type 2 線上商店的一般資訊](information-common-to-type-1-and-type-2-online-stores.md)                   | 包含適用于 Type 1 和 Type 2 線上商店的資訊。                                          |
| [重新整理具有 PlaysForSure 標誌之商店的授權](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | 包含未與 Windows Media Player 整合之線上商店的相關資訊，可以更新授權。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Windows Media Player SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 






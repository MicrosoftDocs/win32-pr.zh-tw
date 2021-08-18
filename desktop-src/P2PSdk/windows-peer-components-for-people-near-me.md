---
description: Windows近端分享的對等元件
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: Windows近端分享的對等元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762ea58aa9738bfe01e23844dd146e4de8a6a5f76433ef969b60b30fb5886db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011496"
---
# <a name="windows-peer-components-for-people-near-me"></a>Windows近端分享的對等元件

在主要 Windows 對等網路可執行檔 (P2phost.exe) 中，[近端分享架構](people-near-me-architecture.md)會使用下列元件：

### <a name="people-near-me"></a>近端分享

近端分享 (PNM) 元件會針對支援 PNM 之電腦的使用者名稱，使用本機子網上的 Web 服務探索來起始探索。

### <a name="people-near-me-publisher"></a>近端分享 Publisher

近端分享 Publisher 元件會發佈已登入使用者的昵稱，以指出在本機子網上使用 PNM 的其他電腦可用性。 登入的使用者必須選擇在公告昵稱之前發佈其昵稱。 昵稱是使用 Web 服務探索在子網上發佈的。 此外，也可以發行物件和應用程式。 但是，使用者必須為「**近端分享**」或「**全部**」範圍指定物件和應用程式發行。

### <a name="people-near-me-enumerator"></a>近端分享列舉值

近端分享枚舉器元件會列舉本機子網上的使用者清單。 使用此清單，Web 服務探索會傳送多播查詢並接收回應。 取得昵稱清單之後，應用程式就可以使用此 API 來取得使用者所發佈的更多資料 (使用 [SChannel](windows-vista-components-for-people-near-me.md)) 加密，例如已註冊的應用程式清單，以及任何要發行的物件。

搜尋和列舉程式不會自動發生，而是必須由使用者或應用程式以登入 PNM 來明確起始。 搜尋結果是在相同子網上使用 PNM API 公告其昵稱的其他使用者的昵稱清單。

### <a name="publication-manager"></a>發行集管理員

發行集管理員元件負責將目前狀態、應用程式或物件更新發佈給訂閱或輪詢資料的連絡人或近端人員。

### <a name="peer-signaling"></a>對等信號

對等信號元件會處理對等互連與 exchange 資料之間的連接建立。 針對近端分享，當使用者或應用程式將單播查詢傳送至特定電腦以取得其公開金鑰、應用程式和物件時，就會使用對等信號。

### <a name="receive-invitation-handlerux"></a>接收邀請處理常式/UX

接收邀請處理常式/UX 元件接收來自其他人的傳入邀請，會提示使用者決定是否要啟動與邀請相關聯的應用程式，然後根據接受邀請的使用者來啟動應用程式。 邀請是來自其他人的訊息，可使用安裝在這兩個使用者電腦上的特定應用程式起始共同作業活動，並且由受邀的使用者進行公告。

### <a name="peer-security"></a>對等安全性

傳送狀態、應用程式和物件時，會使用 SSL 通道 ([Schannel](windows-vista-components-for-people-near-me.md)) 來加密資訊。 起始電腦使用受邀電腦的公開金鑰來協商秘密金鑰，該金鑰是用來加密在兩個對等之間傳送的後續資料。

 

 




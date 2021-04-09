---
description: 近端分享需求
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: 近端分享需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849306"
---
# <a name="people-near-me-requirements"></a>近端分享需求

為了讓 [近端分享](about-people-near-me.md) 為 Windows 對等網路應用程式提供順暢的連線能力和簡單的共同作業，請完成下列作業：

### <a name="people-discovery"></a>人們探索

人們探索可讓使用者探索和顯示位於本機子網上的一組對等。 本機子網上的任何電腦都必須通告登入對等的名稱。 探索查詢之後所列的對等，是一組執行 Windows Vista 的使用者，已設定為使用 [近端分享](about-people-near-me.md)將昵稱通告給其他使用者。 這項功能預設為停用，且必須由已登入的使用者啟用。

> [!Note]  
> 在「近端分享」探索程式期間探索到的遠端對等，不一定是與探索到之對等相關聯的預期使用者。

 

### <a name="extended-data-discovery"></a>擴充資料探索

擴充資料探索允許搜尋有特定興趣的使用者。 使用者也可以指定他們想要通告本身的其他資料。 例如，除了已登入之使用者的昵稱之外，資料也可以在產業會議上概述特定的專業興趣。

### <a name="application-discovery"></a>應用程式探索

近端分享啟用的臨機操作共同作業的確切本質是應用程式所特有。 例如，共同作業可能正在聊天或共用相片，而這兩者都需要特定的應用程式。 為了讓近端分享能夠啟用共同作業活動，一組適用于近端分享案例的應用程式也必須經過公告和探索。

### <a name="subscription"></a>訂用帳戶

使用訂用帳戶，應用程式可以訂閱以追蹤人員的存在性、應用程式和物件變更。

### <a name="invitation"></a>邀請

在探索到人員、興趣和應用程式之後，使用近端分享應用程式的對等共同作業，可以開始邀請和接受交換。 初始化對等會將邀請訊息傳送給另一個對等。 收到邀請的使用者可以接受或拒絕邀請。 接受邀請時，會啟動所要求活動的適當對等應用程式。

### <a name="add-as-a-contact"></a>新增為連絡人

如果使用者透過近端分享建立共同作業活動，並且想要維護一段時間的連絡人，他們可以將彼此新增為連絡人。 完成這項作業之後，他們就可以觀察使用者的目前狀態 (例如線上、離線或離開) ，並在網際網路上隨時邀請他們進入共同作業活動。 當人位於附近時，任何可能的活動也可以透過網際網路的連絡人進行。

### <a name="security"></a>安全性

若要保護對等共同作業活動中所交換的使用者和資料，使用者可以對所公告的內容進行配置控制。 使用者也必須接受邀請，才可開始對等共同作業。 共同作業活動會使用安全通訊端層 (SSL) 加密通道進行加密 (也稱為 Schannel) 。 SSL 是一種密碼編譯通訊協定，可保護以 TCP 為基礎的通訊。 如需詳細資訊，請參閱 [SChannel](windows-vista-components-for-people-near-me.md)。 在 Windows Vista 中， [Windows 對等網路](what-is-peer-networking-.md)架構中的一組新元件支援這些需求。

 

 




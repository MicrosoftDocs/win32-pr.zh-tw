---
description: 從 Windows XP，主控台支援主控台專案的分類。 註冊的專案會出現在一或多個類別中。 無法建立新的類別。
title: 指派主控台分類
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478484"
---
# <a name="assigning-control-panel-categories"></a>指派主控台分類

從 Windows XP，主控台支援主控台專案的分類。 註冊的專案會出現在一或多個類別中。 無法建立新的類別。

若要在一或多個類別中註冊主控台專案，請視需要在[註冊主控台專案](registering-control-panel-items.md)的[可執行檔主控台專案註冊](registering-control-panel-items.md)或[DLL 主控台專案註冊](registering-control-panel-items.md)區段中，加入值。




| 類別目錄識別碼 | 類別名稱 (Windows 7)  | Windows Vista) 的類別名稱 ( | Windows XP) 的類別名稱 ( | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | 「所有主控台專案」 | [其他選項]<blockquote>[!Note]<br />未指定類別目錄識別碼的任何主控台專案都會出現在此分類中。</blockquote><br /> | 「其他主控台選項」<blockquote>[!Note]<br />未指定類別目錄識別碼的任何主控台專案都會出現在此分類中。</blockquote><br /> | 
| 1 | 「外觀和個人化」 | 「外觀和個人化」 | 「外觀和主題」 | 
| 2 | 「硬體和音效」 | 「硬體和音效」 | 「印表機和其他硬體」 | 
| 3 | 「網路和網際網路」 | 「網路和網際網路」 | 「網路和網際網路連接」 | 
| 4 | 不再使用。 只要將本身新增至類別4的任何專案，就會出現在類別 2 (硬體和音效) 。 | 不再使用。 只要將本身新增至類別4的任何專案，就會出現在類別 2 (硬體和音效) 。 | 「聲音、語音和音訊裝置」 | 
| 5 | 「系統和安全性」 | 「系統和維護」 | 「效能和維護」 | 
| 6 | 「時鐘、語言和區域」 | 「時鐘、語言和區域」 | 「日期、時間、語言和地區選項」 | 
| 7 | "輕鬆存取" | "輕鬆存取" | [協助工具選項] | 
| 8 | 程式 | 程式 | [新增或移除程式] | 
| 9 | 「使用者帳戶」<blockquote>[!Note]<br />若未連線至網域，這稱為「使用者帳戶和家庭安全」。</blockquote><br /> | 「使用者帳戶」<blockquote>[!Note]<br />若未連線至網域，這稱為「使用者帳戶和家庭安全」。</blockquote><br /> | 「使用者帳戶」 | 
| 10 | 不再使用。 在此類別中註冊的專案會出現在 [類別 5 (系統和安全性) ] 中。 | "Security" | 「安全性中心」<blockquote>[!Note]<br />僅適用于 Windows XP Service Pack 2 (SP2) 或更新版本。</blockquote><br /> | 
| 11 | 不再使用。 在此類別中註冊的專案會顯示在類別 0 (所有主控台專案) 。 | "Mobile PC"<blockquote>[!Note]<br />此類別只會顯示在行動電腦上。</blockquote><br /> | 未使用。 | 




 

在 Windows XP 中，[**新增或移除程式**] 和 [**使用者帳戶**] 類別的運作方式與主控台中其他類別的運作方式稍有不同。 當一或多個專案新增至這兩個類別的其中一個時，主控台中的相關聯連結會開啟 [類別目錄] 頁面。 註冊的專案會出現在頁面的下半部的 [或挑選主控台圖示] 標題下方。 如果未針對其中一個類別註冊任何專案，主控台中的相關連結會直接叫用該類別的標準 Windows 專案。 在 Windows Vista 和更新版本中，[**程式**] 類別和 [**使用者帳戶**] 類別沒有此屬性。

「**安全性中心**」類別（僅適用于 Windows XP SP2）也有點非標準。 按一下此類別會在新視窗中開啟 [ **安全性中心** ] 頁面。 針對「 **安全性中心** 」註冊的專案會出現在該頁面下半部的 [ **管理安全性設定：**] 標題下方。 按一下圖示會開啟主控台專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[主控台專案](control-panel-applications.md)
</dt> <dt>

[使用者體驗指南](user-experience-guidelines.md)
</dt> <dt>

[註冊主控台專案](registering-control-panel-items.md)
</dt> <dt>

[使用 CPLApplet](using-cplapplet.md)
</dt> <dt>

[主控台訊息處理](message-processing.md)
</dt> <dt>

[執行主控台專案](executing-control-panel-items.md)
</dt> <dt>

[擴充系統主控台專案](extending-system-control-panel-items.md)
</dt> <dt>

[建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)
</dt> <dt>

[在 Windows Vista 下存取保管庫模式下的主控台](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 





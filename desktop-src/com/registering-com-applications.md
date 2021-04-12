---
title: 註冊 COM 應用程式
description: 註冊 COM 應用程式
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301783"
---
# <a name="registering-com-applications"></a>註冊 COM 應用程式

登錄是系統資料庫，其中包含有關系統硬體和軟體的設定以及系統使用者的資訊。 任何以 Windows 為基礎的程式都可以將資訊新增至登錄，然後從登錄中讀取資訊。 用戶端會搜尋登錄以取得要使用的有趣元件。

登錄會維護系統中安裝之所有 COM 物件的相關資訊。 每當應用程式建立 COM 元件的實例時，系統會諮詢登錄以將元件的 CLSID 或 ProgID 解析成包含該元件的伺服器 DLL 或 EXE 的路徑名稱。 在判斷元件的伺服器之後，Windows 會將伺服器載入用戶端應用程式的進程空間 (同進程元件) 或在其本身的進程空間 (本機和遠端伺服器) 啟動伺服器。 伺服器會建立元件的實例，並將其中一個元件介面的參考傳回給用戶端。

如需 Windows 登錄的詳細資訊，請參閱下列主題：

-   [登錄階層](registry-hierarchy.md)
-   [類別和伺服器](classes-and-servers.md)
-   [分類元件](classifying-components.md)
-   [使用 OleView](using-oleview.md)
-   [註冊元件](registering-components.md)
-   [正在檢查註冊](checking-registration.md)
-   [未知的使用者類型](unknown-user-types.md)
-   [COM 登錄機碼](com-registry-keys.md)

 

 





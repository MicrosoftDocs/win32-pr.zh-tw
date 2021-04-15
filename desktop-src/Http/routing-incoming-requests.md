---
title: 路由傳送連入要求
description: HTTP 伺服器 API 會維護路由資料庫，以判斷哪個應用程式會接收傳入要求。
ms.assetid: 7c613137-66bd-4375-93cb-b5562823bc12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da483030441f3a9239eef153da59212166bce9eb
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104383209"
---
# <a name="routing-incoming-requests"></a>路由傳送連入要求

HTTP 伺服器 API 會維護路由資料庫，以判斷哪個應用程式會接收傳入要求。 路由表是由保留資料庫所建立，其中包含保留專案以及目前的註冊。 進行註冊或保留時，會將它放入對應至主機類型的路由資料庫值區中，如下所示：

-   \+ ：埠註冊會放在「強式萬用字元」 bucket 中

-   主機：埠註冊會放在「明確」 bucket 中

-   IP：埠註冊會放在「IP 系結弱式萬用字元」 bucket 中

-   \* ：埠註冊會放在「弱式萬用字元」 bucket 中

這些步驟也會參考傳入 HTTP 要求的處理順序。 強式萬用字元保留專案會先檢查明確的保留，後面接著 IP 系結的弱式萬用字元和弱式萬用字元。 找到相符的情況時，就會停止搜尋，因此找不到任何剩餘 bucket 中的註冊。

HTTP 伺服器 API 路由演算法會藉由搜尋路由資料庫的註冊專案和保留專案，從強式萬用字元值區開始，並以弱式萬用字元值區結尾，來找出最符合 [UrlPrefix](urlprefix-strings.md) 的專案。 在值區中，最符合的是在 UrlPrefix (的相對 URI 部分中的最長相符項（假設 URL) 的主機、埠和配置部分完全相符）。 在值區中找到相符項之後，路由演算法會停止其搜尋並略過所有較低優先順序的 bucket。

例如，請考慮下列註冊 (根據值區類型以依優先順序遞減的順序列出：

-   註冊： `https://+:80/vroot/` 由應用程式1註冊

-   註冊： `https://adatum.com:80/` 由應用程式2註冊

-   註冊： `https://\*:80/` 由應用程式3註冊

的連入要求 `https://adatum.com:80/vroot/subdir/file.htm/` 會傳遞至應用程式1。 的連入要求 `https://adatum.com:80/default.htm/` 會傳遞至應用程式2。 的連入要求 `https://otheradatum.com:80/file.htm/` 會傳遞至應用程式3。

如果最符合專案是保留專案，這表示應該接收要求的應用程式不在執行中。 例如，請考慮下列註冊和保留：

-   註冊： `https://\*:80/vroot/` 由應用程式1註冊，使用者 A

-   保留： `https://adatum.com:80/` 已保留給使用者 B

的連入要求 `https://adatum.com:80/vroot/file.htm/` 未傳遞至應用程式1，因為最符合專案會導致使用者 B 的保留專案。在此情況下，優先順序規則會套用至優先順序較高的保留。 如果沒有任何作用中的進程已獲授權，並已向其註冊以取得 URL 的服務要求，則會以400狀態碼 (不正確的要求) 來拒絕該要求。

 

 





---
title: 處理註冊
description: HTTP 伺服器 Api 會在註冊期間使用路由資料庫來套用存取檢查。
ms.assetid: d72aa213-b8e8-4fe9-b98c-41114d2cea56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74454d888cccf083e27fc9067c8a5485e286b4f55df4c5c18f2b2e490dc9db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393841"
---
# <a name="processing-registrations"></a>處理註冊

HTTP 伺服器 Api 會在註冊期間使用路由資料庫來套用存取檢查。 [UrlPrefix](urlprefix-strings.md)的註冊必須通過一系列的存取檢查，以確保註冊命名空間的使用者有存取權限。 使用 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函數來新增註冊。

**使用 HttpAddUrl 新增註冊**

1.  如果 UrlPrefix 中的埠號碼具有與 UrlPrefix 中配置不同的配置保留或註冊，則註冊會失敗。 在相同的埠上無法支援 HTTP 和 HTTPS。
2.  註冊時，會將註冊帶到適當的 bucket。 值區是以 URL 的主機類型為基礎，如 [路由傳入要求](routing-incoming-requests.md) 一節中所述。 以下是相對於這個特定值區的步驟。
3.  如果存在重複的註冊專案，則傳回錯誤碼。
4.  選取具有與 UrlPrefix 相同的配置、主機和埠元件的保留專案。 從這些專案找出具有最長 **relativeUri** 相符專案的專案。 如果專案存在，請根據與該專案相關聯的 ACL 來檢查許可權，並傳回成功。 如果專案不存在，則傳回已存在的錯誤程式 \_ \_ 代碼。

下列範例說明在路由資料庫中安裝註冊的程式。 保留1和2存在於路由資料庫中。

-   保留1： `https://+:80/vroot/subdir/` 適用于使用者 A 和使用者 C。此保留專案會放在 "+" bucket 中。
-   保留2： `https://adatum.com:80/vroot/` 適用于使用者 B。此保留專案會放在「明確主機」 bucket 中。
-   註冊： `https://+:80/vroot/subdir/` 依使用者 B 而失敗，因為保留1。
-   註冊： `https://adatum.com:80/vroot/subdir/` 使用者 B 由於保留2而成功。
-   註冊： `https://adatum.com:80/vroot/subdir/` 依使用者 C 失敗，因為有更明確的保留2。 強式萬用字元保留在明確保留或註冊的內容中沒有意義。
-   註冊： `https://+:80/vroot/subdir/` 使用者 A 成功，因為保留1。
-   註冊： `https://adatum.com:80/vroot/anotherdir/` 使用者 B 由於保留2而成功。

註冊的存取檢查不包含委派許可權的檢查。 不會根據保留來檢查存取 (請參閱 [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)) 。 刪除註冊的唯一需求，就是呼叫進程必須建立註冊。

 

 





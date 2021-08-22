---
title: 剖析例外狀況
description: HTTP 伺服器 API 提供登錄機碼，以支援將例外狀況剖析為 HTTP/1.1 規格，以提供回溯相容性。
ms.assetid: b93a3b43-c1ca-41ec-9702-72c1b04aec69
keywords:
- 剖析例外狀況
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b546c5473641bbd5d719908903c2d9e19db25ade2ff6677a5ce5ec7ea472d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950727"
---
# <a name="parsing-exceptions"></a>剖析例外狀況

HTTP 伺服器 API 提供登錄機碼，以支援將例外狀況剖析為 HTTP/1.1 規格，以提供回溯相容性。 這些例外狀況預設不會啟用，而且當伺服器遇到與 HTTP 用戶端的相容性問題時，應該只會以個別案例為基礎啟用。 這些值會在下列登錄位置建立：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Http
               Parameters
```

下表列出提供的登錄機碼，可支援所列的例外狀況。 若要啟用例外狀況，請將對應的金鑰值設定為1，然後重新開機 HTTP 服務。



| 索引鍵名稱                              | 描述                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowWeakHeaderNameSyntax (DWORD)      | 允許 HTTP 剖析器接受具有分隔符號的標頭名稱，例如 '？ '。                                                                                                                                                                                                                                                                                            |
| AllowWeakHeaderValueSyntax (DWORD)     | 允許 HTTP 剖析器接受含有原始 (非重) 控制字元的標頭值。                                                                                                                                                                                                                                                                                   |
| AllowCaseInsensitiveVerbs (DWORD)      | 允許 HTTP 剖析器接受小寫 HTTP 方法/動詞，例如 "get"。                                                                                                                                                                                                                                                                                                    |
| AllowUnEscapedRestrictedChars (DWORD)  | 允許 HTTP 剖析器接受 abspath 中的控制字元，以及 URL 的查詢字串。 如果是絕對 URL，主機名稱中將不允許控制字元。 所有類別的 Url （即 UTF8、DBCS 和 ANSI）都會允許控制字元。 所有 ASCII 控制字元（NUL (0x00) 、LF (0x0a) 、CR (0x0d) 和水準索引標籤 (0x09) 都將被允許。 |



 

 

 





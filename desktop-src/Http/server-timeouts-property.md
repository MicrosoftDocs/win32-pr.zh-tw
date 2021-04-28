---
title: 伺服器超時屬性
description: 伺服器超時屬性
ms.assetid: 5525c226-3786-41c4-86a2-3e077682313d
keywords:
- 伺服器超時屬性 HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26fcd1376e8b7394a3a037bbbe00495466e32609
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090856"
---
# <a name="server-timeouts-property"></a>伺服器超時屬性

HTTP 伺服器 API 可讓應用程式設定伺服器會話或 URL 群組的伺服器連接逾時限制。 HTTP 超時屬性是用來設定應用程式特定的所有超時。 **IdleConnection** 和 **HeaderWait** 計時器也可以設定為「HTTP 伺服器 API 範圍」。 當計時器設定為使用 HTTP 伺服器 API 時，它們會套用至電腦上的所有 HTTP 伺服器 API 應用程式，而設定會在服務重新開機時保存。

如需設定計時器的詳細資訊，請參閱設定 [應用程式特定的超時](configuring-the-application-specific-timeouts.md)。

如果未針對 URL 群組或伺服器會話設定計時器，則會套用 HTTP 伺服器 API 的預設設定。

執行超時的順序如下：

1.  HTTP 伺服器 API 範圍的預設值適用于電腦上的所有 HTTP 伺服器 API 應用程式。
2.  設定時，伺服器會話超時會覆寫 HTTP 伺服器 API 範圍的設定。
3.  設定時，URL 群組設定會覆寫伺服器會話設定。

下表列出預設的連接逾時限制



| 計時器           | 定義                                                                                                        | HTTP 伺服器 API 預設值 | 可設定為 HTTP 伺服器 API 寬 | 可設定為應用程式特定 |
|-----------------|-------------------------------------------------------------------------------------------------------------------|-------------------------|--------------------------------------|--------------------------------------|
| IdleConnection  | 連接會在保持閒置狀態時過期。                                                                        | 120秒                 | 是                                  | 限制                              |
| HeaderWait      | 在等候 HTTP 伺服器 API 剖析標頭時，連接已過期。                                 | 120秒                 | 是                                  | 限制                              |
| EntityBody      | 等待要求實體內容到達時，連接已過期。                                       | 120秒                 | 否                                   | 是                                  |
| DrainEntityBody | 在等候 HTTP 伺服器 API 將實體主體清空 Keep-Alive 連接時，連接已過期。 | 120秒                 | 否                                   | 是                                  |
| MinSendRate     | 連接已過期，因為回應傳送速率低於預設值150位元組/秒。               | 150秒                 | 否                                   | 是                                  |
| RequestQueue    | 連接已過期，因為要求會在應用程式挑選之前保留在要求佇列中。     | 120位元組/秒           | 否                                   | 是                                  |



 

 

 





---
description: 訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。 它們是使用 MESSAGETABLE 資源定義語句在資源檔中宣告的。 若要存取訊息字串，請使用 FormatMessage 函數。
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: 訊息資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6141f78342db2554e85053adda7ee68bdb0e855f213f103da1bb7f62eac1d703
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691818"
---
# <a name="message-tables"></a>訊息資料表

訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。 它們是使用 [MESSAGETABLE](../menurc/messagetable-resource.md) 資源定義語句在資源檔中宣告的。 若要存取訊息字串，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函數。

系統會提供 [系統錯誤碼](system-error-codes.md)的訊息資料表。 若要取得對應至錯誤碼的字串，請使用[](/windows/desktop/api/WinBase/nf-winbase-formatmessage) \_ \_ 來自 \_ 系統旗標的格式訊息來呼叫 FormatMessage。

若要為您的應用程式提供消息表，請依照 [訊息文字檔](../eventlog/message-text-files.md)中的指示進行。 若要從訊息資料表中取出字串， [](/windows/desktop/api/WinBase/nf-winbase-formatmessage)請使用 \_ \_ 來自 HMODULE 旗標的格式訊息來呼叫 FormatMessage \_ 。

 

 

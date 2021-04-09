---
description: 訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。 它們是使用 MESSAGETABLE 資源定義語句在資源檔中宣告的。 若要存取訊息字串，請使用 FormatMessage 函數。
ms.assetid: db84f190-1d1e-4192-8dba-baaee0a3e3ea
title: 訊息資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe12b28c9b4f89d9a6d32c398a2e246940bb79a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936099"
---
# <a name="message-tables"></a>訊息資料表

訊息資料表是顯示錯誤訊息時使用的特殊字元串資源。 它們是使用 [MESSAGETABLE](../menurc/messagetable-resource.md) 資源定義語句在資源檔中宣告的。 若要存取訊息字串，請使用 [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) 函數。

系統會提供 [系統錯誤碼](system-error-codes.md)的訊息資料表。 若要取得對應至錯誤碼的字串，請使用[](/windows/desktop/api/WinBase/nf-winbase-formatmessage) \_ \_ 來自 \_ 系統旗標的格式訊息來呼叫 FormatMessage。

若要為您的應用程式提供消息表，請依照 [訊息文字檔](../eventlog/message-text-files.md)中的指示進行。 若要從訊息資料表中取出字串， [](/windows/desktop/api/WinBase/nf-winbase-formatmessage)請使用 \_ \_ 來自 HMODULE 旗標的格式訊息來呼叫 FormatMessage \_ 。

 

 

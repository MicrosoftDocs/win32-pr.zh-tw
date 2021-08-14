---
description: 資料查詢是要求類別實例的 WQL 語句。 為了發出資料查詢，應用程式會呼叫 IWbemServices：： ExecQuery 或 IWbemServices：： ExecQueryAsync 方法。
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: 要求類別實例資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316285"
---
# <a name="requesting-class-instance-data"></a>要求類別實例資料

資料查詢是要求類別實例的 WQL 語句。 為了發出資料查詢，應用程式會呼叫 [**IWbemServices：： ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) 或 [**Iwbemservices：： ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) 方法。

下列語句會用來進行資料查詢：

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIATORS OF](associators-of-statement.md)
-   [的參考](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

wql SELECT 語句是標準結構化查詢語言 (SQL)  (SQL) 語句來抓取資訊，其中包含一些 WQL 專屬的限制和延伸。 雖然 SQL SELECT 語句通常用於資料庫環境中，以從資料表中取出特定資料行，但是在 WMI 中使用 WQL SELECT 語句來取出單一類別的實例。 WQL 不支援跨多個類別的查詢。

語句的 ASSOCIATORS OF 和參考是針對 WQL 專屬的，而且不是標準 SQL 的一部分。 語句的 ASSOCIATORS OF 會抓取與特定來源類別實例相關聯的所有類別實例，而的參考則會抓取參考特定來源實例的所有實例。 關聯是以 [關聯類別](declaring-an-association-class.md)的實例來表示。

 

 




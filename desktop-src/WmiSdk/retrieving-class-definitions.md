---
description: 架構查詢是要求類別定義的 WQL 語句，以及架構關聯的相關資訊。
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: 正在抓取類別定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114896"
---
# <a name="retrieving-class-definitions"></a>正在抓取類別定義

架構查詢是要求類別定義的 WQL 語句，以及 [架構關聯](schema-associations.md)的相關資訊。 類別提供者會在其 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)類別的實例中使用架構查詢，以指定它們在向 WMI 註冊時所支援的類別。 架構查詢位於 **\_ \_ ClassProviderRegistration** 實例的 **ResultSetQueries**、 **ReferencedSetQueries** 和 **UnsupportedQueries** 屬性中。

架構查詢與資料查詢類似，因為它們支援下列 WQL 語句：

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASSOCIATORS OF](schema-associations.md)
-   [的參考](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

架構查詢類似于指定 **ClassDefsOnly** 關鍵字的資料查詢 [參考](references-of-statement.md);換句話說，它會傳回類別定義物件的結果集，而非關聯類別的實際實例。 但是，的參考只有在有實例存在時才會傳回類別定義。 架構查詢會傳回類別定義，無論實例是否存在。

 

 




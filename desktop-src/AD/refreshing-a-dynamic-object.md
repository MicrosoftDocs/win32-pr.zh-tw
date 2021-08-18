---
title: 重新整理動態物件
description: 用戶端可以重新整理指定目錄專案的存留時間 (TTL) ，讓它以兩種方式的其中一種，在專案進行垃圾收集之前，對其 entryTTL 屬性的值執行 LDAP 更新。
ms.assetid: 5f51013c-b278-4ef7-a235-b238eed79a35
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6c351b559da8d08ccca3346f7126a9bbe47fcd3774486ea64a8dff29ac7e799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025173"
---
# <a name="refreshing-a-dynamic-object"></a>重新整理動態物件

用戶端可以透過下列兩種方式的其中一種，重新整理指定目錄專案的存留時間 (TTL) ，以保持運作狀態：

-   在專案進行垃圾收集之前，對其 **entryTTL** 屬性的值執行 LDAP 更新。 在目錄中重新整理動態專案的這種方法，是 RFC 2589 未指定 Active Directory Domain Services 的額外 (選用) 功能。
-   使用1.3.6.1.4.1.1466.101.119.1 的 OID 執行 LDAP 擴充作業來進行 TTL 重新整理，如 RFC 2589 中的約定。 此 OID 在 WINLDAP 中會定義為 **LDAP \_ TTL \_ 擴充 \_ OP \_ OID** 。

 
* * 備註 * * *：當垃圾收集行程過期時，該物件會被垃圾收集行程移除，而當物件已過期時，就不會有該物件的任何階段。 當您重新整理物件時，您必須小心使用 AD 複寫延遲。 您必須確保重新整理 TTL 的更新會提早過期，因此命名內容的所有複本 (完整和通用類別目錄) 會在物件于本機到期之前查看重新整理交易。

 





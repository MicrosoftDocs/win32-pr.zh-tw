---
title: 使用 ADO 進行範圍抓取
description: 如果使用自動化語言，則應該使用 (ADO) 的 ActiveX 目錄物件，以抓取屬性值的範圍。使用 ADO 進行範圍抓取時，有一個必須特別解決的問題。
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- 使用 ADO 進行範圍抓取 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671111"
---
# <a name="using-ado-for-range-retrieval"></a>使用 ADO 進行範圍抓取

如果使用自動化語言，則應該使用 (ADO) 的 ActiveX 目錄物件，以抓取屬性值的範圍。

使用 ADO 進行範圍抓取時，有一個必須特別解決的問題。 當查詢屬性值的最後一個群組時，ADO 物件將會取出零個物件，即使有更多的物件也一樣。 若要取得其餘的值，請使用範圍萬用字元 ' \* '。 例如，如果群組包含150成員，則可以使用範圍抓取來正常地取出成員值0-100。 如果接著要求範圍101-200，ADO 物件將會傳回零個物件。 此時，必須將查詢修改為要求範圍 101- \* 。 這會將值從101取出至150。 如需詳細資訊和程式碼範例，請參閱 [使用範圍取得群組成員的範例程式碼](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)。

如需使用 ADO 進行範圍抓取的詳細資訊，請參閱：

-   [ADO LDAP 範圍方言](ado-ldap-ranging-dialect.md)
-   [ADO SQL 範圍方言](ado-sql-ranging-dialect.md)
-   [使用範圍取得群組成員的範例程式碼](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 





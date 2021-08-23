---
title: 組合查詢字串
description: 在 Active Directory 中，使用特定篩選準則可提升搜尋效能。 這是因為 Active Directory 會評估所有述詞、識別索引，然後選取一個可能會產生最小傳回值集的索引。
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- 組合查詢字串 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 610ba78d6536d9cfe12f296fcbfa46d04cd572ae05cdb7d3bb8b0e1e7b5d32a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962192"
---
# <a name="assembling-query-strings"></a>組合查詢字串

在 Active Directory 中，使用特定篩選準則可提升搜尋效能。 這是因為 Active Directory 會評估所有述詞、識別索引，然後選取一個可能會產生最小傳回值集的索引。

避免搜尋字串中間或結尾的文字，例如 "cn = \* hille \* " 或 "cn = \* larouse"。

可能的話，請搜尋已編制索引的屬性。 索引屬性會儲存在所有網域控制站上，因此查詢最可能會比搜尋非索引屬性更快。

 

 





---
title: 組合查詢字串
description: 在 Active Directory 中，使用特定篩選準則可提升搜尋效能。 這是因為 Active Directory 會評估所有述詞、識別索引，然後選取一個可能會產生最小傳回值集的索引。
ms.assetid: 4139eedb-1383-4654-9b40-5e294a71be24
ms.tgt_platform: multiple
keywords:
- 組合查詢字串 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e56dec34f63a4a3e12385a36ad5fe5339a0f3d9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967599"
---
# <a name="assembling-query-strings"></a>組合查詢字串

在 Active Directory 中，使用特定篩選準則可提升搜尋效能。 這是因為 Active Directory 會評估所有述詞、識別索引，然後選取一個可能會產生最小傳回值集的索引。

避免搜尋字串中間或結尾的文字，例如 "cn = \* hille \* " 或 "cn = \* larouse"。

可能的話，請搜尋已編制索引的屬性。 索引屬性會儲存在所有網域控制站上，因此查詢最可能會比搜尋非索引屬性更快。

 

 





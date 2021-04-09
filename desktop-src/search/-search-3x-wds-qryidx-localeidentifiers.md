---
description: Inputlocale 和 keywordlocale 識別碼可協助搜尋引擎使用正確的斷詞工具，其方式是識別使用者輸入查詢的語言，以及使用 Advanced Query 語法關鍵字的語言。
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: '地區設定識別碼引數 (Windows Search) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea1549a550e4bf6b8099241a6f3d2275860a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847822"
---
# <a name="locale-identifier-arguments-windows-search"></a>地區設定識別碼引數 (Windows Search) 

`inputlocale`和 `keywordlocale` 識別碼可協助搜尋引擎使用正確的斷詞工具，其方式是識別使用者輸入查詢的語言以及 Advanced Query 語法關鍵字的語言。 這些不一定是 (Lcid) 的語言代碼識別碼，因為 Windows Search 是以許多國際版本提供，而且也包含適用于其他語言的 MUI 套件。 Inputlocale 會識別使用者在中輸入其搜尋查詢之語言的 LCID，而 keywordlocale 則會識別搜尋引擎用於關鍵字的 LCID。

本主題的組織方式如下：

-   [範例](#example)
-   [相關主題](#related-topics)

## <a name="example"></a>範例


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[具有 Parameter-Value 引數的開始使用](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[連結引數](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[語法引數](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY 引數](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[子查詢引數](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 




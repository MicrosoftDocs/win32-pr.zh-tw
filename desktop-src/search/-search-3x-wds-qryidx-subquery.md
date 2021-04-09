---
description: 子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。
ms.assetid: a92c774f-310b-4c40-be1c-0c2b0cac907b
title: " (Windows Search) 的子查詢引數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f673cf9c2a9867593fd6c8fdac83b5901f531257
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943281"
---
# <a name="subquery-argument-windows-search"></a> (Windows Search) 的子查詢引數

子查詢是已儲存的搜尋檔案 (\* . 搜尋-ms) ，您可以用來作為新查詢的篩選準則。 子查詢的結果會用來作為新查詢的來源。 例如，假設您有數個儲存的搜尋檔案，這些檔案會根據電子郵件通訊群組清單來限制查詢： mydepartment。搜尋-ms、j 和 corporatewide。搜尋-毫秒。 使用 `subquery` 引數可讓您將電子郵件搜尋限制在這些儲存的所有搜尋中。

本主題的組織方式如下：

-   [範例](#example)
-   [相關主題](#related-topics)

## <a name="example"></a>範例


```
 search-ms:query=vacation&subquery=mydepartment.search-ms
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[具有 Parameter-Value 引數的開始使用](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[地區設定識別碼引數](-search-3x-wds-qryidx-localeidentifiers.md)
</dt> <dt>

[連結引數](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[語法引數](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[STACKEDBY 引數](-search-3x-wds-qryidx-stackedby.md)
</dt> </dl>

 

 




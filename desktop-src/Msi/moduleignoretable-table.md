---
description: 如果 merge 模組中的資料表列在 ModuleIgnoreTable 資料表中，它就不會合並到 .msi 檔案中。
ms.assetid: 9ff87993-74f6-4436-b0a9-d7ebed6555bd
title: ModuleIgnoreTable 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46337b74f6822b374314a9248f0377ec63359c6576a6ca1398a931d27e548138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042856"
---
# <a name="moduleignoretable-table"></a>ModuleIgnoreTable 資料表

如果 merge 模組中的資料表列在 ModuleIgnoreTable 資料表中，它就不會合並到 .msi 檔案中。 如果資料表已經存在於 .msi 檔案中，則不會被合併修改。 因此，ModuleIgnoreTable 中的資料表可能包含合併後不需要的資料。

ModuleIgnoreTable 資料表具有下列資料行。



| Column | 類型                         | 答案 | Nullable |
|--------|------------------------------|-----|----------|
| 資料表  | [識別碼](identifier.md) | Y   | 否       |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>表
</dt> <dd>

合併模組中的資料表名稱，不會合並到 .msi 檔案中。

</dd> </dl>

## <a name="remarks"></a>備註

若要將 .msm 檔案的大小降到最低，建議開發人員從用於轉散發的模組中移除未使用的資料表，而不是在 ModuleIgnoreTable 資料表中列出這些資料表。

 

 




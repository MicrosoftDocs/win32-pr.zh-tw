---
description: ICEM02 會確認所有模組相依性和排除專案都與目前的模組相關。
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 332ad83ba753984d752a78bebc19bc17e3b5d25ef8b580f9f105a9577d016318
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430818"
---
# <a name="icem02"></a>ICEM02

ICEM02 會確認所有模組相依性和排除專案都與目前的模組相關。

Merge module 會儲存在合併模組中，名為 Mergemod 的 .cub 檔中，而不是在包含用於封裝驗證的 Ices-003 的 .cub 檔案中。

## <a name="result"></a>結果

如果模組資料庫嘗試指定與目前模組無關的相依性或排除專案，ICEM02 會張貼錯誤訊息。 如果模組資料庫嘗試將目前的模組指定為相依或本身排除，ICEM02 會張貼錯誤訊息。

## <a name="example"></a>範例

ICEM02 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[ModuleSignature 資料表](modulesignature-table.md)



| ModuleID         | 語言 | 版本 |
|------------------|----------|---------|
| MyModule.*GUID1* | 1033     | 1.0     |



 

[ModuleDependency 資料表](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule.*GUID2* | 1033           | OtherModule.*GUID3* | 0                | 1.0             |
| MyModule.*GUID1*    | 1033           | MyModule.*GUID1*    | 1033             | 1.2             |



 

[ModuleExclusion 資料表](moduleexclusion-table.md) (部分) 



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule.*GUID2* | 1033           | OtherModule.*GUID3* | 0                |
| MyModule.*GUID1*    | 1033           | MyModule.*GUID1*    | 1033             |



 

Merge module ICE 會張貼第一個錯誤，因為 ModuleDependency 資料表中第一個資料列的是，它並未針對 ModuleSignature 資料表中指定的目前模組指定必要的相依性。 模組的相依性只能在它自己的 ModuleDependency 資料表中指定。 如果為 OtherModule，則為。目前的模組需要 *GUID3* ，請使用 ModuleSignature 資料表中的資料來取代資料列的前兩個數據行。 如果為 OtherModule，則為。此模組不需要 *GUID3* ，請刪除此資料列。

合併模組 ICE 會張貼第二個錯誤，因為模組無法自行指定相依性。

Merge module ICE 會張貼第三個錯誤，因為 ModuleExclusion 資料表中的第一個資料列不會針對 ModuleSignature 資料表中指定的目前模組指定必要的排除。 模組的排除專案只能在它自己的 ModuleExclusion 資料表中指定。 如果目前的模組排除 OtherModule。*GUID3*，將資料列的前兩個數據行取代為 ModuleSignature 資料表中的資料。 如果目前的模組未排除 OtherModule。*GUID3*，請刪除此資料列。

合併模組 ICE 會張貼第四個錯誤，因為模組無法指定它本身排除。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




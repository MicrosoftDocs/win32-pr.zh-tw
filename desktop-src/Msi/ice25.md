---
description: ICE25 會驗證 .msi 檔案是否符合其所有的內部合併模組相依性和排除專案。
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850179"
---
# <a name="ice25"></a>ICE25

ICE25 會驗證 .msi 檔案是否符合其所有的內部 [合併模組](merge-modules.md) 相依性和排除專案。 ICE 會驗證下列各項：

-   在 .msi 檔案的 [ModuleDependency 資料表](moduledependency-table.md) 中指出的所有合併模組相依性，都是由 [ModuleSignature 資料表](modulesignature-table.md)中至少列出一個合併模組所滿足。
-   [ModuleExclusion 資料表](moduleexclusion-table.md)中沒有任何已排除的合併模組與[ModuleSignature 資料表](modulesignature-table.md)中所列的合併模組不相容。

## <a name="result"></a>結果

如果 .msi 檔案先前與不相容的合併模組合併，或尚未與必要的合併模組合併，ICE25 會張貼錯誤訊息。

## <a name="example"></a>範例

ICE25 會針對所顯示的範例張貼下列錯誤。

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[ModuleSignature 資料表](modulesignature-table.md)



| ModuleID | 語言 | 版本 |
|----------|----------|---------|
| ModuleA  | 0        | 1.0     |
| ModuleB  | 1033     | 1.0     |



 

[ModuleDependency 資料表](moduledependency-table.md)



| ModuleID | ModuleLanguage | RequiredID | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| ModuleA  | 0              | ModuleX    | 0                | 2.0             |



 

[ModuleExclusion 資料表](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| ModuleA  | 0              | ModuleB    | 1033             |                    |                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




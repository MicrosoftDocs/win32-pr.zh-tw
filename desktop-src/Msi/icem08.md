---
description: ICEM08 可確保模組不會排除其相依的另一個模組。
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884217"
---
# <a name="icem08"></a>ICEM08

ICEM08 可確保模組不會排除其相依的另一個模組。

## <a name="result"></a>結果

當模組排除相依的另一個模組時，ICEM08 會張貼錯誤。

## <a name="example"></a>範例

ICEM08 會針對包含範例中所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[ModuleDependency 資料表](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA。 &lt;GUID&gt; | 1033           | ModuleB。 &lt;GUID&gt; | 1033             | 1.0             |



 

[ModuleExclusion 資料表](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA。 &lt;GUID&gt; | 1033           | ModuleB。 &lt;GUID&gt; | 1033             |                    | 1.0                |



 

若要修正錯誤，請移除相依性或排除。 如果 ModuleB 是 (RequiredID) 的相依性，您就無法將它排除 (如 ModuleExclusion 資料表) 的 ExludedID 資料行所示。 如果您必須排除 ModuleB，則必須移除 ModuleA 的相依性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




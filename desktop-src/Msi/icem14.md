---
description: ICEM14 會驗證 ModuleSubstitution 資料表的 Value 資料行。
ms.assetid: e07ba63a-e748-4835-ae1b-9f7d30e46d39
title: ICEM14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72223f27338fb08efe4ea95b817acebd6234063f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114332"
---
# <a name="icem14"></a>ICEM14

ICEM14 會驗證 [ModuleSubstitution 資料表](modulesubstitution-table.md)的 Value 資料行。

## <a name="result"></a>結果

ICEM14 會張貼下列錯誤。



| 錯誤                                                                                                                                                         | 意義                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 資料列 \[ 1 \] \[ 中 ModuleSubstitution 資料行的取代字串。2 \] . \[\]在 ModuleConfiguration 資料表中找不到3。                                 | \[1 \] . \[2 \] . \[3 \] 指的是 ModuleSubstitution 資料表中資料 *列的資料表.* 資料行主鍵。 此資料列的 [值] 欄位中的格式化範本未對應至 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中可設定屬性的資料列。                                                            |
| 在第1列的 ModuleSubstitution 資料表中 \[ \] 。 \[2 \] . \[3 \] ，資料表 '% s ' 中指出可設定的專案。 資料表 '% s ' 不能包含可設定的專案。 | 下列其中一個資料表列在 ModuleSubstitution 資料表的資料表資料行中： [ModuleSubstitution](modulesubstitution-table.md)、 [ModuleConfiguration](moduleconfiguration-table.md)、 [ModuleExclusion](moduleexclusion-table.md)或 [ModuleSignature](modulesignature-table.md)。 這些資料表不能包含可設定的欄位。 |
| 在第1列的 ModuleSubstitution 資料表中 \[ \] 。 \[2 \] . \[3 \] ，指定空的取代字串。                                                               | 此資料列的 [值] 欄位中的格式化範本未對應至 [ModuleConfiguration 資料表](moduleconfiguration-table.md)中可設定屬性的資料列。                                                                                                                                                                    |



 

ICEM14 會張貼下列警告。



| 警告                                                                  | 意義                                  |
|--------------------------------------------------------------------------|------------------------------------------|
| 存在 ModuleSubstitution 資料表，但遺漏 ModuleConfiguration 資料表 | ModuleConfiguration 資料表不存在。 |



 

## <a name="table-used-during-execution"></a>執行期間所使用的資料表

[ModuleSubstitution 資料表](modulesubstitution-table.md)

[ModuleConfiguration 資料表](moduleconfiguration-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 




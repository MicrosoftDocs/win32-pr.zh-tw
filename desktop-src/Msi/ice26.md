---
description: ICE26 會驗證 Windows Installer 資料庫中的順序資料表。
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850176"
---
# <a name="ice26"></a>ICE26

ICE26 會驗證下列每一個 [*順序資料表*](s-gly.md) 都包含資料表所需的動作，而且不包含資料表中不允許的任何動作：

-   [AdminUISequence 資料表](adminuisequence-table.md)
-   [AdminExecuteSequence 資料表](adminexecutesequence-table.md)
-   [InstallUISequence 資料表](installuisequence-table.md)
-   [InstallExecuteSequence 資料表](installexecutesequence-table.md)

## <a name="result"></a>結果

如果安裝封裝的順序資料表缺少必要的動作，或包含不允許的動作，ICE26 會張貼錯誤訊息。

## <a name="example"></a>範例



| ICE26 錯誤                                                                   | Description                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 動作： InstallExecuteSequence 順序資料表中必須有 ' Action1 '。   | 指定的順序資料表中遺漏必要的動作。 請參閱 [使用順序資料表](using-a-sequence-table.md)中的 template.msi 或建議的順序資料表。 |
| 動作： InstallExecuteSequence 順序資料表中禁止 ' Action2 '。 | 這個動作不能在指定的順序資料表中。 從順序資料表中移除此動作。                                                                             |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




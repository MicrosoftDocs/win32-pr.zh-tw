---
description: ICE82 會驗證 RegisterProduct 動作、RegisterUser 動作、PublishProduct 動作和 PublishFeatures 動作都存在於 InstallExecuteSequence 資料表中。 如果所有動作都存在，則會驗證套件。
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694251"
---
# <a name="ice82"></a>ICE82

ICE82 會驗證 [RegisterProduct 動作](registerproduct-action.md)、 [RegisterUser 動作](registeruser-action.md)、 [PublishProduct 動作](publishproduct-action.md)和 [PublishFeatures 動作](publishfeatures-action.md) 都存在於 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。 如果所有動作都存在，則會驗證套件。

ICE82 會在 InstallExecuteSequence、InstallUISequence、AdminExecuteSequence、AdminUISequence 或 AdvtExecuteSequence 資料表中列出兩個具有相同序號的動作時張貼警告。

## <a name="result"></a>結果

ICE82 會張貼下列警告。



| ICE82 警告                                                                                                                                                                                                                 | Description                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstallExecuteSequence 資料表未包含以下所述的動作集合：缺少的動作：<br/> 發佈功能<br/> 發佈產品<br/> 註冊產品<br/> 註冊使用者<br/> | 如果所有四個動作都不存在，則 ICE82 自訂動作會張貼警告。                                                                                                                                         |
| 此動作 \[ 1 \] \[ \] 在資料表3中有重複的序號 \[ 2 \] 。                                                                                                                                                     | ICE82 會在 InstallExecuteSequence、InstallUISequence、AdminExecuteSequence、AdminUISequence 或 AdvtExecuteSequence 資料表中列出兩個具有相同序號的動作時張貼警告。 |



 

ICE82 會張貼下列錯誤。



| ICE82 錯誤                                                                                                                                                                                                                                        | Description                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| InstallExecuteSequence 應包含以下所述的所有動作，或不存在任何動作<br/> <List of actions present> <br/> 遺漏的動作：<br/> <List of actions missing> <br/> | 如果有四個動作中有部分存在，而其他動作都不存在，ICE82 就會張貼錯誤。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 





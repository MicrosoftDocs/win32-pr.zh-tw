---
description: ICE13 會驗證順序資料表中的對話是否出現在 AdminUISequence 或 InstallUISequence 資料表中。 對話方塊不得列在 InstallExecuteSequence、AdminExecuteSequence 或 AdvtExecuteSequence 資料表中。
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944536"
---
# <a name="ice13"></a>ICE13

ICE13 會驗證順序資料表中的對話是否出現在 [AdminUISequence](adminuisequence-table.md)或 [InstallUISequence](installuisequence-table.md) 資料表中。 對話方塊不得列在 [InstallExecuteSequence](installexecutesequence-table.md)、 [AdminExecuteSequence](adminexecutesequence-table.md)或 [AdvtExecuteSequence](advtexecutesequence-table.md) 資料表中。

## <a name="result"></a>結果

如果對話方塊出現在執行順序資料表中，ICE13 會張貼一則錯誤訊息。

## <a name="example"></a>範例

在下列範例中，ICE13 會張貼錯誤訊息，指出 ' WelcomeDialog ' 不能列在 ' InstallExecuteSequence ' 資料表中。

[InstallExecuteSequence 資料表](installexecutesequence-table.md) (部分) 



| 動作          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| WelcomeDialog   |



 

[InstallUISequence 資料表](installuisequence-table.md) (部分) 



| 動作         |
|----------------|
| CostFinalize   |
| CostInitialize |
| BrowseDialog   |



 

[對話方塊資料表](dialog-table.md) (部分) 



| 對話        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




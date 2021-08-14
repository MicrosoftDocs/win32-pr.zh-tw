---
description: ICE13 會驗證順序資料表中的對話是否出現在 AdminUISequence 或 InstallUISequence 資料表中。 對話方塊不得列在 InstallExecuteSequence、AdminExecuteSequence 或 AdvtExecuteSequence 資料表中。
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc11f8254c721d404a65e63fc897aa6e55bc61364c768b48f2d5aded4348d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946632"
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

 

 




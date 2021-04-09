---
description: ICE28 通常用來驗證 ForceReboot 動作是放在動作順序資料表中的特定動作群組之前或之後，而不在其中。 請參閱 ForceReboot 動作主題，以判斷組成此群組的動作。
ms.assetid: 746d907a-33e1-479a-bcb0-93e7fd5dd975
title: ICE28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc65878bdc3db4f9b79ba95b4a170b694a4728ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689743"
---
# <a name="ice28"></a>ICE28

ICE28 通常用來驗證 ForceReboot 動作是放在動作順序資料表中的特定動作群組之前或之後，而不在其中。 請參閱 [ForceReboot 動作](forcereboot-action.md) 主題，以判斷組成此群組的動作。

ICE28 會驗證下列順序資料表中的動作：

[AdminUISequence 資料表](adminuisequence-table.md)

[AdminExecuteSequence 資料表](adminexecutesequence-table.md)

[InstallUISequence 資料表](installuisequence-table.md)

[InstallExecuteSequence 資料表](installexecutesequence-table.md)

## <a name="result"></a>結果

如果在指定的動作群組內排序 ForceReboot，ICE28 會張貼錯誤訊息。

## <a name="example"></a>範例

如範例所示，ICE28 會張貼下列錯誤訊息：

``` syntax
Action: 'ForceReboot' of table InstallExecuteSequence is not permitted in the range 5 to 15 because it cannot separate a set of actions contained in this range.
```

[InstallExecuteSequence 資料表](installexecutesequence-table.md)



| 動作             | 順序 |
|--------------------|----------|
| ForceReboot        | 10       |
| RegisterMIMEInfo   |   5      |
| RegisterProgIdInfo | 15       |



 

指定給 ForceReboot 中斷的序號會產生錯誤，因為它位於 RegisterMIMEInfo 和 RegisterProgIdInfo 的序號之間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 




---
description: InstallExecuteSequence 資料表會列出執行最上層安裝動作時所執行的動作。
ms.assetid: 995d4159-bfc9-48b2-8328-3ae8251d785d
title: InstallExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d48fb83bd8f3c947feb81ab95df490572ba1ee68d423957759a95c323005070
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142162"
---
# <a name="installexecutesequence-table"></a>InstallExecuteSequence 資料表

InstallExecuteSequence 資料表會列出執行最上層 [安裝動作](install-action.md) 時所執行的動作。

安裝順序中的動作，直到 [InstallValidate 動作](installvalidate-action.md)和任何結束對話方塊都位於 [InstallUISequence 資料表](installuisequence-table.md)中。 從 InstallValidate 到安裝順序結束的所有動作都會在 InstallExecuteSequence 資料表中。 由於 InstallExecuteSequence 資料表需要獨立，因此它具有任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md) 動作。

需要使用者介面的 [自訂動作](custom-actions.md)應使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，而不是使用 [對話方塊資料表](dialog-table.md)所建立的編寫對話方塊。

InstallExecuteSequence 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 動作    | [識別碼](identifier.md) | Y   | N        |
| 條件 | [Condition](condition.md)   | N   | Y        |
| 順序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要執行之動作的名稱。 這可能是內建動作或自訂動作。

主表索引鍵。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

此欄位包含條件運算式。 如果運算式評估為 False，則會略過該動作。 如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。 如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

決定執行此動作之順序位置的數位。

正值表示序列位置。 Null 值表示不執行動作。 下列負數值表示如果安裝程式傳回相關聯的終止旗標，則會執行此動作。 每個終止旗標 (負數值) 可用於不超過一個動作。 多個動作可以有終止旗標，但它們必須是不同的旗標。 終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。



| 終止旗標          | 值 | 描述                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | 順利完成。 與 [結束] [對話方塊一起使用](exit-dialog.md) 。               |
| msiDoActionStatusUserExit | -2    | 使用者終止安裝。 搭配 [UserExit](userexit-dialog.md) 對話方塊使用。     |
| msiDoActionStatusFailure  | -3    | 嚴重結束終止。 搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。 |
| msiDoActionStatusSuspend  | -4    | 安裝已暫停。                                                                |



 

零、所有其他負數或 Null 值表示永遠不會執行動作。

</dd> </dl>

## <a name="remarks"></a>備註

進度顯示或記錄的當地語系化文字是在 [ActionText 資料表](actiontext-table.md)中指定的。

如需順序資料表的範例，請參閱 [使用順序資料表](using-a-sequence-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
</dl>

 

 




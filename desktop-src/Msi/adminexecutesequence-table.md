---
description: AdminExecuteSequence 資料表會列出安裝程式在執行最上層系統管理動作時，會依序呼叫的動作。
ms.assetid: 33a2ef50-519b-424e-b510-55c21c5706a3
title: AdminExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c62ae43f8436ab210765e5402751c5722b78b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986891"
---
# <a name="adminexecutesequence-table"></a>AdminExecuteSequence 資料表

AdminExecuteSequence 資料表會列出安裝程式在執行最上層系統 [管理動作](admin-action.md) 時，會依序呼叫的動作。

安裝順序中的系統管理動作（最多 [InstallValidate 動作](installvalidate-action.md) 和任何結束對話方塊）都位於 [AdminUISequence 資料表](adminuisequence-table.md)中。

從 InstallValidate 動作到安裝順序結束的系統管理動作都位於 AdminExecuteSequence 資料表中。 由於 AdminExecuteSequence 資料表需要獨立，因此它也包含任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md)。

需要使用者介面的 [自訂動作](custom-actions.md)應使用 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) ，而不是使用 [對話方塊資料表](dialog-table.md)所建立的編寫對話方塊。

這些資料行與 [InstallExecuteSequence 資料表](installexecutesequence-table.md)的資料行相同。 AdminExecuteSequence 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 動作    | [識別碼](identifier.md) | Y   | N        |
| 條件 | [Condition](condition.md)   | N   | Y        |
| 順序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要執行之動作的名稱。 這是 [CustomAction 資料表](customaction-table.md)中所列的標準動作或自訂動作。

主表索引鍵。

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件
</dt> <dd>

邏輯運算式。 如果運算式評估為 false，則會略過該動作。 如果運算式語法無效，則序列會終止，並傳回 iesBadActionData。 如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

正值表示動作的序列位置。 下列負數值表示如果安裝程式傳回終止旗標，則會呼叫動作。 每個終止旗標 (負數值) 可用於不超過一個動作。 多個動作可以有終止旗標，但它們必須是不同的旗標。 終止旗標 (負數值) 通常會與 [對話方塊](dialog-boxes.md)一起使用。



| 終止旗標          | 值 | 描述                                                                          |
|---------------------------|-------|--------------------------------------------------------------------------------------|
| msiDoActionStatusSuccess  | -1    | 順利完成。 與 [結束] [對話方塊一起使用](exit-dialog.md) 。               |
| msiDoActionStatusUserExit | -2    | 使用者終止安裝。 搭配 [UserExit](userexit-dialog.md) 對話方塊使用。     |
| msiDoActionStatusFailure  | -3    | 嚴重結束終止。 搭配 [FatalError](fatalerror-dialog.md) 對話方塊使用。 |
| msiDoActionStatusSuspend  | -4    | 安裝已暫停。                                                                |



 

零、所有其他負數或 null 值表示永遠不會呼叫該動作。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE13](ice13.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 




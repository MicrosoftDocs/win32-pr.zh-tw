---
description: AdminUISequence 資料表會列出當執行最上層系統管理員動作，而內部使用者介面層級設定為完整 UI 或縮減 UI 時，安裝程式會依序呼叫的動作。
ms.assetid: 7227846d-b755-4af9-acc3-e27742a5097a
title: AdminUISequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8fb460f65d223e75ebd50a7587f5b3f4adeced8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977044"
---
# <a name="adminuisequence-table"></a>AdminUISequence 資料表

AdminUISequence 資料表會列出當執行最上層系統 [管理員動作](admin-action.md) ，而內部使用者介面層級設定為完整 ui 或縮減 ui 時，安裝程式會依序呼叫的動作。 如果使用者介面層級設定為基本 UI 或沒有 UI，則安裝程式會略過此資料表中的動作。 [關於消費者介面的詳細資訊，](about-the-user-interface.md)請參閱。

安裝順序中的系統管理動作，直到 [InstallValidate 動作](installvalidate-action.md)和任何結束對話方塊都位於 AdminUISequence 資料表中。 從 InstallValidate 到安裝順序結束的所有動作都會在 [AdminExecuteSequence 資料表](adminexecutesequence-table.md)中。 由於 AdminExecuteSequence 資料表需要獨立，因此它也包含任何必要的初始化動作，例如 [LaunchConditions](launchconditions-action.md)、 [CostInitialize](costinitialize-action.md)、 [FileCost](filecost-action.md)和 [CostFinalize](costfinalize-action.md)。 它也有 [ExecuteAction 動作](executeaction-action.md)。

這些資料行與 [InstallUISequence 資料表](installuisequence-table.md)的資料行相同。 AdminUISequence 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 動作    | [識別碼](identifier.md) | Y   | N        |
| 條件 | [Condition](condition.md)   | N   | Y        |
| 順序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

要執行之動作的名稱。 這是標準動作、使用者介面 wizard 或 [CustomAction 資料表](customaction-table.md)中所列的自訂動作。

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
[ICE20](ice20.md)  
[ICE26](ice26.md)  
[ICE27](ice27.md)  
[ICE28](ice28.md)  
[ICE46](ice46.md)  
[ICE75](ice75.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICE96](ice96.md)  
[ICEM04](icem04.md)  
</dl>

 

 




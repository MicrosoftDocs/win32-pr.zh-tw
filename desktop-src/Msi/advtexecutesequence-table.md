---
description: AdvtExecuteSequence 資料表會列出安裝程式在執行最上層通告動作時所呼叫的動作。
ms.assetid: 8873c161-a709-48b8-a66f-fe2ee9be859f
title: AdvtExecuteSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed9a566b721be1065e825cbf7cd6650a52c83ace653dc2730f1fcf7785d125c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381587"
---
# <a name="advtexecutesequence-table"></a>AdvtExecuteSequence 資料表

AdvtExecuteSequence 資料表會列出安裝程式在執行最上層 [通告動作](advertise-action.md) 時所呼叫的動作。

只有下列動作可以在 AdvtExecuteSequence 資料表中使用。 自訂動作不能用在此資料表中。

[CostFinalize](costfinalize-action.md)

[CostInitialize](costinitialize-action.md)

[CreateShortcuts](createshortcuts-action.md)

[InstallFinalize](installfinalize-action.md)

[InstallInitialize](installinitialize-action.md)

[InstallValidate](installvalidate-action.md)

[MsiPublishAssemblies](msipublishassemblies-action.md)

[PublishComponents](publishcomponents-action.md)

[PublishFeatures](publishfeatures-action.md)

[PublishProduct](publishproduct-action.md)

[RegisterClassInfo](registerclassinfo-action.md)

[RegisterExtensionInfo](registerextensioninfo-action.md)

[RegisterMIMEInfo](registermimeinfo-action.md)

[RegisterProgIdInfo](registerprogidinfo-action.md)

這些資料行與 [InstallExecuteSequence 資料表](installexecutesequence-table.md)的資料行相同。 AdvtExecuteSequence 資料表具有下列資料行。



| Column    | 類型                         | 答案 | Nullable |
|-----------|------------------------------|-----|----------|
| 動作    | [識別碼](identifier.md) | Y   | N        |
| 條件 | [Condition](condition.md)   | N   | Y        |
| 順序  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

安裝程式要執行的 [標準動作](standard-actions.md) 名稱。 這是資料表的主鍵。

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
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE72](ice72.md)  
[ICE79](ice79.md)  
[ICE82](ice82.md)  
[ICE83](ice83.md)  
[ICE84](ice84.md)  
[ICE86](ice86.md)  
[ICEM04](icem04.md)  
</dl>

 

 




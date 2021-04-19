---
description: ActionText 資料表包含要在 [進度] 對話方塊中顯示的文字，並會寫入記錄檔中，以找出需要很長時間才能執行的動作。 顯示的文字包含動作描述，以及來自動作的選擇性格式化資料。
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: ActionText 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8071a8542571a3364e151522a7fc4c0b11362045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106980813"
---
# <a name="actiontext-table"></a>ActionText 資料表

ActionText 資料表包含要在 [進度] 對話方塊中顯示的文字，並會寫入記錄檔中，以找出需要很長時間才能執行的動作。 顯示的文字包含動作描述，以及來自動作的選擇性格式化資料。

ActionText 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 動作      | [識別碼](identifier.md) | Y   | N        |
| Description | [Text](text.md)             | N   | Y        |
| 範本    | [範本](template.md)     | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>行動
</dt> <dd>

動作的名稱。

主表索引鍵。

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述
</dt> <dd>

顯示在 [進度] 對話方塊中，或在執行動作時寫入至記錄檔的當地語系化描述。

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>範本
</dt> <dd>

當地語系化的格式範本，用來格式化動作資料記錄，以便在執行動作時顯示。 如果未提供範本，則不會顯示動作資料。

</dd> </dl>

## <a name="remarks"></a>備註

一般而言，ActionText 資料表中的專案會參考順序資料表中的動作。 安裝程式所執行的其他動作不會列在順序資料表中，但仍然需要在資料表中指定。 下表識別必要的資料表專案，其中必須完全依照顯示的方式撰寫動作名稱和範本，但是可以自訂描述。



| 動作          | 描述                             | 範本 |
|-----------------|-----------------------------------------|----------|
| 復原        | 復原動作。                         | \[1\]    |
| RollbackCleanup | 移除舊檔案。                      | \[1\]    |
| GenerateScript  | 產生動作的系統作業。 | \[1\]    |



 

> [!Note]  
> 只有在安裝腳本內執行的動作才會顯示動作文字。 因此，只有在 [InstallInitialize](installinitialize-action.md) 和 [InstallFinalize](installfinalize-action.md) 動作之間排序的動作才會顯示動作文字。

 

您可以使用 Msidb.exe 或 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)，將當地語系化的 ActionText 資料表匯入資料庫中。 SDK 包含當地語系化的 ActionText 資料表，適用于「 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) 」一節中所列的每一種語言。 如果未填入 ActionText 資料表，安裝程式會針對 [**ProductLanguage**](productlanguage.md) 屬性所指定的語言載入當地語系化的字串。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 




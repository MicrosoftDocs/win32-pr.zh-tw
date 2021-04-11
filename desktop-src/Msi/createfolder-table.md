---
description: CreateFolder 資料表包含需要針對特定元件明確建立之資料夾的參考。
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193921"
---
# <a name="createfolder-table"></a>CreateFolder 資料表

CreateFolder 資料表包含需要針對特定元件明確建立之資料夾的參考。

CreateFolder 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 目錄\_ | [識別碼](identifier.md) | Y   | N        |
| 元件\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_
</dt> <dd>

在 [目錄資料表](directory-table.md)的第一個資料行中的外部索引鍵。

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_
</dt> <dd>

在 [元件資料表](component-table.md)的第一個資料行中的外部索引鍵。

</dd> </dl>

## <a name="remarks"></a>備註

安裝元件時，會建立此資料表中的資料夾。 只有在元件已卸載或移至從來源執行時，才會嘗試移除這些資料夾。 如果資料夾變成空白，則不會觸發自動移除。 相反地，安裝程式所建立但未列在此資料表中的資料夾，會在它們變成空白時移除。

因為安裝程式所建立的資料夾是空的，所以您必須在 CreateFolder 資料表中撰寫一個專案，才能安裝包含空資料夾的元件。

當呼叫 [CreateFolders](createfolders-action.md) 動作或 [RemoveFolders](removefolders-action.md) 動作時，就會參考此資料表。

如需如何保護資料夾的詳細資訊，請參閱 [MsiLockPermissionsEx 資料表](msilockpermissionsex-table.md) 和 [LockPermissions 資料表](lockpermissions-table.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE18](ice18.md)  
[ICE32](ice32.md)  
[ICE55](ice55.md)  
</dl>

 

 




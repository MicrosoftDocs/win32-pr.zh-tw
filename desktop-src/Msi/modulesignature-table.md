---
description: ModuleSignature 資料表是必要的資料表。
ms.assetid: 09802282-72ad-43f1-8cce-4cdc68b01e87
title: ModuleSignature 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d75e3bb013472c49d18fa44b840ce07b11728faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513489"
---
# <a name="modulesignature-table"></a>ModuleSignature 資料表

ModuleSignature 資料表是必要的資料表。 它包含識別合併模組所需的所有資訊。 合併工具會將此資料表加入至 .msi 檔案（如果尚未存在的話）。 Merge 模組中的 ModuleSignature 資料表只有一個資料列包含 ModuleID、Language 和 Version。 不過，.msi 檔案中的 ModuleSignature 資料表具有一個資料列，其中包含每個已合併至其中的 .msm 檔案的這項資訊。

合併和驗證工具會檢查 .msi 檔案中的 ModuleSignature 資料表，以判斷它是否具有目前合併模組所需的所有相依合併模組 (請參閱 [ModuleDependency 資料表](moduledependency-table.md)) 以及安裝封裝是否先前與任何衝突的合併模組合併 (請參閱 [ModuleExclusion 資料表](moduleexclusion-table.md)) 。

ModuleSignature 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| ModuleID | [識別碼](identifier.md) | Y   | N        |
| 語言 | [整數](integer.md)       | Y   | N        |
| 版本  | [版本](version.md)       |     | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID
</dt> <dd>

可唯一識別合併模組的識別碼。 除非合併模組與其前身完全相容，否則兩個合併模組不能具有相同的 ModuleID。 您可以使用 GUIDGEN 之類的公用程式來建立此欄位的 GUID。 ModuleID 資料行是資料表的主鍵，因此必須遵循命名慣例來 [命名合併模組資料庫中的主鍵](naming-primary-keys-in-merge-module-databases.md)。 例如，如果合併模組的可讀取名稱是 MyLibrary，而 GUID 是 {880DE2F0-CDD8-11D1-A849-006097ABDE17}，則 ModuleID 資料行中的專案會變成 MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 A849 006097ABDE17 \_ \_ 。

</dd> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>語言
</dt> <dd>

語言識別項會指定合併模組的預設語言。 語言識別項採用十進位格式，例如，美國英文為1033。 合併模組所使用的語言可以藉由在合併之前套用轉換至合併模組來變更。

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>版本
</dt> <dd>

[版本] 欄位包含描述合併模組之主要和次要版本的字串。

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多個語言合併模組](multiple-language-merge-modules.md)
</dt> </dl>

 

 




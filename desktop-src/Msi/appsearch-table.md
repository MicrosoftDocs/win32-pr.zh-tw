---
description: AppSearch 資料表包含搜尋具有特定檔案簽章的檔案時所需的屬性。 AppSearch 資料表也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: AppSearch 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192461"
---
# <a name="appsearch-table"></a>AppSearch 資料表

AppSearch 資料表包含搜尋具有特定檔案簽章的檔案時所需的屬性。 AppSearch 資料表也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。

AppSearch 資料表具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| 屬性    | [識別碼](identifier.md) | Y   | N        |
| 簽名\_ | [識別碼](identifier.md) | Y   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

執行 [AppSearch](appsearch-action.md) 動作時，會將這個屬性設定為簽章資料行所指出的檔案位置 \_ 。 如果使用者的電腦上有檔案簽章，就會設定這個屬性。 此資料行中使用的屬性必須是 [公用](public-properties.md) 屬性，而且具有不包含小寫字母的識別碼。

[屬性] 欄位中所列的屬性，可以在 [屬性](property-table.md) 表中或從命令列初始化。 如果 [AppSearch](appsearch-action.md) 動作找出簽章，則安裝程式會使用找到的值來覆寫已初始化的屬性值。 如果找不到簽章，則會使用初始屬性值。 如果屬性從未初始化，則只有在找到簽章時，才會設定屬性。 否則，屬性會是未定義的。

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>簽名\_
</dt> <dd>

簽章資料 \_ 行包含稱為簽章的唯一識別碼，而且也是 [RegLocator](reglocator-table.md)、 [IniLocator](inilocator-table.md)、 [CompLocator](complocator-table.md)和 [DrLocator](drlocator-table.md) 資料表中的外部索引鍵。 搜尋檔案時，這個資料行中的值也必須是簽 [章資料表中的外](signature-table.md) 鍵。 如果此資料行中的值未列在簽章資料表中，安裝程式會判斷搜尋是否為目錄。

</dd> </dl>

## <a name="remarks"></a>備註

[*順序資料表*](s-gly.md)中的 [AppSearch](appsearch-action.md)動作會處理此資料表中的資訊。 如需使用 *順序資料表* 的詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md)。

[AppSearch](appsearch-action.md)動作會先使用[CompLocator](complocator-table.md)資料表、 [RegLocator](reglocator-table.md)資料表第二個、 [IniLocator](inilocator-table.md)資料表第三個，最後是[DrLocator](drlocator-table.md)資料表來搜尋簽章。 簽章會 [列在簽章資料表中](signature-table.md) 。 不在簽章資料表中的簽章代表目錄，而動作則會將屬性設定為該簽章的目錄路徑。

請參閱 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)。

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 




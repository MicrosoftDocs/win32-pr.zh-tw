---
description: AppSearch 動作會使用檔案簽章來搜尋現有的產品版本。
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: AppSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192462"
---
# <a name="appsearch-action"></a>AppSearch 動作

AppSearch 動作會使用檔案簽章來搜尋現有的產品版本。 AppSearch 動作可能會使用此資訊來判斷要安裝升級的位置。 AppSearch 動作也可以用來將屬性設為登錄或 .ini 檔案專案的現有值。

## <a name="sequence-restrictions"></a>順序限制

AppSearch 應該撰寫在 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。 如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止在 InstallExecuteSequence 序列中執行 AppSearch 動作。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述      |
|-------|---------------------------------|
| \[1\] | 保存檔案位置的屬性。 |
| \[2\] | 檔案簽章。                 |



 

## <a name="remarks"></a>備註

AppSearch 動作需要簽 [章資料表出現](signature-table.md) 在安裝套件中。 簽章會列在簽章資料表中。 不在簽章資料表中的簽章代表目錄，而動作則會將屬性設定為該簽章的目錄路徑。

AppSearch 動作會先使用 [CompLocator](complocator-table.md) 資料表、 [RegLocator](reglocator-table.md) 資料表、 [IniLocator](inilocator-table.md) 資料表，最後是 [DrLocator](drlocator-table.md) 資料表來搜尋檔案簽章。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[AppSearch](appsearch-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 




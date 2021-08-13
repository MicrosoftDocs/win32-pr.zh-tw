---
description: DuplicateFiles 動作會複製 InstallFiles 動作所安裝的檔案。 重複的檔案可以複製到具有不同名稱的相同目錄，或複製到具有原始名稱的不同目錄。
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: DuplicateFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7969440aed4361ad264baa0d30a9c1d16f0ca673c72a2a7c3c1326e5d393ffc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637710"
---
# <a name="duplicatefiles-action"></a>DuplicateFiles 動作

DuplicateFiles 動作會複製 [InstallFiles](installfiles-action.md) 動作所安裝的檔案。 重複的檔案可以複製到具有不同名稱的相同目錄，或複製到具有原始名稱的不同目錄。

## <a name="sequence-restrictions"></a>順序限制

DuplicateFiles 動作必須晚于 [InstallFiles 動作](installfiles-action.md)。 DuplicateFiles 動作也必須在 [PatchFiles 動作](patchfiles-action.md) 之後，以防止複製未修補的檔案版本。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                       |
|-------|--------------------------------------------------|
| \[1\] | 重複檔案的識別碼。                   |
| \[6\] | 重複檔案的大小。                         |
| \[9\] | 保存重複檔案之目錄的識別碼。 |



 

## <a name="remarks"></a>備註

只有當連結到該專案的元件是在本機安裝時，DuplicateFiles 動作才會處理 [DuplicateFile 資料表](duplicatefile-table.md) 專案。 如需詳細資訊，請參閱 [元件表格](component-table.md)。

DestFolder 欄位中的字串是屬性名稱，其值應解析為完整路徑。 這個屬性可以是 [目錄](directory-table.md) 資料表中的任何目錄專案、任何預先定義的資料夾屬性 ([**CommonFilesFolder**](commonfilesfolder.md)（例如) ），或是 [AppSearch](appsearch-table.md) 資料表中任何專案所設定的屬性。 如果 **DestFolder** 屬性未評估為有效的路徑，則 DuplicateFiles 動作不會對該專案執行任何動作。

如果 DuplicateFile 資料表的 DestName 資料行中之目的地檔案的名稱保留空白，則目的地檔案名將會與原始檔案名稱相同。

DuplicateFiles 動作所安裝的檔案會在適當時由 [RemoveDuplicateFiles](removeduplicatefiles-action.md) 動作移除。

 

 




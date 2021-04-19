---
description: RemoveFiles 動作會移除 InstallFiles 動作先前安裝的檔案。
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: RemoveFiles 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971491"
---
# <a name="removefiles-action"></a>RemoveFiles 動作

RemoveFiles 動作會移除 [InstallFiles](installfiles-action.md) 動作先前安裝的檔案。 這些檔案中的每一個都是由 [元件](component-table.md) 表格中專案的連結所管制。 只有當元件安裝在本機時，具有元件的檔案才會解析為 *msiInstallStateAbsent* 狀態或 *msiInstallStateLocal* 狀態。

## <a name="sequence-restrictions"></a>順序限制

呼叫 RemoveFiles 之前，必須先呼叫 [InstallValidate](installvalidate-action.md) 動作。 如果使用 [InstallFiles](installfiles-action.md) 動作，它必須出現在 RemoveFiles 之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述                    |
|-------|-----------------------------------------------|
| \[1\] | 已移除之檔案的識別碼。                   |
| \[9\] | 保存已移除檔案之目錄的識別碼。 |



 

## <a name="remarks"></a>備註

如果沒有其他要移除的檔案，則可以從安裝程式資料庫省略 [RemoveFile](removefile-table.md) 資料表。

RemoveFiles 動作也可以移除 InstallFiles 動作未安裝的作者指定檔案。 這些檔案會在 [RemoveFile](removefile-table.md) 資料表中指定。 這些檔案中的每一個都是由 [元件](component-table.md) 表格中專案的連結所管制。 如果檔案存在於指定的目錄中，這些檔案的元件會解析為任何作用中的動作 (狀態，而不是在 Off 或 Null 狀態中，則會移除) 。 第一次安裝連結元件時，會嘗試移除 RemoveFile 資料表中指定的檔案，在重新安裝期間，以及在移除連結元件時，也會發生此情況。

RemoveFiles 動作也可以移除資料夾。 如果 RemoveFile 資料表的 FileName 資料行中的值為 null，則會移除空的資料夾。

移除先前安裝的檔案時，RemoveFiles 動作會查詢與 [InstallFiles](installfiles-action.md) 動作所查詢之相同資料表中的相同欄位，但 RemoveFiles 動作未使用 [媒體資料表](media-table.md) 的例外。

您可以在 RemoveFile 資料表的 FileName 資料行中，以當地語系化的文字指定目的檔案名。

 

 




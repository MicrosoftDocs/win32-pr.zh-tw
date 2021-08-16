---
description: 必須撰寫多語言合併模組、語言轉換和封包檔，使檔案的順序符合檔案資料表中指定的順序。
ms.assetid: c6ddf5fc-a7c5-49c1-899b-ff9fdff9c028
title: 排序多個語言合併模組 CAB 中的檔案順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e0d7d5efc3c4599f7a3f0eecce2101d1a7db034be6e0f80eda30245a95204d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942805"
---
# <a name="ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module"></a>排序多個語言合併模組 CAB 中的檔案順序

多語言合併模組、語言轉換和封包檔必須撰寫成使 .cab 中的檔案順序符合 [File 資料表](file-table.md)中指定之檔案的安裝順序，即使是在語言轉換的應用程式之後也一樣。 如果模組和 .cab 中的順序不相符，就無法使用合併模組。

指派給模組中的每個檔案，這是與語言無關的唯一序號，然後一律使用該檔案的序號。 建立封包檔和撰寫語言轉換時，請使用相同的順序。

因為安裝程式只會安裝檔案 [資料表](file-table.md)中所列的檔案，所以在封包、檔案 [資料表](file-table.md)和語言轉換中使用全域檔案順序，可讓合併工具略過儲存在封包中未列在檔案 [資料表](file-table.md)中的任何其他檔案。 其他檔案可能會存在於封包中，但不能列在檔案 [資料表](file-table.md)中。 例如，安裝 Code.dll、英文 .dat、德文和法文的模組可以使用下列全域檔案順序順序。



| 檔案        | 順序 |
|-------------|----------|
| Code.Dll    | 1        |
| 英文版 .Dat | 2        |
| 德文 .Dat  | 3        |
| 法文  | 4        |



 

然後可以撰寫語言轉換來修改模組的檔案 [表格](file-table.md) ，以取得英文、德文或法文。

英文) 的[檔資料表](file-table.md) (部分



| 檔案        | 順序 |
|-------------|----------|
| Code.Dll    | 1        |
| 英文版 .Dat | 2        |



 

德文) 的[檔資料表](file-table.md) (部分



| 檔案       | 順序 |
|------------|----------|
| Code.Dll   | 1        |
| 德文 .Dat | 3        |



 

[File 資料表](file-table.md) (部分的法文) 



| 檔案       | 順序 |
|------------|----------|
| Code.Dll   | 1        |
| 法文 | 4        |



 

如需詳細資訊，請參閱 [撰寫多個語言合併模組的語言轉換](authoring-a-language-transform-for-a-multiple-language-merge-module.md) 和 [撰寫合併模組檔案資料表](authoring-merge-module-file-tables.md)。

 

 




---
description: 每個合併模組都必須要有一個檔案資料表，而且每個檔案的記錄都應該由合併模組傳遞至目標安裝套件。
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: 撰寫合併模組檔案資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026642"
---
# <a name="authoring-merge-module-file-tables"></a>撰寫合併模組檔案資料表

每個合併模組都必須要有一個檔案 [資料表](file-table.md) ，而且每個檔案的記錄都應該由合併模組傳遞至目標安裝套件。 合併模組合併為 .msi 檔案時，合併模組檔案資料表中的每個檔案都會儲存在 .msm 檔案的封 [*包*](c-gly.md) 檔中。 合併模組中的封包名稱一律如下： MergeModule.CABinet。

如需詳細資訊，請參閱 [產生 MergeModule.CABinet 封包](generating-mergemodule-cabinet-cabinet-files.md)檔。

-   因為合併模組的檔案一律儲存在封包檔中，所以不需要在檔案 [資料表](file-table.md)的 [屬性] 資料行中設定 **msidbFileAttributesNoncompressed** 或 **msidbFileAttributesCompressed** 位旗標。
-   MergeModule.CABinet 中的檔案名必須符合合併模組的檔案 [資料表](file-table.md)中的主鍵。

    File 資料行是檔案 [資料表](file-table.md) 的主鍵，而此欄位中的專案必須遵循在 [合併模組資料庫中命名主鍵](naming-primary-keys-in-merge-module-databases.md)所述的慣例。

-   檔案序號是在 [File 資料表](file-table.md)的 sequence 資料行中指定。

    檔案必須以儲存在 MergeModule.CABinet 中的相同順序，列在合併模組的檔案 [資料表](file-table.md) 中。 檔案的序號不需要連續，但它們的順序必須與儲存在封包內的檔案相同。 例如，儲存在封包中的第一個、第二個和第三個檔案的序號可能是100、200和300。

-   安裝程式會略過未列在檔案 [資料表](file-table.md)中 MergeModule.CABinet 包含的額外檔案。

    一個封包檔可以包含使用轉換支援多種語言的合併模組所需的所有檔案。 所有語言檔案都可在封包中提供唯一的序號，然後當特定語言需要時，轉換可以在檔案 [資料表](file-table.md) 中新增或移除檔案。 如需詳細資訊，請參閱 [撰寫多個語言合併模組](authoring-multiple-language-merge-modules.md)。

如需詳細資訊，請參閱檔案 [資料表](file-table.md)。

 

 




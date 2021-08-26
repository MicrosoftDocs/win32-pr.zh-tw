---
description: 您可以使用此指導方針來撰寫包含32767以上檔案的 Windows Installer 套件。
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: 撰寫大型封裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d55f7933fe600bd6c0db0705328f18d7eae2f55e3463e3ea03be8118229eca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996878"
---
# <a name="authoring-a-large-package"></a>撰寫大型封裝

您可以使用此指導方針來撰寫包含32767以上檔案的 Windows Installer 套件。

如果您的 Windows Installer 封裝包含32767個以上的檔案，您必須變更資料庫的架構，以增加下列資料行的限制：

-   [File 資料表](file-table.md)的 Sequence 資料行。
-   [媒體資料表](media-table.md)的 LastSequence 資料行。
-   [Patch 資料表](patch-table.md)的 Sequence 資料行。

如需詳細資訊，請參閱資料 [行定義格式](column-definition-format.md)。

**若要增加資料庫資料行的限制**

1.  將資料表匯出至 idt 檔案。 如需詳細資訊，請參閱 [Msidb.exe](msidb-exe.md)、 [匯出](export-files.md)檔案，以及匯 [入和匯出](importing-and-exporting.md)。
2.  編輯 idt 檔案，將資料行類型從 i2 變更為 i4，或從 I2 變更為 I4。
3.  將[ \_ 驗證](-validation-table.md)資料表匯出至 idt 檔案。
4.  編輯 idt 檔案，以變更 [ [ \_ 驗證](-validation-table.md)] 資料表的 [int32.maxvalue] 資料行中的值，以容納增加的資料行寬度。
5.  將 idt 檔案匯入回資料庫。

請注意，無法在具有不同資料行類型的兩個封裝之間建立轉換和修補程式。

 

 




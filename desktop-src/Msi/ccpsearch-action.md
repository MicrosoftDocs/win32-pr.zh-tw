---
description: CCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。
ms.assetid: 0aa7bf8b-de76-464d-8e7b-3aa4f609fe19
title: CCPSearch 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 201af22dd557541825dcf2c47f06e7cf67cd8785fa85e0b78a28c25a570ffc89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145691"
---
# <a name="ccpsearch-action"></a>CCPSearch 動作

CCPSearch 動作會在執行升級安裝之前，使用檔案簽章來驗證是否已在系統上安裝合格產品。

## <a name="sequence-restrictions"></a>順序限制

CCPSearch 動作應該撰寫到 [InstallUISequence 資料表](installuisequence-table.md) 和 [InstallExecuteSequence 資料表](installexecutesequence-table.md)中。 如果動作已在 InstallUISequence 序列中執行，則安裝程式會防止在 InstallExecuteSequence 序列中執行 CCPSearch 動作。 CCPSearch 動作必須位於 [RMCCPSearch](rmccpsearch-action.md) 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息

沒有任何 ActionData 訊息。

## <a name="remarks"></a>備註

CCPSearch 動作會使用下列資料表依序搜尋系統上 CCPSearch 資料表中所列的檔案簽章： Signature、CompLocator、RegLocator、IniLocator 和 DrLocator。

如果有任何簽章確定存在，則 **CCP \_ Success** 屬性會設定為1，而 CCPSearch 動作會終止。

簽章資料表缺少簽章代表目錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[CCPSearch](ccpsearch-table.md)
</dt> <dt>

[簽名](signature-table.md)
</dt> <dt>

[CompLocator](complocator-table.md)
</dt> <dt>

[RegLocator](reglocator-table.md)
</dt> <dt>

[IniLocator](inilocator-table.md)
</dt> <dt>

[DrLocator](drlocator-table.md)
</dt> </dl>

 

 




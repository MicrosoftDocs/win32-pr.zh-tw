---
description: 如果元件設定為在本機安裝或從來源執行，則 RemoveIniValues 動作會移除在 RemoveIniFile 資料表中指定要移除的 .ini 檔案資訊。
ms.assetid: a30793c8-4154-4990-a42a-d022e69f960a
title: RemoveIniValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095985165bf6d9629aa0cae67a5b3f7975d817151ac4b04de40a08d5c2bab4d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626387"
---
# <a name="removeinivalues-action"></a>RemoveIniValues 動作

如果元件設定為在本機安裝或從來源執行，則 RemoveIniValues 動作會移除在 [RemoveIniFile 資料表](removeinifile-table.md) 中指定要移除的 .ini 檔案資訊。 RemoveIniValues 動作會移除與 [IniFile 資料表](inifile-table.md)中的元件相關聯 .ini 檔案資訊。 如果資訊是由 [WriteIniValues 動作](writeinivalues-action.md) 寫入，而元件已排程要卸載，此動作也會移除 .ini 的檔案資訊。

## <a name="sequence-restrictions"></a>順序限制

[InstallValidate](installvalidate-action.md)動作必須在 RemoveIniValues 動作之前呼叫。 如果序列中使用 [WriteIniValues](writeinivalues-action.md) 動作，它必須出現在 RemoveIniValues 之後。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述    |
|-------|-------------------------------|
| \[1\] | .ini 檔案的識別碼。      |
| \[2\] | .ini 的檔案金鑰區段。     |
| \[3\] | 從 .ini 檔案中移除的專案。  |
| \[4\] | 從 .ini 檔案中移除的值。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[RemoveIniFile 資料表](removeinifile-table.md)
</dt> <dt>

[IniFile 資料表](inifile-table.md)
</dt> <dt>

[WriteIniValues 動作](writeinivalues-action.md)
</dt> <dt>

[InstallValidate](installvalidate-action.md)
</dt> </dl>

 

 




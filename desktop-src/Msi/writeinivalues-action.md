---
description: WriteIniValues 動作會將應用程式需要寫入的 .ini 檔案資訊寫入其 .ini 檔。
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: WriteIniValues 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942096"
---
# <a name="writeinivalues-action"></a>WriteIniValues 動作

WriteIniValues 動作會將應用程式需要寫入的 .ini 檔案資訊寫入其 .ini 檔。 這項資訊的寫入是由 [元件資料表](component-table.md)所管制。 如果對應的元件已設定為要安裝在本機或從來源執行，則會寫入 .ini 值。

## <a name="sequence-restrictions"></a>順序限制

InstallValidate 動作必須位於 WriteIniValues 動作之前。 如果序列中有 [RemoveIniValues 動作](removeinivalues-action.md) ，則必須在 WriteIniValues 動作之前。

## <a name="actiondata-messages"></a>ActionData 訊息



| 欄位 | 動作資料的描述              |
|-------|-----------------------------------------|
| \[1\] | .ini 檔案的識別碼。                |
| \[2\] | 下一節中 .ini 的檔案索引鍵。 |
| \[3\] | 從 .ini 檔案中移除的專案。            |
| \[4\] | 從 .ini 檔案中移除的值。           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[IniFile 資料表](inifile-table.md)
</dt> </dl>

 

 




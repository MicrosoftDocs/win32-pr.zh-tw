---
description: RemoveODBC 動作會移除在安裝期間列出要移除的資料來源、轉譯程式和驅動程式。
ms.assetid: 548984fd-e4f7-4db8-a625-87b4a0a4bdb2
title: RemoveODBC 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6619bc5b8a18cff2ee33dbe45261764c682953bad75a17cb9d6e93cbe487147b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580428"
---
# <a name="removeodbc-action"></a>RemoveODBC 動作

RemoveODBC 動作會移除在安裝期間列出要移除的資料來源、轉譯程式和驅動程式。 此動作會查詢已排程要移除的每個資料來源、翻譯工具或驅動程式的 [ODBCDataSource 資料表](odbcdatasource-table.md)、 [ODBCTranslator 資料表](odbctranslator-table.md)和 [ODBCDriver 資料表](odbcdriver-table.md) 。

## <a name="sequence-restrictions"></a>順序限制

沒有任何順序限制。

## <a name="actiondata-messages"></a>ActionData 訊息

每個安裝的驅動程式。



| 欄位 | 動作資料的描述               |
|-------|------------------------------------------|
| \[1\] | 驅動程式描述。 ODBC 驅動程式金鑰。 |
| \[2\] | ComponentId                              |



 

針對每個已安裝的翻譯工具。



| 欄位 | 動作資料的描述               |
|-------|------------------------------------------|
| \[1\] | 驅動程式描述。 ODBC 驅動程式金鑰。 |
| \[2\] | ComponentId                              |



 

針對每個已安裝的資料來源。



| 欄位 | 動作資料的描述                              |
|-------|---------------------------------------------------------|
| \[1\] | 驅動程式描述。 ODBC 驅動程式金鑰。                |
| \[2\] | ComponentId                                             |
| \[3\] | 註冊： SQL \_ 移除 \_ DSN 或 SQL \_ 移除 \_ SYS \_ DSN |



 

## <a name="remarks"></a>備註

如果 ODBC 使用計數和檔案使用計數都變成零，則會移除該檔案。 註冊相依于 ODBC 使用計數，而檔案移除是以共用 Dll 金鑰參考計數為基礎。

 

 




---
description: InstallODBC 動作會在 ODBCDriver 資料表、ODBCTranslator 資料表和 ODBCDataSource 資料表中安裝驅動程式、轉譯程式和資料來源。
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: InstallODBC 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a371aed67ec412c46946d7df7fd4775f0a0d4e20d91cbb60d69f894371f203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142222"
---
# <a name="installodbc-action"></a>InstallODBC 動作

InstallODBC 動作會在 [ODBCDriver 資料表](odbcdriver-table.md)、 [ODBCTranslator 資料表](odbctranslator-table.md)和 [ODBCDataSource 資料表](odbcdatasource-table.md)中安裝驅動程式、轉譯程式和資料來源。 如果驅動程式或轉譯器已存在，InstallODBC 動作會讓安裝所需的 SQL 呼叫。

## <a name="sequence-restrictions"></a>順序限制

InstallODBC 動作不會複製或移除檔案，而且必須在複製或移除檔案的動作之後。

## <a name="actiondata-messages"></a>ActionData 訊息

下表指出每個已安裝驅動程式的 ActionData 訊息。



| 欄位       | 描述                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | 驅動程式描述。 ODBC 驅動程式金鑰。                                 |
| \[2\]       | ComponentId.                                                             |
| \[3\]       | 資料夾。                                                                  |
| \[4、5、.。。\] | 來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。 |



 

下錶針對每個已安裝的翻譯工具，識別 ActionData 的訊息。



| 欄位       | 描述                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | 驅動程式描述。 ODBC 驅動程式金鑰。                                 |
| \[2\]       | ComponentId.                                                             |
| \[3\]       | 資料夾。                                                                  |
| \[4、5、.。。\] | 來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。 |



 

下表指出每個已安裝資料來源的 ActionData 訊息。



| 欄位       | 描述                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | 驅動程式描述。 ODBC 驅動程式金鑰。                                 |
| \[2\]       | ComponentId.                                                             |
| \[3\]       | 註冊： ODBC \_ 新增 \_ DSN 或 odbc \_ 新增 \_ SYS \_ DSN。                     |
| \[4、5、.。。\] | 來自 [ODBCAttribute](odbcattribute-table.md)的屬性和值配對。 |



 

## <a name="remarks"></a>備註

ODBC 驅動程式管理員必須在 Microsoft Installer 封裝中撰寫，且必須包含名為 ODBCDriverManager 的元件。 如有必要，則會安裝管理員。

若要重新命名元件，請將名為 ODBCDriverManager 的屬性設定為元件的新名稱。 如果要安裝64位 ODBC 驅動程式管理員，則攜帶該驅動程式的元件應該命名為 ODBCDriverManager64。

-   InstallODBC 動作會查詢 [ODBCDataSource 資料表](odbcdatasource-table.md) 和 [ODBCSourceAttribute 資料表](odbcsourceattribute-table.md) ，找出要安裝的每個資料來源，以及資料來源的屬性。
-   InstallODBC 動作會針對已選取要安裝的每個驅動程式和翻譯工具，查詢 [ODBCDriver 資料表](odbcdriver-table.md) 和 [ODBCTranslator 資料表](odbctranslator-table.md) 。
-   InstallODBC 動作會查詢 [ODBCAttribute 資料表](odbcattribute-table.md) ，以取得驅動程式和轉譯程式的屬性。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式範例](windows-installer-examples.md)
</dt> </dl>

 

 




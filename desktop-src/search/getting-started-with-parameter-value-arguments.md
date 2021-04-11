---
description: Search-ms？應用程式協定是查詢 Windows Search 索引的慣例。
ms.assetid: e8b18018-c712-4007-bb0a-af90a75780d6
title: 具有 Parameter-Value 引數的開始使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd6e3df2ddb1d0c3f62293d3d3dc2615e855f93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191199"
---
# <a name="getting-started-with-parameter-value-arguments"></a>具有 Parameter-Value 引數的開始使用

**搜尋毫秒**？[應用程式協定](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767916(v=vs.85))是查詢 Windows Search 索引的慣例。 此通訊協定可讓應用程式（例如 Windows 檔案總管）查詢具有參數值引數的索引，包括屬性引數、先前儲存的搜尋、先進的查詢語法 (AQS) 、自然查詢語法 (NQS) ，以及 (索引子和查詢本身的語言程式碼識別碼) Lcid。

本主題的組織方式如下：

- [關於 Parameter-Value 引數](#about-parameter-value-arguments)
- [範例](#examples)
- [相關主題](#related-topics)

## <a name="about-parameter-value-arguments"></a>關於 Parameter-Value 引數

搜尋 ms 通訊協定會使用下列標準的 URL 編碼語法：

```
search-ms:parameter=value[&parameter=value]&
```

語法一開始會識別通訊協定本身 (搜尋-ms： ) 。 參數/值組是傳遞給搜尋引擎的引數，如下表所述。

| 參數                                                    | 值                                                         | 描述                                                                                                                                                                                                                                                                | 版本                  |
|--------------------------------------------------------------|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| 查詢                                                        | URL 編碼的文字                                              | 使用者輸入的查詢文字。                                                                                                                                                                                                                                        | Windows XP 及更新版本    |
| [inputlocale](-search-3x-wds-qryidx-localeidentifiers.md)   | 任何有效的 LCID                                                | 識別查詢之輸入語言的 LCID。                                                                                                                                                                                                                 | Windows XP 及更新版本    |
| [keywordlocale](-search-3x-wds-qryidx-localeidentifiers.md) | 任何有效的 LCID                                                | 識別索引子之國際版本語言的 LCID。 預設值為 1033 (en-us) 。                                                                                                                                                            | Windows XP 及更新版本    |
| [粉](-search-3x-wds-qryidx-crumb.md)                     | AQS 語句                                                 | 此引數會限制要搜尋的範圍。 在 Windows Vista 和更新版本中，搜尋 ms 支援完整 AQS 以及引數的特殊實作為 `location` 。 在 Windows XP 中，search-ms 也支援完整 AQS，除了與的特殊執行 `kind` 之外 `store` 。 | Windows XP 及更新版本    |
| [語法](-search-3x-wds-qryidx-syntaxargument.md)           | NQS，AQS (不區分大小寫)                                  | 用來搜尋索引的查詢語法：自然查詢語法或 Advanced Query 語法 (AQS) 。 AQS 是預設值，而且一律會假設為已剖析且受支援。                                                                                                    | Windows Vista 和更新版本 |
| [stackedby](-search-3x-wds-qryidx-stackedby.md)             | 屬性系統中的任何有效屬性                   | 屬性，指定要用來堆疊結果的資料行。                                                                                                                                                                                                                  | Windows Vista 和更新版本 |
| [subquery](-search-3x-wds-qryidx-subquery.md)               | 已儲存的搜尋檔案 (的完整指定路徑 \* 。搜尋-ms)  | 子查詢的結果會當做查詢的來源使用。 也就是說，會針對子查詢的結果搜尋查詢詞彙。                                                                                                                           | Windows Vista 和更新版本 |
| displayname                                                  | URL 編碼的字串                                            | 目前搜尋的名稱。                                                                                                                                                                                                                                            | Windows Vista 和更新版本 |


如需相關資訊，請參閱 [向 URL 通訊協定註冊應用程式](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))。

## <a name="examples"></a>範例

```
search-ms:query=microsoft&
search-ms:query=vacation&subquery=mydepartment.search-ms&
search-ms:query=seattle&crumb=kind:pics&
search-ms:query=seattle&crumb=folder:C:\MyFolder&
```

## <a name="related-topics"></a>相關主題

[地區設定識別碼引數](-search-3x-wds-qryidx-localeidentifiers.md)

[連結引數](-search-3x-wds-qryidx-crumb.md)

[語法引數](-search-3x-wds-qryidx-syntaxargument.md)

[STACKEDBY 引數](-search-3x-wds-qryidx-stackedby.md)

[子查詢引數](-search-3x-wds-qryidx-subquery.md)

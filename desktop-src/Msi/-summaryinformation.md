---
description: '\_SummaryInformation 資料表是與摘要資訊資料流程搭配使用的特殊資料表。 您可以藉由匯出或匯入名為 SummaryInformation. idt 的文字保存檔案，來取得或設定 Windows Installer 資料庫的摘要資訊串流 \_ 。'
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3824ceb9b3ad12338d84dfeea016a3c7e4404c274543cc691dc6ea0fb121bd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805734"
---
# <a name="_summaryinformation"></a>\_SummaryInformation

\_SummaryInformation 資料表是與[摘要資訊資料流程](summary-information-stream.md)搭配使用的特殊資料表。 您可以藉由匯出或匯入名為 SummaryInformation. idt 的[文字保存](text-archive-files.md)盤案，來取得或設定 Windows Installer 資料庫的摘要資訊串流 \_ 。

匯出之 SummaryInformation 資料表的 idt 檔案 \_ 具有下列格式。

-   第一個資料列包含以定位字元分隔的資料表資料行名稱： PropertyId 和 Value。 如需屬性及其識別碼的清單，請參閱 [摘要資訊資料流程屬性集](summary-information-stream-property-set.md) 主題 (PID) 。
-   第二個數據列包含以定位字元分隔的資料行定義。 您可以用 idt 封存檔案 [格式](archive-file-format.md)的相同方式來指定資料行定義。 PropertyId 資料行可以是不可為 null 的短整數。 值資料行可以是不可為 null 的可當地語系化字串（長度為255個字元）。
-   第三個數據列是資料表名稱，而主鍵資料行名稱是以 tab 分隔： \_ SummaryInformation 和 PropertyId。
-   檔案中的其餘資料列代表 PID 和相關聯的值（以 tab 分隔）。 SummaryInformation 中的日期和時間 \_ 格式如下： YYYY/MM/DD hh：： MM：： ss。 例如，1999/03/22 15:25:45。

下列是 idt 格式之資料庫的 [摘要資訊資料流程](summary-information-stream.md) 範例。

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

當您使用 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)或 [**Database**](database-object.md)物件的 [import](database-import.md)方法，將名為 SummaryInformation 的文字保存資料表匯入到 \_ 安裝程式資料庫時，您會在資料庫中寫入 "05SummaryInformation" 資料流程。

 

 




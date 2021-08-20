---
title: Windows Server 2003 SP1 中的錯誤記錄
description: Windows Server 2003 SP1 中的錯誤記錄
ms.assetid: 8c7fcc66-5446-4e25-8e6d-1a9260c55e36
keywords:
- 在 Windows Server 2003 Service Pack 1 (SP1) 中記錄錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d5a84dfba8ecb9a78ed38d3ad112f0820e6b578bce77e189e5047a25f458b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014806"
---
# <a name="error-logging-in-windows-server-2003-sp1"></a>Windows Server 2003 SP1 中的錯誤記錄

## <a name="addition-of-w3c-style-headers"></a>加入 W3C 樣式標頭

從 Windows Server 2003 Service Pack 1 (SP1) 開始，HTTP 伺服器 API 錯誤記錄檔包含的 W3C 樣式標頭，可讓您使用標準記錄剖析器剖析記錄檔。 下方顯示的範本會列出可記錄在 HTTP 錯誤記錄檔中的所有欄位。

``` syntax
#Software: <Name of the HTTP Server>
#Version: 1.0 <Log format version>
#Date: <Log file creation date and time>
#Fields: <date time s-computername c-ip c-port s-ip s-port cs-version
         cs-method cs-uri cs(User-Agent) cs(Cookie) cs(referrer) 
         cs-host sc-status sc-bytes cs-bytes time-taken s-siteid  
         s- reason s-queuename <header names of fields logged>

```

## <a name="logging-additional-fields"></a>記錄其他欄位

HTTP 錯誤記錄檔已擴充為包含九個以上的欄位，可記錄有關發生之失敗的資料。 新的錯誤欄位如下所示：

-   伺服器電腦名稱稱 \[ S-COMPUTERNAME\]
-   使用者代理程式 \[ CS (使用者 \_ 代理程式) \]
-   Cookie \[ CS (cookie) \]
-   訪客 (訪客) 的推薦者 \[\]
-   主機名稱 \[ CS-主機\]
-   伺服器 SC 所接收的位元組 \[ -位元組\]
-   伺服器 CS 接收和處理的位元組 \[ -位元組\]
-   處理要求時間所花費的時間 \[\]
-   Queue-Name (保留給 IIS) \[ S-QUEUENAME\]

## <a name="selecting-fileds-to-log-in-the-http-error-log-file"></a>選取 Fileds 以登入 HTTP 錯誤記錄檔

已新增 **ErrorLoggingFields** 登錄機碼，以控制登入 HTTP 錯誤記錄檔中的欄位。 此登錄值位於下列位置的 HTTP \\ 參數機碼：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
      Services
         HTTP
            Parameters
```

**ErrorLoggingFields** 登錄值是 DWORD 值，其中包含每個可記錄欄位的位值。 若要啟用特定欄位的記錄功能，請將其對應的位值設定為1，然後重新開機 HTTP 服務。 若要停用記錄，請將位值設定為0。 若要設定多個欄位，請使用個別值的位 OR。 例如，若要開啟 Cookie 和查閱者記錄欄位，此值應為 0x00020000 \| 0x00040000 = 0x00060000。 如果 **ErrorLoggingFields** 登錄機碼不存在，則會記錄預設欄位。 要記錄預設欄位的 **ErrorLoggingFields** 值是0x7c884c7。 若要針對下表所顯示的所有欄位啟用記錄，請將值設定為0x7dff4e7。

錯誤記錄欄位會列在下表中：



| 記錄欄位            | 預設記錄 | 位元值  |
|----------------------|-------------------|------------|
| Date                 | 是               | 0x00000001 |
| 時間                 | Yes               | 0x00000002 |
| 伺服器電腦名稱稱 | No                | 0x00000020 |
| 用戶端 IP 位址    | Yes               | 0x00000004 |
| 用戶端埠          | Yes               | 0x00400000 |
| 伺服器 IP 位址    | Yes               | 0x00000040 |
| 伺服器通訊埠          | Yes               | 0x00008000 |
| 通訊協定版本     | Yes               | 0x00080000 |
| 方法               | Yes               | 0x00000080 |
| URI                  | Yes               | 0x00800000 |
| 使用者代理程式           | No                | 0x00010000 |
| Cookie               | No                | 0x00020000 |
| 引薦             | No                | 0x00040000 |
| Host                 | No                | 0x00100000 |
| 通訊協定狀態      | Yes               | 0x00000400 |
| SC-Bytes             | No                | 0x00001000 |
| CS-Bytes             | No                | 0x00002000 |
| 花費的時間           | No                | 0x00004000 |
| SiteId               | Yes               | 0x01000000 |
| 原因片語        | Yes               | 0x02000000 |
| 佇列名稱           | No                | 0x04000000 |
| 串流識別碼            | No                | 0x???????? |



 

## <a name="time-and-date-rollover"></a>日期和時間變換

根據預設，當目前的記錄檔達到指定的大小時，會建立新的 HTTP 錯誤記錄檔 (稱為檔案變換) 。 從 Windows Server 2003 （含 SP1）開始，可以根據日期和時間建立新的錯誤記錄檔。 時間和日期變換是由兩個新的登錄值所控制： **ErrorLoggingRolloverType** 和 **ErrorLoggingLocaltimeRollover**。 若要啟用時間和日期變換，必須將這些登錄值新增至登錄。 當這些金鑰新增至登錄時，必須重新開機 Http 服務。 記錄檔變換登錄機碼會在下列機碼底下建立：

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            HTTP
               Parameters
```

**ErrorLoggingRolloverType** 登錄機碼會指出所需的變換類型，而且預設會設定為以大小為基礎的變換。 變換也可以設定為每日、每週、每月或每小時進行。 當檔案變換以時間為基礎時， **ErrorLoggingLocaltimeRollover** 值為0表示變換時間以 GMT 表示，而值為1則表示變換時間以當地時程表示。 **ErrorLoggingRolloverType** 索引鍵可採用從0到4的值，如下表所示。



| 變換類型值 | 描述                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 0                   | 以大小為基礎的變換。 當檔案到達 **ErrorLogFileTruncateSize** 登錄機碼中定義的大小時，就會變換記錄檔。 |
| 1                   | 記錄檔變換每日發生一次。                                                                                                         |
| 2                   | 記錄檔變換每週進行一次。                                                                                                        |
| 3                   | 每月都會進行記錄檔變換。                                                                                                       |
| 4                   | 記錄檔變換每小時進行一次。                                                                                                        |



 

儲存錯誤記錄檔之檔案的命名慣例，與大小、日期和以時間為基礎的變換不同。 下表列出 Http 記錄檔的命名慣例。



| Tollover 類型 | 記錄檔名稱  | 描述                                                                                                                         |
|---------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 大小          | HTTPERRn .LOG   | 當記錄檔到達特定大小時，就會回收記錄檔。 n 是檔案編號，而且會在記錄檔變換時遞增。 |
| 每日         | htYYMMDD .log   | 記錄檔每天都會回收。                                                                                                     |
| 每週        | htYYMMww .log   | 每週都會回收記錄檔，其中 ww 是當月的第幾周。                                                                 |
| 每月       | htYYMM .log     | 每個月都會回收記錄檔。                                                                                               |
| 每小時        | htYYMMDDhh .log | 記錄檔會每小時回收一次，其中 hh 是以0-24 小時標記法表示的一天中的小時。                                   |



 

 

 





---
title: 使用 ETW 追蹤的案例2剖析器範例
description: 若要產生 HTTP 伺服器 API 元件的 ETW 追蹤報告，請執行如 \ 0034; 中所示的步驟。產生 ETW 追蹤報告 \ 0034;使用 ETW 追蹤和 Netsh 命令的案例 1 HTTP Timeout 範例一節，但重現此案例特定的錯誤。
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ec0448801334dddb1f964473a925ff18183af992157a55c0d90d7b259f1159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996196"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>案例2：使用 ETW 追蹤的剖析器範例

若要產生 HTTP 伺服器 API 元件的 ETW 追蹤報告，請執行 [下列步驟：使用 ETW 追蹤和 Netsh 命令](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md)的「產生 Etw 追蹤報表」一節中所示的步驟，但重現此案例特定的錯誤。 在此範例中，從用戶端電腦存取 web 應用程式，導致用戶端上顯示「400不正確的要求」訊息。 這些步驟會在伺服器上執行，因為它會裝載 web 應用程式。

## <a name="viewing-the-trace-and-diagnosing"></a>查看追蹤和診斷

您可以在 Excel 或支援 csv 格式的任何工具中，查看所產生的追蹤 csv 檔案。 下表2顯示範例追蹤檔 (httptrace.csv) 的摘錄。 在追蹤報表中，[層級] 資料行會顯示值為 "2" 的專案，代表錯誤。 如先前所述，HTTP 伺服器 API 元件會遵循 [LevelType 複雜型別複雜型](../wes/eventmanifestschema-leveltype-complextype.md)別一文中定義的 ETW 層級。

ETW 層級包括：1關鍵;2錯誤;3警告;4資訊;5詳細資訊。

發生此錯誤時，事件種類 (類型資料行) 報告 "ParseRequestFailed"。 在 ParseRequestFailed 事件的後續資料行中，我們會看到 "InvalidHost" 專案。 此專案表示 HTTP 要求中識別的主機不正確（根據 HTTP 通訊協定）。 請注意，資料表中包含 "InvalidHost" 專案的資料行不包含在資料表中，以求簡潔，並避免 excerpting 非連續的資料行。

若要修正此剖析問題，應該更正 web 用戶端，以符合 HTTP RFC 的規範。 

| 事件名稱                    | 類型               | 事件識別碼 | 版本 | 管道 | 層級 |
|-------------------------------|--------------------|----------|---------|---------|-------|
| EventTrace                    | 標頭             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

表2：剖析問題的範例追蹤報表摘錄

 

 
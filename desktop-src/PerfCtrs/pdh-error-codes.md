---
description: 所有效能資料協助程式 (PDH) 函數都會傳回類型為 PDH 的值 \_ 。
ms.assetid: ea67d798-81db-44ad-b0fb-24e0c3be7388
title: 效能資料協助程式錯誤碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0417801b4f7a23e48a74201aa48193987a0edee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985653"
---
# <a name="performance-data-helper-error-codes"></a>效能資料協助程式錯誤碼

所有效能資料協助程式 (PDH) 函數都會傳回類型為 **PDH \_** 的值。 如果函式成功，則傳回值為 `ERROR_SUCCESS` 。 否則，函數會傳回 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 PDH 錯誤碼。 若要在您的應用程式中取得錯誤的描述文字，請使用 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式，如下列範例所示。

```C++
#include <windows.h>
#include <stdio.h>
#include <pdhmsg.h>

void main(void)
{
    HANDLE hPdhLibrary = NULL;
    LPWSTR pMessage = NULL;
    DWORD_PTR pArgs[] = { (DWORD_PTR)L"<collectionname>" };
    DWORD dwErrorCode = PDH_PLA_ERROR_ALREADY_EXISTS;

    hPdhLibrary = LoadLibrary(L"pdh.dll");
    if (NULL == hPdhLibrary)
    {
        wprintf(L"LoadLibrary failed with %lu\n", GetLastError());
        return;
    }

    if (!FormatMessage(FORMAT_MESSAGE_FROM_HMODULE
                       FORMAT_MESSAGE_ALLOCATE_BUFFER
                       FORMAT_MESSAGE_IGNORE_INSERTS,
                       hPdhLibrary,
                       dwErrorCode,
                       0,
                       (LPWSTR)&pMessage,
                       0,
                       NULL))
    {
        wprintf(L"Format message failed with 0x%x\n", GetLastError());
        return;
    }

    wprintf(L"Formatted message: %ls\n", pMessage);
    LocalFree(pMessage);
}
```

針對資料收集和格式化函數，請務必記住，函式的傳回值會指出函式呼叫的成功或錯誤，而不一定是計數器資料。 請一律檢查傳回之計數器值的 **CStatus** 成員，以確保傳回的資料在使用之前都是有效的。 如果 **CStatus** 成員的值未表示成功，請不要使用資料。

下表提供 PDH 專用的錯誤碼清單。 這些值會定義在 `pdhmsg.h` 標頭檔中。

| 錯誤碼                                                   | 描述
|--------------------------------------------------------------|------------
| 0x00000000 (PDH \_ CSTATUS \_ 有效的 \_ 資料)                        | 傳回的資料是有效的。
| 0x00000001 (PDH \_ CSTATUS \_ 新 \_ 資料)                          | 傳回資料值有效，與最後一個範例不同。
| 0x800007D0 (PDH \_ CSTATUS \_ 沒有 \_ 電腦)                        | 無法連接到指定的電腦，或電腦已離線。
| 0x800007D1 (PDH \_ CSTATUS \_ 沒有 \_ 實例)                       | 指定的實例不存在。
| 0x800007D2 (PDH \_ 更多 \_ 資料)                                  | 要傳回的資料會比提供的緩衝區更多。 配置較大的緩衝區，然後再次呼叫函式。
| 0x800007D3 (PDH \_ CSTATUS \_ 專案 \_ 未 \_ 通過驗證)               | 資料項目已加入至查詢，但尚未經過驗證或存取。 沒有此資料項目的其他狀態資訊可供使用。
| 0x800007D4 (PDH \_ 重試)                                       | 應該重試選取的作業。
| 0x800007D5 (PDH \_ 沒有任何 \_ 資料)                                    | 沒有要傳回的資料。
| 0x800007D6 (PDH \_ 計算 \_ 負 \_ 分母)                 | 偵測到具有負分母值的計數器。
| 0x800007D7 (PDH 計算負的時間 \_ \_ \_ 基數)                    | 偵測到具有負時間基底值的計數器。
| 0x800007D8 (PDH \_ 計算 \_ 負 \_ 數值)                       | 偵測到具有負數值的計數器。
| 已取消 0x800007D9 (PDH \_ 對話 \_)                           | 使用者已取消對話方塊。
| 0x800007DA (PDH \_ 記錄檔結尾 \_ \_ \_)                          | 已到達記錄檔的結尾。
| 0x800007DB (PDH \_ 非同步 \_ 查詢 \_ 超時)                       | 等候非同步計數器集合執行緒結束時發生超時。
| 0x800007DC (PDH \_ 無法 \_ 設定 \_ 預設 \_ 即時 \_ 資料來源)  | 無法變更 set default 即時資料源。 有即時的查詢會話會收集計數器資料。
| 0xC0000BB8 (PDH \_ CSTATUS \_ 沒有 \_ 物件)                         | 在系統上找不到指定的物件。
| 0xC0000BB9 (PDH \_ CSTATUS \_ 無 \_ 計數器)                        | 找不到指定的計數器。
| 0xC0000BBA (PDH \_ CSTATUS \_ 不正確 \_ 資料)                      | 傳回的資料無效。
| 0xC0000BBB (PDH \_ 記憶體 \_ 配置 \_ 失敗)                 | PDH 函數無法配置足夠的暫存記憶體來完成作業。 請關閉部分應用程式或延伸分頁檔案，然後重試此函式。
| 0xC0000BBC (PDH \_ 不正確 \_ 控制碼)                             | 控制碼不是有效的 PDH 物件。
| 0xC0000BBD (PDH \_ 無效 \_ 引數)                           | 必要的引數遺失或不正確。
| 找不到 0xC0000BBE (PDH \_ 函數 \_ \_)                        | 找不到指定的函式。
| 0xC0000BBF (PDH \_ CSTATUS \_ 沒有 \_ COUNTERNAME)                    | 未指定任何計數器。
| 0xC0000BC0 (PDH \_ CSTATUS 不 \_ 正確的 \_ COUNTERNAME)                   | 無法剖析計數器路徑。 檢查指定路徑的格式和語法。
| 0xC0000BC1 (PDH \_ 不正確 \_ 緩衝區)                             | 呼叫端傳遞的緩衝區無效。
| 0xC0000BC2 (PDH \_ \_ 緩衝區不足)                        | 要求的資料大於提供的緩衝區。 無法傳回要求的資料。
| 0xC0000BC3 (PDH \_ 無法 \_ 連接 \_ 電腦)                    | 無法連接到要求的電腦。
| 0xC0000BC4 (PDH \_ 不正確 \_ 路徑)                               | 無法解讀指定的計數器路徑。
| 0xC0000BC5 (PDH \_ 不正確 \_ 實例)                           | 無法從指定的計數器路徑讀取實例名稱。
| 0xC0000BC6 (PDH \_ 不正確 \_ 資料)                               | 資料無效。
| 0xC0000BC7 (PDH \_ 沒有 \_ 對話 \_ 資料)                            | 對話方塊資料區塊遺失或無效。
| 0xC0000BC8 (PDH \_ 無法 \_ 讀取 \_ 名稱 \_ 字串)                 | 無法從指定的電腦讀取計數器及/或解說文字。
| 0xC0000BC9 (PDH \_ 記錄 \_ 檔 \_ 建立 \_ 錯誤)                    | 無法建立指定的記錄檔。
| 0xC0000BCA (PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤)                      | 無法開啟指定的記錄檔。
| 找不到 0xC0000BCB (PDH \_ 記錄 \_ 類型 \_ \_)                       | 此系統上未安裝指定的記錄檔類型。
| 0xC0000BCC (PDH \_ 沒有 \_ 其他 \_ 資料)                              | 沒有其他可用的資料。
| 0xC0000BCD (PDH \_ 專案 \_ 不 \_ 在 \_ 記錄檔中 \_)                   | 在記錄檔中找不到指定的記錄。
| 0xC0000BCE (PDH \_ 資料 \_ 源 \_ 是 \_ 記錄檔 \_)                 | 指定的資料來源是記錄檔。
| 0xC0000BCF (PDH \_ 資料 \_ 源 \_ 是 \_ 即時 \_)                | 指定的資料來源是目前的活動。
| 0xC0000BD0 (PDH \_ 無法 \_ 讀取 \_ 記錄檔 \_ 標頭)                   | 無法讀取記錄檔標頭。
| \_ \_ 找不到 0XC0000BD1 (PDH 檔案 \_)                            | 找不到指定的檔案。
| 0xC0000BD2 (PDH \_ 檔案 \_ 已 \_ 存在)                       | 已經有檔案具有指定的檔案名。
| 0xC0000BD3 (PDH \_ 未 \_ 執行)                            | 參考的函式尚未實作為參考。
| 找不到 0xC0000BD4 (PDH \_ 字串 \_ \_)                          | 在效能名稱和解說文字字串清單中找不到指定的字串。
| 0x80000BD5 (PDH \_ 無法 \_ 對應 \_ 名稱檔案 \_)                    | 無法對應至效能計數器名稱資料檔案。 系統會從登錄讀取資料，並儲存在本機。
| 0xC0000BD6 (PDH \_ 未知的 \_ 記錄 \_ 格式)                        | PDH DLL 無法辨識指定記錄檔的格式。
| 0xC0000BD7 (PDH \_ 不明 \_ LOGSVC \_ 命令)                    | 無法辨識指定的記錄服務命令值。
| 找不到 0xC0000BD8 (PDH \_ LOGSVC \_ 查詢 \_ \_)                   | 找不到或無法開啟從記錄服務指定的查詢。
| 0xC0000BD9 (PDH \_ LOGSVC \_ 未 \_ 開啟)                         | 無法開啟效能資料記錄服務金鑰。 這可能是因為許可權不足或未安裝服務。
| 0xC0000BDA (PDH \_ WBEM \_ 錯誤)                                 | 存取 WBEM 資料存放區時發生錯誤。
| 0xC0000BDB (PDH \_ \_ 拒絕存取)                              | 無法存取所需的電腦或服務。 針對要監視的電腦或服務上的記錄服務或互動式使用者會話，檢查其許可權和驗證。
| 0xC0000BDC (PDH \_ 記錄 \_ 檔 \_ 太 \_ 小)                       | 指定的記錄檔大小上限太小，無法記錄選取的計數器。 此記錄檔中不會記錄任何資料。 請指定一組較小的計數器來記錄或較大的檔案大小，然後重試此呼叫。
| 0xC0000BDD (PDH \_ 不正確 \_ DATASOURCE)                         | 無法連接到 ODBC 資料來源名稱。
| 0xC0000BDE (PDH \_ 不正確 \_ SQLDB)                              | SQL Database 不包含適用于 Perfmon 的有效資料表集。
| 0xC0000BDF (PDH \_ 沒有 \_ 計數器)                                | 找不到此 Perfmon SQL 記錄集的計數器。
| 0xC0000BE0 (PDH \_ SQL \_ 配置 \_ 失敗)                          | 呼叫 SQLAllocStmt 失敗，發生 %1。
| 0xC0000BE1 (PDH \_ SQL \_ ALLOCCON \_ 失敗)                       | 呼叫 SQLAllocConnect 失敗，發生 %1。
| 0xC0000BE2 (PDH \_ SQL \_ EXEC \_ 直接 \_ 失敗)                   | 呼叫 SQLExecDirect 失敗，發生 %1。
| 0xC0000BE3 (PDH \_ SQL \_ 提取 \_ 失敗)                          | 呼叫 SQLFetch 失敗，發生 %1。
| 0xC0000BE4 (PDH \_ SQL 資料列 \_ 計數 \_ 失敗)                       | 呼叫 SQLRowCount 失敗，發生 %1。
| 0xC0000BE5 (PDH \_ SQL \_ 的 \_ 結果 \_ 失敗)                  | 呼叫 SQLMoreResults 失敗，發生 %1。
| 0xC0000BE6 (PDH \_ SQL \_ CONNECT \_ 失敗)                        | 呼叫 SQLConnect 失敗，發生 %1。
| 0xC0000BE7 (PDH \_ SQL \_ BIND \_ 失敗)                           | 呼叫 SQLBindCol 失敗，發生 %1。
| 0xC0000BE8 (PDH \_ 無法連線 \_ 至 \_ WMI \_ 伺服器)                | 無法連接到所要求電腦上的 WMI 伺服器。
| 0xC0000BE9 (PDH \_ PLA \_ 集合 \_ 已在執行中 \_)           | 集合 "%1！ s！" 已在執行中。
| 0xC0000BEA (PDH \_ PLA \_ 錯誤 \_ 排程重 \_ 迭)               | 指定的開始時間晚于結束時間。
| 找不到 0xC0000BEB (PDH \_ PLA \_ 集合 \_ \_)                 | 集合 "%1！ s！" 不存在。
| 0xC0000BEC (PDH \_ PLA \_ 錯誤 \_ 排程已耗用 \_)               | 指定的結束時間已過。
| 0xC0000BED (PDH \_ PLA \_ ERROR \_ NOSTART)                         | 集合 "%1！ s！" 未啟動;檢查應用程式事件記錄檔中是否有任何錯誤。
| 0xC0000BEE (PDH \_ PLA \_ 錯誤 \_ 已 \_ 存在)                 | 集合 "%1！ s！" 已經存在。
| 0xC0000BEF (PDH \_ PLA \_ 錯誤 \_ 類型 \_ 不符)                  | 設定類型不符。
| 0xC0000BF0 (PDH \_ PLA \_ 錯誤 \_ FILEPATH)                        | 指定的資訊無法解析為有效的路徑名稱。
| 0xC0000BF1 (PDH \_ PLA \_ 服務 \_ 錯誤)                         | 「效能記錄 & 警示」服務沒有回應。
| 0xC0000BF2 (PDH \_ PLA \_ 驗證 \_ 錯誤)                      | 傳遞的資訊無效。
| 0x80000BF3 (PDH \_ PLA \_ 驗證 \_ 警告)                    | 傳遞的資訊無效。
| 0xC0000BF4 (PDH \_ PLA \_ 錯誤 \_ 名稱 \_ 太 \_ 長)                 | 提供的名稱太長。
| 0xC0000BF5 (PDH \_ 不正確 \_ SQL \_ 記錄 \_ 格式)                   | SQL 記錄格式不正確。 正確的格式為 `SQL:<DSN-name>!<LogSet-Name>` 。
| 0xC0000BF6 (PDH \_ 計數器 \_ 已 \_ 在 \_ 查詢) 中                | 效能查詢中已新增 [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) 呼叫中的效能計數器。 忽略此計數器。
| 0xC0000BF7 (PDH \_ 二進位 \_ 記錄檔已損毀 \_)                        | 無法從輸入的二進位記錄檔讀取計數器資訊和資料。
| 0xC0000BF8 (PDH \_ 記錄 \_ 範例 \_ 太 \_ 小)                     | 至少有一個輸入二進位記錄檔包含兩個以上的資料樣本。
| 0xC0000BF9 (PDH \_ OS \_ 較新 \_ 版本)                          | 電腦上名為 %1 的作業系統版本晚于本機電腦上的作業系統版本。 本機電腦無法使用這項操作。
| 0xC0000BFA (PDH \_ OS \_ 舊版 \_)                        | %1 支援 %2 或更新版本。 檢查名為 %3 之電腦上的作業系統版本。
| 0xC0000BFB (PDH \_ 不正確的 \_ 附加 \_ 時間)                     | 輸出檔案必須包含比要附加之檔案更舊的資料。
| 0xC0000BFC (PDH 不 \_ 相符的 \_ 附加 \_ 計數器)                  | 這兩個檔案都必須有相同的計數器才能附加。
| 0xC0000BFD (PDH \_ SQL \_ ALTER \_ DETAIL \_ 失敗)                  | 無法改變 SQL database 中的 CounterDetail 資料表配置。
| 0xC0000BFE (PDH \_ 查詢 \_ 效能 \_ 資料 \_ 超時)                  | 系統忙碌中。 收集計數器資料時，發生超時。 請稍後再試一次，或增加 **CollectTime** 登錄值。

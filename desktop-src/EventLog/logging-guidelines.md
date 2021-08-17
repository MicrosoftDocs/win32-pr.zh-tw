---
description: 事件記錄會代表系統和在系統上執行的應用程式，儲存重要事件的記錄。
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: 記錄指導方針
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b5bac0c2827478953a64c30e21d546e57932cf07599285f60d6ff6601eefa9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119383758"
---
# <a name="logging-guidelines"></a>記錄指導方針

事件記錄會代表系統和在系統上執行的應用程式，儲存重要事件的記錄。 由於記錄功能是一般用途，因此您必須決定適當的記錄資訊。 一般而言，您應該只記錄可能有助於診斷硬體或軟體問題的資訊。 事件記錄並非用來做為追蹤工具。

## <a name="choosing-events-to-log"></a>選擇要記錄的事件

以下是事件記錄會有説明的案例範例：

-   資源問題。 當記憶體配置失敗時，記錄警告事件有助於指出記憶體不足狀況的原因。
-   硬體問題。 如果設備磁碟機發生磁碟控制卡超時、平行埠的電源中斷，或網路或序列卡的資料錯誤，設備磁碟機可以記錄這些事件的相關資訊，以協助系統管理員診斷硬體問題。
-   損毀的磁區。 如果磁片驅動程式遇到損壞的磁區，它可能會在重試作業之後讀取或寫入磁區，但最後的磁區將會不良。 如果磁片驅動程式可以繼續，則應該記錄警告事件;否則，它應該記錄錯誤事件。 如果檔案系統驅動程式發現大量的損毀的磁區並修正它們，記錄警告事件可能有助於系統管理員判斷磁片可能即將失敗。
-   資訊事件。 伺服器應用程式 (例如資料庫伺服器) 記錄使用者登入、開啟資料庫或開機檔案傳輸。 伺服器也可以記錄其他事件（例如錯誤） (無法存取檔案、主機進程中斷連接等) 、資料庫損毀，或檔案傳輸是否成功。

## <a name="writing-messages"></a>寫入訊息

對於嘗試針對問題進行疑難排解的系統管理員和使用者而言，訊息應該是合理的。 訊息應該包含所有必要資訊，以瞭解造成問題的原因，以及如何修正問題。

避免寫入一則模糊的訊息，例如「從 i/o 子系統接收的驅動程式封包無效。 資料為封包。」更好的訊息會指出有問題的驅動程式正常運作，但會記錄格式不正確的封包。 您可以繼續說，需要有 Unicode 版本的驅動程式才能更正問題。 如需有關撰寫良好錯誤訊息的詳細資訊，請參閱 [錯誤訊息指導方針](/windows/desktop/Debug/error-message-guidelines)。

請勿在郵件內文中使用 tab 或逗點，因為事件記錄檔可以儲存為逗號或 tab 分隔的文字檔。 許多組織會將這些檔案匯入資料庫中，而額外的格式化字元需要手動操作。

使用 UNC 名稱或其他包含空格的連結時，請將名稱括在角括弧中。 例如，<\\ \\ *共用* \\ *名 servername*>。 您可以將 URL 寫入至訊息結尾，以將使用者指向相關的說明內容。 URL 必須是完整的 DNS 主機名稱。 例如，您可以將下列文字附加至訊息：「如需有關此訊息的詳細資訊，請造訪我們的支援網站」 https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp 。 連結會導致 ASP 頁面將使用者重新導向至與錯誤訊息相關的內容。 它會剖析 (在) URL 時傳遞的額外參數，以判斷要將使用者重新導向至何處。

傳遞至 [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) 函數的引數會附加至 URL，如下所示：

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

如果事件來源的郵件 DLL 標頭中的公司名稱、產品名稱、產品版本、檔案名和檔案版本是有效的，則它們也會附加至 URL：

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>減少額外負荷

事件記錄會耗用磁碟空間和處理器時間等資源。 事件記錄檔所需的磁碟空間量，以及記錄事件的應用程式所產生的額外負荷，取決於您選擇要記錄多少資訊。 這就是為什麼只記錄基本資訊很重要的原因。 也可以將事件記錄呼叫放入程式碼中的錯誤路徑，而不是在主要程式碼路徑中，這樣會降低效能。

每個事件記錄檔記錄所需的磁碟空間量包括 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) 結構的成員。 這是可變長度的結構;字串和二進位資料會儲存在結構後面。

 

 

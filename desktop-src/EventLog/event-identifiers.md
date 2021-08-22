---
description: 事件識別碼可唯一識別特定的事件。
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: '事件記錄 (事件識別碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951437"
---
# <a name="event-identifiers-event-logging"></a>事件記錄 (事件識別碼) 

事件識別碼可唯一識別特定的事件。 每個 [事件來源](event-sources.md) 都可以定義自己的編號事件，以及它們在其訊息檔案中對應的描述字串。 事件檢視器可將這些字串呈現給使用者。 他們應該可以協助使用者瞭解發生什麼問題，並建議要採取的動作。 引導使用者解決自己的問題，而不是在系統管理員或支援技術人員上的說明。 如需詳細資訊，請參閱 [錯誤訊息指導方針](/windows/desktop/Debug/error-message-guidelines)。

## <a name="format"></a>格式

下圖說明事件識別碼的格式。

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>嚴重性
</dt> <dd>

嚴重性。 嚴重性的定義如下：

<dl> <dd>00-成功</dd> <dd>01-資訊</dd> <dd>10-警告</dd> <dd>11-錯誤</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

客戶位。 此位定義如下：

<dl> <dd>0-系統程式碼</dd> <dd>1-客戶程式碼</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

保留位元 

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>設施
</dt> <dd>

設備碼。 此值可以是設備 \_ Null。

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>代碼
</dt> <dd>

設備的狀態碼。

</dd> </dl>

## <a name="message-definitions"></a>訊息定義

訊息是在事件訊息檔案中定義。 事件訊息檔中的描述字串是依事件識別碼進行編制索引，讓事件檢視器根據事件識別碼顯示任何事件的事件特定文字。 所有描述都具有當地語系化和語言相依。 如需建立訊息檔案的詳細資訊，請參閱 [訊息文字檔](message-text-files.md)。

描述字串可能包含%*n* 形式的插入字串預留位置，其中 %1 表示第一個插入字串，依此類推。 例如，以下是在 mc 檔案中的範例專案：

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

在此情況下， [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) 所傳回的緩衝區會包含插入字串。 [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord)結構的 **NumStrings** 成員表示插入字串的數目。 **EVENTLOGRECORD** 結構的 **StringOffset** 成員表示緩衝區中第一個插入字串的位置。 您可以傳遞 DWORD \_ PTRs 的陣列，這個陣列會在呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函式時，指向緩衝區中每個字串的位址，並將字串插入訊息中。

描述字串也可以包含參數訊息檔案中參數字串的預留位置。 預留位置的格式為%%*n*，其中% %1 取代為識別碼為1的參數字串，依此類推。 不過，您必須將參數字串插入 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 傳回的訊息字串中。 一般來說，您會呼叫 **FormatMessage** 來取得事件的訊息字串。 然後，您可以剖析%%*n* 參數的訊息字串。 如果訊息包含一或多個參數，請載入來源的 **ParameterMessageFile** 登錄值。 針對訊息字串中的每個參數，取得識別碼，並將它傳遞給 **FormatMessage** 以取得參數字串。 將訊息字串中的參數取代為 **FormatMessage** 傳回的參數字串。

## <a name="insertion-strings"></a>插入字串

插入字串是選擇性的語言獨立字串，用來填入描述字串中的預留位置值。 因為字串未當地語系化，所以這些預留位置只能用來表示與語言無關的字串，例如數值、檔案名、使用者名稱等等。 字串長度不能超過 32 kb-1 個字元。

請避免使用數個字串來建立較大的描述。 插入字串應該被視為資料，而不是文字。 例如，在下列範例中，不應該使用 pszString1 和 pszString2 做為 pszDescription 的插入字串。

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

在下列範例中，您適合使用 pszString1 或 pszString2 在 pszDescription 中插入字串。

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 

---
description: 每個事件來源都應該註冊訊息檔案，其中包含每個事件識別碼、事件類別目錄和參數的描述字串。
ms.assetid: 0c251a45-1414-4855-a6f5-86ebdfab2693
title: 訊息檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb20d5919c75f06bfd7b6db9b47216566ab6ac8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513157"
---
# <a name="message-files"></a>訊息檔案

每個 [事件來源](event-sources.md) 都應該註冊訊息檔案，其中包含每個 [事件識別碼](event-identifiers.md)、 [事件類別目錄](event-categories.md)和 [參數](event-identifiers.md)的描述字串。 在事件來源的 **EventMessageFile**、 **CategoryMessageFile** 和 **ParameterMessageFile** 登錄值中註冊這些檔案。

您可以建立一個包含事件識別碼、分類和參數描述的訊息檔案，或建立三個不同的訊息檔案。 無論您是在一個檔案或三個檔案中指定訊息，所有訊息的訊息識別碼都應該是唯一的。 數個應用程式可以共用相同的訊息檔案。 如需訊息檔案的詳細資訊，請參閱 [**訊息編譯器**](/windows/desktop/WES/message-compiler--mc-exe-)。 如需訊息檔語法的詳細資訊，請參閱 [訊息文字檔](message-text-files.md)。

## <a name="example-message-file"></a>範例訊息檔案

以下是範例訊息檔案。

``` syntax
; /* --------------------------------------------------------
; HEADER SECTION
;*/
SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
               Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
               Warning=0x2:STATUS_SEVERITY_WARNING
               Error=0x3:STATUS_SEVERITY_ERROR
              )
;
;
FacilityNames=(System=0x0:FACILITY_SYSTEM
               Runtime=0x2:FACILITY_RUNTIME
               Stubs=0x3:FACILITY_STUBS
               Io=0x4:FACILITY_IO_ERROR_CODE
              )
;
;/* ------------------------------------------------------------------
; MESSAGE DEFINITION SECTION
;*/

MessageIdTypedef=WORD

MessageId=0x1
SymbolicName=CAT_1
Language=English
Category 1
.

MessageId=0x2
SymbolicName=CAT_2
Language=English
Category 2
.

MessageId=0x3
SymbolicName=CAT_3
Language=English
Category 3
.

MessageIdTypedef=DWORD

MessageId=0x100
Severity=Error
Facility=Runtime
SymbolicName=MSG_COMMAND_ERR
Language=English
The command is incorrect. 
.

MessageId=0x101
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

MessageId=0x102
Severity=Error
Facility=System
SymbolicName=MSG_FILE_BAD_CONTENTS
Language=English
File %1 contains %2, which is in error
.

MessageId=0x103
Severity=Warning
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1 retrys with %2 success! Disconnect from
the server and retry later.
.

MessageId=0x104
Severity=Informational
Facility=System
SymbolicName=MSG_INSERT_DISK
Language=English
Insert %%1000 in %%1001 and hit any key when ready... 
.

;/* Insert string parameters */
;

MessageId=1000
Severity=Success
Facility=System
SymbolicName=DISK
Language=English
disk%0
.

MessageId=1001
Severity=Success
Facility=System
SymbolicName=DRIVE
Language=English
drive%0
.
```

事件查看應用程式可使用下列程式取得訊息 DLL 中的 [訊息字串](event-identifiers.md) 存取權。

**取得描述字串**

1.  呼叫 [**RegOpenKey**](/windows/desktop/api/winreg/nf-winreg-regopenkeya) 函數來開啟事件來源。
2.  呼叫 [**RegQueryValueEx**](/windows/desktop/api/winreg/nf-winreg-regqueryvalueexa) 函數，以取得事件來源的 **EventMessageFile** 值內容，也就是訊息 DLL 的名稱。
3.  呼叫 [**LoadLibraryEx**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa) 函式以載入步驟2所決定的訊息 DLL。
4.  使用訊息識別碼呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 函數，以從 DLL 取得描述。  (請注意，訊息識別碼是在中定義。訊息編譯器所產生的 H 檔案。 ) **FormatMessage** 函式會使用您傳遞的引數值來取代插入字串，但不會取代參數插入字串;您必須在顯示字串之前，自行取代參數插入字串。

 

 

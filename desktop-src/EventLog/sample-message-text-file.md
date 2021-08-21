---
description: 下列範例訊息檔會示範如何建立和使用以多種語言定義訊息的訊息文字檔。
ms.assetid: 403eaccc-07a3-4368-a39a-18c706c65537
title: 範例訊息文字檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60f59e6d20f53560da6f1230886fe6c8cbb54b9052b97c2293d0f49720743ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151484"
---
# <a name="sample-message-text-file"></a>範例訊息文字檔

下列範例訊息檔會示範如何建立和使用以多種語言定義訊息的訊息文字檔。

## <a name="sample-message-file"></a>範例訊息檔案

這個範例訊息檔 Sample.mc 包含一個批註區塊，後面接著一個標頭區段，後面接著兩個語言的訊息。 您必須使用 Unicode 相容的編輯器，同時支援不同書寫語言所使用的字元。 如需有關 mc 檔案語法的詳細資訊和詳細說明，請參閱 [訊息文字檔](message-text-files.md)。

``` syntax
; // ***** Sample.mc *****
; // This is the header section.

MessageIdTypedef=DWORD

SeverityNames=(Success=0x0:STATUS_SEVERITY_SUCCESS
Informational=0x1:STATUS_SEVERITY_INFORMATIONAL
Warning=0x2:STATUS_SEVERITY_WARNING
Error=0x3:STATUS_SEVERITY_ERROR
)

FacilityNames=(System=0x0:FACILITY_SYSTEM
Runtime=0x2:FACILITY_RUNTIME
Stubs=0x3:FACILITY_STUBS
Io=0x4:FACILITY_IO_ERROR_CODE
)

LanguageNames=(English=0x409:MSG00409)
LanguageNames=(Japanese=0x411:MSG00411)

; // The following are message definitions.

MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x2
Severity=Warning
Facility=Io
SymbolicName=MSG_BAD_PARM1
Language=English
Cannot reconnect to the server.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x3
Severity=Success
Facility=System
SymbolicName=MSG_STRIKE_ANY_KEY
Language=English
Press any key to continue . . . %0
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2 which is in error.
.

Language=Japanese
<Japanese message string goes here>
.

MessageId=0x5
Severity=Informational
Facility=System
SymbolicName=MSG_RETRYS
Language=English
There have been %1!d! attempts with %2!d!%% success%! Disconnect from 
the server and try again later.
.

Language=Japanese
<Japanese message string goes here>
.
```

 

 




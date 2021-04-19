---
description: 下列範例訊息檔會示範如何建立和使用以多種語言定義訊息的訊息文字檔。
ms.assetid: 403eaccc-07a3-4368-a39a-18c706c65537
title: 範例訊息文字檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e4247b1e39ef94c006262f282d8d830af11851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979098"
---
# <a name="sample-message-text-file"></a><span data-ttu-id="9fb9e-103">範例訊息文字檔</span><span class="sxs-lookup"><span data-stu-id="9fb9e-103">Sample Message Text File</span></span>

<span data-ttu-id="9fb9e-104">下列範例訊息檔會示範如何建立和使用以多種語言定義訊息的訊息文字檔。</span><span class="sxs-lookup"><span data-stu-id="9fb9e-104">The following sample message file shows how to create and use a message text file that defines messages in multiple languages.</span></span>

## <a name="sample-message-file"></a><span data-ttu-id="9fb9e-105">範例訊息檔案</span><span class="sxs-lookup"><span data-stu-id="9fb9e-105">Sample Message File</span></span>

<span data-ttu-id="9fb9e-106">這個範例訊息檔 Sample.mc 包含一個批註區塊，後面接著一個標頭區段，後面接著兩個語言的訊息。</span><span class="sxs-lookup"><span data-stu-id="9fb9e-106">This sample message file, Sample.mc, contains a comment block, followed by a header section, followed by messages in two languages.</span></span> <span data-ttu-id="9fb9e-107">您必須使用 Unicode 相容的編輯器，同時支援不同書寫語言所使用的字元。</span><span class="sxs-lookup"><span data-stu-id="9fb9e-107">You must use a Unicode-compatible editor to simultaneously support the characters used in different written languages.</span></span> <span data-ttu-id="9fb9e-108">如需有關 mc 檔案語法的詳細資訊和詳細說明，請參閱 [訊息文字檔](message-text-files.md)。</span><span class="sxs-lookup"><span data-stu-id="9fb9e-108">For more information and a detailed description of the syntax of .mc files, see [Message Text Files](message-text-files.md).</span></span>

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

 

 




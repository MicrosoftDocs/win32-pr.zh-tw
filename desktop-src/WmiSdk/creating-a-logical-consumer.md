---
description: 邏輯取用者是永久事件取用者類別的實例。
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: 建立邏輯取用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983868"
---
# <a name="creating-a-logical-consumer"></a>建立邏輯取用者

邏輯取用者是永久事件取用者類別的實例。 邏輯取用者的主要目的是為實體取用者提供實體取用者所執行活動的參數。 如需詳細資訊，請參閱 [建立新的永久事件取用者類別](creating-a-new-permanent-event-consumer-class.md)。 永久取用者在取用者、篩選和系結實例中必須具有相同的 [**CreatorSID**](--eventconsumer.md) 。 如需詳細資訊，請參閱 [安全地接收事件](receiving-events-securely.md)。 如需使用邏輯取用者的範例，請參閱 [根據事件執行腳本](running-a-script-based-on-an-event.md)，它會顯示使用標準取用者類別 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 來設定永久取用者。

下列程式說明如何建立邏輯取用者。

**建立邏輯取用者**

1.  建立永久取用者類別的實例。
2.  使用您想要實體取用者執行之動作的參數，填滿實例的屬性。

下列 MOF 程式碼範例說明包含腳本的邏輯取用者。

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

建立邏輯取用者之後，您必須將每個篩選準則連結至事件篩選器，以將動作指派給特定的事件。 如需詳細資訊，請參閱 [建立事件篩選](creating-an-event-filter.md)。

 

 




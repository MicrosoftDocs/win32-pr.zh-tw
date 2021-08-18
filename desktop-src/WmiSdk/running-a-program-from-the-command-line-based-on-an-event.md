---
description: CommandLineEventConsumer 類別會在指定的事件發生時，從命令列執行指定的可執行程式。 此類別是 WMI 提供的標準事件取用者。
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: 根據事件從命令列執行程式
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c499713b3c6496759d94229e291138b0cb07de9e9f35d116eb19b4a7aeb3829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553965"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>根據事件從命令列執行程式

[**CommandLineEventConsumer**](commandlineeventconsumer.md)類別會在指定的事件發生時，從命令列執行指定的可執行程式。 此類別是 WMI 提供的標準事件取用者。

當您使用 [**CommandLineEventConsumer**](commandlineeventconsumer.md)時，應該保護您想要啟動的可執行檔。 如果可執行檔不在安全的位置，或未使用強式存取控制清單保護 (ACL) ，則沒有存取權限的使用者可以使用不同的可執行檔來取代您的可執行檔。 您可以使用 [**win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) 或 [**win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) 類別，以程式設計方式變更檔案或共用的安全性。 如需詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。 下列程式會新增至基本程式，專屬於 [**CommandLineEventConsumer**](commandlineeventconsumer.md) 類別，並說明如何建立可執行程式的事件取用者。

> [!Caution]
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md)類別具有特殊的安全性條件約束。 此標準取用者必須由本機電腦上 Administrators 群組的本機成員進行設定。 如果您使用網域帳戶來建立訂用帳戶，LocalSystem 帳戶必須擁有網域的必要許可權，才能確認建立者是本機系統管理員群組的成員。
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md) 無法用來啟動以互動方式執行的進程。

 

下列程式描述如何建立從命令列執行進程的事件取用者。

**若要建立從命令列執行進程的事件取用者**

1.  在受控物件格式 (MOF) 檔中，建立 [**CommandLineEventConsumer**](commandlineeventconsumer.md) 的實例，以接收您在查詢中要求的事件。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。
2.  建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並為其命名。
3.  建立查詢以指定事件的類型。 如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。
4.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**CommandLineEventConsumer**](commandlineeventconsumer.md)的實例產生關聯。
5.  使用 [**Mofcomp.exe**](mofcomp.md)編譯您的 MOF 檔案。

## <a name="example"></a>範例

下列程式碼範例會建立名為 "MyCmdLineConsumer" 的新類別，以便在 MOF 結束時建立新類別的實例時產生事件。 此範例是在 MOF 程式碼中，但您可以使用適用于 WMI 的 [腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。

下列程式說明如何建立名為 MyCmdLineConsumer 的新類別。

**若要建立名為 MyCmdLineConsumer 的新類別**

1.  \\ \_ 使用可執行可見程式的命令（例如 "calc.exe"）建立 c： cmdlinetest.bat 檔案。
2.  將 MOF 複製到文字檔，並使用 mof 副檔名加以儲存。
3.  在命令視窗中，使用下列命令編譯 MOF 檔案： **mofcomp.exe filename. MOF**。

> [!Note]  
> Cmdlinetest.bat 中指定的程式 \_ 應該執行。

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

---
description: ActiveScriptEventConsumer 類別所執行的標準取用者可讓電腦執行腳本，並在發生重要事件時採取動作，以確保電腦可以自動偵測並解決問題。
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: 根據事件執行腳本
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852016"
---
# <a name="running-a-script-based-on-an-event"></a>根據事件執行腳本

[**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別所執行的標準取用者可讓電腦執行腳本，並在發生重要事件時採取動作，以確保電腦可以自動偵測並解決問題。

此取用者預設會在 **根 \\ 訂** 用帳戶命名空間中載入。

您可以在 [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)的單一實例中設定 **Timeout** 或 **MaximumScripts** 屬性的值，以設定系統上所有 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)實例的效能。

使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。 下列新增至基本程式的程式是 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別特有的程式，並說明如何建立執行腳本的事件取用者。

> [!Caution]  
> [**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別具有特殊的安全性條件約束。 此標準取用者必須由本機電腦上 Administrators 群組的本機成員進行設定。 如果您使用網域帳戶來建立訂用帳戶，LocalSystem 帳戶必須擁有網域的必要許可權，才能確認建立者是本機系統管理員群組的成員。

 

下列程式描述如何建立執行腳本的事件取用者。

**若要建立執行腳本的事件取用者**

1.  撰寫要在事件發生時執行的腳本。

    您可以使用任何語言撰寫腳本，但請確定您所選語言的腳本引擎已安裝在您的電腦上。 腳本不需要使用 WMI 腳本物件。

    只有系統管理員可以設定腳本取用者，而腳本會在 LocalSystem 認證下執行，這可為取用者提供廣泛的功能，但網路存取除外。 不過，腳本無法存取特定使用者登入資料，例如環境變數和網路共用。

2.  在受控物件格式 (MOF) 檔中，建立 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 的實例，以接收您在查詢中要求的事件。

    您可以將腳本的文字放在 **ScriptText** 中，也可以在 **ScriptFileName** 中指定腳本的路徑和檔案名。 如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。

3.  建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，將它命名為，然後建立查詢來指定事件的類型，以觸發執行腳本。

    如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。

4.  建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)的實例產生關聯。
5.  使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。

下一節中的範例會示範兩種方法來執行事件驅動的腳本。 第一個範例會使用定義于外部檔案的腳本，而第二個範例會使用 MOF 程式碼內建的腳本。 這些範例位於 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。

## <a name="example-using-an-external-script"></a>使用外部腳本的範例

下列程式說明如何使用外部腳本範例。

**使用外部腳本範例**

1.  建立名為 c：Asec.vbs 的檔案 \\ ，然後將此範例中的腳本複製到其中。
2.  將 MOF 清單複製到文字檔中，並以 mof 副檔名儲存檔案。
3.  在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案。

    **Mofcomp.exe** *filename * * *. mof**

4.  執行計算機來建立 calc.exe 進程。 等候超過五秒，關閉計算機視窗，然後查看 C： \\ 目錄中名為 ASEC 的檔案。

    下列文字類似于將包含在 ASEC 檔中的文字。

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

下列 VBScript 程式碼範例顯示永久性取用者收到事件時所呼叫的腳本。 **TargetEvent** 物件是一個 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)實例，所以它有一個名為 **TargetInstance** 的屬性，它是用來引發事件的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)實例。 **Win32 \_ 進程** 類別的 **UserModeTime** 和 **KernelModeTime** 屬性會放入腳本所建立的記錄檔中。


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



下列 MOF 程式碼範例會在收到事件時呼叫腳本。 它會在 **根 \\ 訂** 用帳戶命名空間中建立篩選、取用者以及它們之間的系結。

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>使用內嵌腳本的範例

下列程式說明如何使用內嵌腳本範例。

**若要使用內嵌腳本範例**

1.  將此區段中的 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。
2.  在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案。

    **Mofcomp.exe** *filename * * *. mof**

下列 MOF 程式碼範例會建立篩選器、取用者以及兩者之間的系結，而且也包含內嵌腳本。

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

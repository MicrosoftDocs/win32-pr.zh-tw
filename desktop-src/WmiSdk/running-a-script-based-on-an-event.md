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
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="a8d26-103">根據事件執行腳本</span><span class="sxs-lookup"><span data-stu-id="a8d26-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="a8d26-104">[**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別所執行的標準取用者可讓電腦執行腳本，並在發生重要事件時採取動作，以確保電腦可以自動偵測並解決問題。</span><span class="sxs-lookup"><span data-stu-id="a8d26-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="a8d26-105">此取用者預設會在 **根 \\ 訂** 用帳戶命名空間中載入。</span><span class="sxs-lookup"><span data-stu-id="a8d26-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="a8d26-106">您可以在 [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)的單一實例中設定 **Timeout** 或 **MaximumScripts** 屬性的值，以設定系統上所有 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)實例的效能。</span><span class="sxs-lookup"><span data-stu-id="a8d26-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="a8d26-107">使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="a8d26-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="a8d26-108">下列新增至基本程式的程式是 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 類別特有的程式，並說明如何建立執行腳本的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="a8d26-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="a8d26-109">[**ActiveScriptEventConsumer**](activescripteventconsumer.md)類別具有特殊的安全性條件約束。</span><span class="sxs-lookup"><span data-stu-id="a8d26-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="a8d26-110">此標準取用者必須由本機電腦上 Administrators 群組的本機成員進行設定。</span><span class="sxs-lookup"><span data-stu-id="a8d26-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="a8d26-111">如果您使用網域帳戶來建立訂用帳戶，LocalSystem 帳戶必須擁有網域的必要許可權，才能確認建立者是本機系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="a8d26-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="a8d26-112">下列程式描述如何建立執行腳本的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="a8d26-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="a8d26-113">**若要建立執行腳本的事件取用者**</span><span class="sxs-lookup"><span data-stu-id="a8d26-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="a8d26-114">撰寫要在事件發生時執行的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="a8d26-115">您可以使用任何語言撰寫腳本，但請確定您所選語言的腳本引擎已安裝在您的電腦上。</span><span class="sxs-lookup"><span data-stu-id="a8d26-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="a8d26-116">腳本不需要使用 WMI 腳本物件。</span><span class="sxs-lookup"><span data-stu-id="a8d26-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="a8d26-117">只有系統管理員可以設定腳本取用者，而腳本會在 LocalSystem 認證下執行，這可為取用者提供廣泛的功能，但網路存取除外。</span><span class="sxs-lookup"><span data-stu-id="a8d26-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="a8d26-118">不過，腳本無法存取特定使用者登入資料，例如環境變數和網路共用。</span><span class="sxs-lookup"><span data-stu-id="a8d26-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="a8d26-119">在受控物件格式 (MOF) 檔中，建立 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 的實例，以接收您在查詢中要求的事件。</span><span class="sxs-lookup"><span data-stu-id="a8d26-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="a8d26-120">您可以將腳本的文字放在 **ScriptText** 中，也可以在 **ScriptFileName** 中指定腳本的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="a8d26-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="a8d26-121">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="a8d26-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="a8d26-122">建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，將它命名為，然後建立查詢來指定事件的類型，以觸發執行腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="a8d26-123">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="a8d26-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="a8d26-124">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**ActiveScriptEventConsumer**](activescripteventconsumer.md)的實例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="a8d26-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="a8d26-125">使用 [**Mofcomp.exe**](mofcomp.md)編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="a8d26-126">下一節中的範例會示範兩種方法來執行事件驅動的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="a8d26-127">第一個範例會使用定義于外部檔案的腳本，而第二個範例會使用 MOF 程式碼內建的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="a8d26-128">這些範例位於 MOF 程式碼中，但您可以使用 [適用于 wmi 的腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。</span><span class="sxs-lookup"><span data-stu-id="a8d26-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="a8d26-129">使用外部腳本的範例</span><span class="sxs-lookup"><span data-stu-id="a8d26-129">Example Using an External Script</span></span>

<span data-ttu-id="a8d26-130">下列程式說明如何使用外部腳本範例。</span><span class="sxs-lookup"><span data-stu-id="a8d26-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="a8d26-131">**使用外部腳本範例**</span><span class="sxs-lookup"><span data-stu-id="a8d26-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="a8d26-132">建立名為 c：Asec.vbs 的檔案 \\ ，然後將此範例中的腳本複製到其中。</span><span class="sxs-lookup"><span data-stu-id="a8d26-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="a8d26-133">將 MOF 清單複製到文字檔中，並以 mof 副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="a8d26-134">在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="a8d26-135">**Mofcomp.exe** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="a8d26-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="a8d26-136">執行計算機來建立 calc.exe 進程。</span><span class="sxs-lookup"><span data-stu-id="a8d26-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="a8d26-137">等候超過五秒，關閉計算機視窗，然後查看 C： \\ 目錄中名為 ASEC 的檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="a8d26-138">下列文字類似于將包含在 ASEC 檔中的文字。</span><span class="sxs-lookup"><span data-stu-id="a8d26-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="a8d26-139">下列 VBScript 程式碼範例顯示永久性取用者收到事件時所呼叫的腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="a8d26-140">**TargetEvent** 物件是一個 [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md)實例，所以它有一個名為 **TargetInstance** 的屬性，它是用來引發事件的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)實例。</span><span class="sxs-lookup"><span data-stu-id="a8d26-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="a8d26-141">**Win32 \_ 進程** 類別的 **UserModeTime** 和 **KernelModeTime** 屬性會放入腳本所建立的記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="a8d26-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


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



<span data-ttu-id="a8d26-142">下列 MOF 程式碼範例會在收到事件時呼叫腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="a8d26-143">它會在 **根 \\ 訂** 用帳戶命名空間中建立篩選、取用者以及它們之間的系結。</span><span class="sxs-lookup"><span data-stu-id="a8d26-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

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

## <a name="example-using-inline-script"></a><span data-ttu-id="a8d26-144">使用內嵌腳本的範例</span><span class="sxs-lookup"><span data-stu-id="a8d26-144">Example Using Inline Script</span></span>

<span data-ttu-id="a8d26-145">下列程式說明如何使用內嵌腳本範例。</span><span class="sxs-lookup"><span data-stu-id="a8d26-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="a8d26-146">**若要使用內嵌腳本範例**</span><span class="sxs-lookup"><span data-stu-id="a8d26-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="a8d26-147">將此區段中的 MOF 清單複製到文字檔中，並以 MOF 副檔名儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="a8d26-148">在 [命令提示字元] 視窗中，使用下列命令編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="a8d26-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="a8d26-149">**Mofcomp.exe** *filename \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="a8d26-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="a8d26-150">下列 MOF 程式碼範例會建立篩選器、取用者以及兩者之間的系結，而且也包含內嵌腳本。</span><span class="sxs-lookup"><span data-stu-id="a8d26-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="a8d26-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="a8d26-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8d26-152">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="a8d26-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

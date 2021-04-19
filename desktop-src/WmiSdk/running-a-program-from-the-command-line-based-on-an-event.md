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
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000264"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="10296-104">根據事件從命令列執行程式</span><span class="sxs-lookup"><span data-stu-id="10296-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="10296-105">[**CommandLineEventConsumer**](commandlineeventconsumer.md)類別會在指定的事件發生時，從命令列執行指定的可執行程式。</span><span class="sxs-lookup"><span data-stu-id="10296-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="10296-106">此類別是 WMI 提供的標準事件取用者。</span><span class="sxs-lookup"><span data-stu-id="10296-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="10296-107">當您使用 [**CommandLineEventConsumer**](commandlineeventconsumer.md)時，應該保護您想要啟動的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="10296-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="10296-108">如果可執行檔不在安全的位置，或未使用強式存取控制清單保護 (ACL) ，則沒有存取權限的使用者可以使用不同的可執行檔來取代您的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="10296-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="10296-109">您可以使用 [**win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) 或 [**win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) 類別，以程式設計方式變更檔案或共用的安全性。</span><span class="sxs-lookup"><span data-stu-id="10296-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="10296-110">如需詳細資訊，請參閱 [在 c + + 中建立新物件的安全描述項](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。</span><span class="sxs-lookup"><span data-stu-id="10296-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="10296-111">使用標準取用者的基本程式一律相同，且位於 [監視和回應標準取用者的事件](monitoring-and-responding-to-events-with-standard-consumers.md)。</span><span class="sxs-lookup"><span data-stu-id="10296-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="10296-112">下列程式會新增至基本程式，專屬於 [**CommandLineEventConsumer**](commandlineeventconsumer.md) 類別，並說明如何建立可執行程式的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="10296-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="10296-113">[**CommandLineEventConsumer**](commandlineeventconsumer.md)類別具有特殊的安全性條件約束。</span><span class="sxs-lookup"><span data-stu-id="10296-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="10296-114">此標準取用者必須由本機電腦上 Administrators 群組的本機成員進行設定。</span><span class="sxs-lookup"><span data-stu-id="10296-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="10296-115">如果您使用網域帳戶來建立訂用帳戶，LocalSystem 帳戶必須擁有網域的必要許可權，才能確認建立者是本機系統管理員群組的成員。</span><span class="sxs-lookup"><span data-stu-id="10296-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="10296-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) 無法用來啟動以互動方式執行的進程。</span><span class="sxs-lookup"><span data-stu-id="10296-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="10296-117">下列程式描述如何建立從命令列執行進程的事件取用者。</span><span class="sxs-lookup"><span data-stu-id="10296-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="10296-118">**若要建立從命令列執行進程的事件取用者**</span><span class="sxs-lookup"><span data-stu-id="10296-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="10296-119">在受控物件格式 (MOF) 檔中，建立 [**CommandLineEventConsumer**](commandlineeventconsumer.md) 的實例，以接收您在查詢中要求的事件。</span><span class="sxs-lookup"><span data-stu-id="10296-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="10296-120">如需詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。</span><span class="sxs-lookup"><span data-stu-id="10296-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="10296-121">建立 [**\_ \_ >eventfilter**](--eventfilter.md)的實例，並為其命名。</span><span class="sxs-lookup"><span data-stu-id="10296-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="10296-122">建立查詢以指定事件的類型。</span><span class="sxs-lookup"><span data-stu-id="10296-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="10296-123">如需詳細資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="10296-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="10296-124">建立 [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md)的實例，以將篩選器與 [**CommandLineEventConsumer**](commandlineeventconsumer.md)的實例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="10296-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="10296-125">使用 [**Mofcomp.exe**](mofcomp.md)編譯您的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="10296-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="10296-126">範例</span><span class="sxs-lookup"><span data-stu-id="10296-126">Example</span></span>

<span data-ttu-id="10296-127">下列程式碼範例會建立名為 "MyCmdLineConsumer" 的新類別，以便在 MOF 結束時建立新類別的實例時產生事件。</span><span class="sxs-lookup"><span data-stu-id="10296-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="10296-128">此範例是在 MOF 程式碼中，但您可以使用適用于 WMI 的 [腳本 API](scripting-api-for-wmi.md) 或 [適用于 WMI 的 COM API](com-api-for-wmi.md)，以程式設計方式建立實例。</span><span class="sxs-lookup"><span data-stu-id="10296-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="10296-129">下列程式說明如何建立名為 MyCmdLineConsumer 的新類別。</span><span class="sxs-lookup"><span data-stu-id="10296-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="10296-130">**若要建立名為 MyCmdLineConsumer 的新類別**</span><span class="sxs-lookup"><span data-stu-id="10296-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="10296-131">\\ \_ 使用可執行可見程式的命令（例如 "calc.exe"）建立 c： cmdlinetest.bat 檔案。</span><span class="sxs-lookup"><span data-stu-id="10296-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="10296-132">將 MOF 複製到文字檔，並使用 mof 副檔名加以儲存。</span><span class="sxs-lookup"><span data-stu-id="10296-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="10296-133">在命令視窗中，使用下列命令編譯 MOF 檔案： **mofcomp.exe filename. MOF**。</span><span class="sxs-lookup"><span data-stu-id="10296-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="10296-134">Cmdlinetest.bat 中指定的程式 \_ 應該執行。</span><span class="sxs-lookup"><span data-stu-id="10296-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="10296-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="10296-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10296-136">使用標準取用者監視及回應事件</span><span class="sxs-lookup"><span data-stu-id="10296-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 

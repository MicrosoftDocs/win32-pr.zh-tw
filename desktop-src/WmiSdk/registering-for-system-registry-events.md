---
description: 若要從系統登錄提供者接收通知，管理應用程式必須註冊為暫存事件取用者。
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: 註冊系統登錄事件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980047"
---
# <a name="registering-for-system-registry-events"></a><span data-ttu-id="2de8e-103">註冊系統登錄事件</span><span class="sxs-lookup"><span data-stu-id="2de8e-103">Registering for System Registry Events</span></span>

<span data-ttu-id="2de8e-104">若要從 [系統登錄](/previous-versions/windows/desktop/regprov/system-registry-provider) 提供者接收通知，管理應用程式必須註冊為暫存事件取用者。</span><span class="sxs-lookup"><span data-stu-id="2de8e-104">To receive notifications from the [System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider) provider, a management application must register as a temporary event consumer.</span></span> <span data-ttu-id="2de8e-105">註冊 System Registry 提供者的大部分需求與其他任何事件註冊相同，不過您也必須執行下列程式。</span><span class="sxs-lookup"><span data-stu-id="2de8e-105">Most of the requirements to register for the System Registry provider are the same as any other event registration, except you must also perform the following procedure.</span></span>

<span data-ttu-id="2de8e-106">登錄提供者會為系統登錄中的事件提供事件類別。</span><span class="sxs-lookup"><span data-stu-id="2de8e-106">The registry provider supplies event classes for events in the system registry.</span></span> <span data-ttu-id="2de8e-107">如需一般事件註冊的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-107">For more information about general event registration, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="2de8e-108">下列程式說明如何註冊系統登錄事件。</span><span class="sxs-lookup"><span data-stu-id="2de8e-108">The following procedure describes how to register for system registry events.</span></span>

<span data-ttu-id="2de8e-109">**註冊系統登錄事件**</span><span class="sxs-lookup"><span data-stu-id="2de8e-109">**To register for system registry events**</span></span>

1.  <span data-ttu-id="2de8e-110">呼叫通知查詢方法。</span><span class="sxs-lookup"><span data-stu-id="2de8e-110">Call a notification query method.</span></span>

    <span data-ttu-id="2de8e-111">在腳本或 c + + 中，請使用通知查詢，例如 [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) 或 [**IWbemServices：： ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-111">In either script or C++, use a notification query such as [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) or [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync).</span></span> <span data-ttu-id="2de8e-112">針對 **IWbemServices：： ExecNotificationQueryAsync** 的 *bstrQuery* 參數或腳本中的 *strQuery* 建立查詢字串。</span><span class="sxs-lookup"><span data-stu-id="2de8e-112">Create a query string for the *bstrQuery* parameter of **IWbemServices::ExecNotificationQueryAsync** or the *strQuery* in script.</span></span>

2.  <span data-ttu-id="2de8e-113">決定您想要接收的事件種類，並建立查詢。</span><span class="sxs-lookup"><span data-stu-id="2de8e-113">Determine which type of event you want to receive and create the query.</span></span>

    <span data-ttu-id="2de8e-114">下表列出您可以使用的登錄事件類別。</span><span class="sxs-lookup"><span data-stu-id="2de8e-114">The following table lists the registry event classes that you can use.</span></span>

    

    | <span data-ttu-id="2de8e-115">事件類別</span><span class="sxs-lookup"><span data-stu-id="2de8e-115">Event class</span></span>                                                      | <span data-ttu-id="2de8e-116">Hive 位置</span><span class="sxs-lookup"><span data-stu-id="2de8e-116">Hive location</span></span>        | <span data-ttu-id="2de8e-117">Description</span><span class="sxs-lookup"><span data-stu-id="2de8e-117">Description</span></span>                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [<span data-ttu-id="2de8e-118">**RegistryEvent**</span><span class="sxs-lookup"><span data-stu-id="2de8e-118">**RegistryEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryevent)                       | <span data-ttu-id="2de8e-119">N/A</span><span class="sxs-lookup"><span data-stu-id="2de8e-119">N/A</span></span><br/>       | <span data-ttu-id="2de8e-120">登錄中變更的抽象基類。</span><span class="sxs-lookup"><span data-stu-id="2de8e-120">Abstract base class for changes in the registry.</span></span><br/> |
    | [<span data-ttu-id="2de8e-121">**RegistryTreeChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="2de8e-121">**RegistryTreeChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | <span data-ttu-id="2de8e-122">RootPath</span><span class="sxs-lookup"><span data-stu-id="2de8e-122">RootPath</span></span><br/>  | <span data-ttu-id="2de8e-123">監視索引鍵階層的變更。</span><span class="sxs-lookup"><span data-stu-id="2de8e-123">Monitors changes to a hierarchy of keys.</span></span><br/>         |
    | [<span data-ttu-id="2de8e-124">**RegistryKeyChangeEvent**</span><span class="sxs-lookup"><span data-stu-id="2de8e-124">**RegistryKeyChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | <span data-ttu-id="2de8e-125">KeyPath</span><span class="sxs-lookup"><span data-stu-id="2de8e-125">KeyPath</span></span><br/>   | <span data-ttu-id="2de8e-126">監視單一金鑰的變更。</span><span class="sxs-lookup"><span data-stu-id="2de8e-126">Monitors changes to a single key.</span></span><br/>                |
    | [<span data-ttu-id="2de8e-127">**Registryvaluechangeeven**</span><span class="sxs-lookup"><span data-stu-id="2de8e-127">**RegistryValueChangeEvent**</span></span>](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | <span data-ttu-id="2de8e-128">ValueName</span><span class="sxs-lookup"><span data-stu-id="2de8e-128">ValueName</span></span><br/> | <span data-ttu-id="2de8e-129">監視單一值的變更。</span><span class="sxs-lookup"><span data-stu-id="2de8e-129">Monitors changes to a single value.</span></span><br/>              |

    

     

    <span data-ttu-id="2de8e-130">這些類別具有一個名為 **Hive** 的屬性，可識別要監視的金鑰階層（例如 **HKEY \_ 本機 \_ 電腦**）。</span><span class="sxs-lookup"><span data-stu-id="2de8e-130">These classes have a property called **Hive** that identifies the hierarchy of keys to be monitored for change, such as **HKEY\_LOCAL\_MACHINE**.</span></span>

    <span data-ttu-id="2de8e-131">**HKEY \_ 類別 \_ 根目錄** 和 **HKEY \_ 目前 \_ 使用者** hive 的變更不受 [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)或衍生自它的類別（例如 [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)）的支援。</span><span class="sxs-lookup"><span data-stu-id="2de8e-131">Changes to the **HKEY\_CLASSES\_ROOT** and **HKEY\_CURRENT\_USER** hives are not supported by [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) or classes derived from it, such as [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).</span></span>

3.  <span data-ttu-id="2de8e-132">為您的事件註冊建立 WHERE 子句。</span><span class="sxs-lookup"><span data-stu-id="2de8e-132">Create the WHERE clause for your event registration.</span></span>

    <span data-ttu-id="2de8e-133">System Registry provider 具有 WHERE 子句的特定規則。</span><span class="sxs-lookup"><span data-stu-id="2de8e-133">The System Registry provider has specific rules for WHERE clauses.</span></span> <span data-ttu-id="2de8e-134">如需詳細資訊，請參閱為登錄 [提供者建立適當的 WHERE 子句](creating-a-proper-where-clause-for-the-registry-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-134">For more information, see [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md).</span></span> <span data-ttu-id="2de8e-135">如需有關建立 WHERE 子句的一般資訊，請參閱 [使用 WQL 查詢](querying-with-wql.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-135">For more general information about creating a WHERE clause, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="2de8e-136">判斷您的取用者是否正在接收事件。</span><span class="sxs-lookup"><span data-stu-id="2de8e-136">Determine whether your consumer is receiving events.</span></span>

    <span data-ttu-id="2de8e-137">系統登錄提供者不保證會傳遞所有傳送的事件。</span><span class="sxs-lookup"><span data-stu-id="2de8e-137">The System Registry provider does not guarantee that all sent events are delivered.</span></span> <span data-ttu-id="2de8e-138">如需詳細資訊，請參閱 [接收登錄事件](receiving-registry-events.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-138">For more information, see [Receiving Registry Events](receiving-registry-events.md).</span></span>

<span data-ttu-id="2de8e-139">下列 VBScript 程式碼範例說明如何偵測 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **Microsoft** hive 或子樹中的登錄變更。</span><span class="sxs-lookup"><span data-stu-id="2de8e-139">The following VBScript code example shows how to detect a registry change in the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft** hive or subtree.</span></span> <span data-ttu-id="2de8e-140">這是一個監視腳本，基於示範目的，會在名為 Wscript.exe 的進程中執行，直到它在 **工作管理員** 中終止、WMI 已停止或作業系統重新開機。</span><span class="sxs-lookup"><span data-stu-id="2de8e-140">This is a monitoring script that, for demonstration purposes, runs in a process named Wscript.exe until it is terminated in **Task Manager**, WMI is stopped, or the operating system is rebooted.</span></span> <span data-ttu-id="2de8e-141">腳本會使用 [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)的 [*半同步*](gloss-s.md)呼叫。</span><span class="sxs-lookup"><span data-stu-id="2de8e-141">The script uses a [*semisynchronous*](gloss-s.md) call to [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md).</span></span> <span data-ttu-id="2de8e-142">如需有關半同步呼叫的詳細資訊，請參閱 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-142">For more information about semisynchronous calls, see [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



下列 VBScript 程式碼範例示範如何藉由登錄登錄提供者事件種類 [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)，來監視金鑰值的變更。 腳本會呼叫非同步方法， [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)。 <span data-ttu-id="2de8e-145">如需非同步呼叫和安全性的詳細資訊，請參閱 [使用 VBScript 進行非同步呼叫](making-an-asynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="2de8e-145">For more information about asynchronous calls and security, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

<span data-ttu-id="2de8e-146">下列腳本會無限期地執行，直到電腦重新開機、WMI 已停止或腳本停止。</span><span class="sxs-lookup"><span data-stu-id="2de8e-146">The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped.</span></span> <span data-ttu-id="2de8e-147">若要手動停止腳本，請使用工作管理員停止進程。</span><span class="sxs-lookup"><span data-stu-id="2de8e-147">To stop the script manually, use Task Manager to stop the process.</span></span> <span data-ttu-id="2de8e-148">若要以程式設計方式停止它，請在 Win32 Process 類別中使用 [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) 方法 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2de8e-148">To stop it programmatically, use the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method in the Win32\_Process class.</span></span>


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 


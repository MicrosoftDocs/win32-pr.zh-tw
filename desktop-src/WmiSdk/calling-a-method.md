---
description: WMI 提供 COM API 和腳本 API 中的方法，以取得資訊或操作企業系統中的物件。
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: 呼叫 WMI 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980713"
---
# <a name="calling-a-wmi-method"></a><span data-ttu-id="76ebc-103">呼叫 WMI 方法</span><span class="sxs-lookup"><span data-stu-id="76ebc-103">Calling a WMI Method</span></span>

<span data-ttu-id="76ebc-104">WMI 提供 [COM API](com-api-for-wmi.md) 和 [腳本 API](scripting-api-for-wmi.md) 中的方法，以取得資訊或操作企業系統中的物件。</span><span class="sxs-lookup"><span data-stu-id="76ebc-104">WMI supplies methods in the [COM API](com-api-for-wmi.md) and the [scripting API](scripting-api-for-wmi.md) to obtain information or manipulate objects in an enterprise system.</span></span> <span data-ttu-id="76ebc-105">例如，WMI 腳本方法 [**SWbemServices.ExecQuery**](swbemservices-execquery.md) 查詢資料。</span><span class="sxs-lookup"><span data-stu-id="76ebc-105">For example, the WMI scripting method [**SWbemServices.ExecQuery**](swbemservices-execquery.md) queries for data.</span></span> <span data-ttu-id="76ebc-106">提供者也有在其註冊的類別中定義的方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-106">Providers also have methods defined in the classes they register.</span></span> <span data-ttu-id="76ebc-107">範例包括 win32 [**\_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)方法 [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk)和 [Win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)所提供的 [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) 。</span><span class="sxs-lookup"><span data-stu-id="76ebc-107">Examples are the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) methods [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) and [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) supplied by the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider).</span></span>

<span data-ttu-id="76ebc-108">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="76ebc-108">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="76ebc-109">與提供者方法相較之下的 WMI 方法</span><span class="sxs-lookup"><span data-stu-id="76ebc-109">WMI Methods Compared to Provider Methods</span></span>](#wmi-methods-compared-to-provider-methods)
-   [<span data-ttu-id="76ebc-110">WMI 中的方法呼叫模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-110">Method-Calling Modes in WMI</span></span>](#method-calling-modes-in-wmi)
    -   [<span data-ttu-id="76ebc-111">同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-111">Synchronous Mode</span></span>](#synchronous-mode)
    -   [<span data-ttu-id="76ebc-112">非同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-112">Asynchronous Mode</span></span>](#asynchronous-mode)
    -   [<span data-ttu-id="76ebc-113">半同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-113">Semisynchronous Mode</span></span>](#semisynchronous-mode)
-   [<span data-ttu-id="76ebc-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="76ebc-114">Related topics</span></span>](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a><span data-ttu-id="76ebc-115">與提供者方法相較之下的 WMI 方法</span><span class="sxs-lookup"><span data-stu-id="76ebc-115">WMI Methods Compared to Provider Methods</span></span>

<span data-ttu-id="76ebc-116">藉由使用與 [*提供者方法*](gloss-p.md)呼叫結合的 [*WMI 方法*](gloss-w.md)呼叫，您可以取得和操作企業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="76ebc-116">By using [*WMI method*](gloss-w.md) calls combined with [*provider method*](gloss-p.md) calls, you can retrieve and manipulate information about your enterprise.</span></span> <span data-ttu-id="76ebc-117">如需詳細資訊，請參閱 [呼叫 WMI 方法](calling-a-wmi-method.md) 和 [呼叫提供者方法](calling-a-provider-method.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-117">For more information, see [Calling a WMI Method](calling-a-wmi-method.md) and [Calling a Provider Method](calling-a-provider-method.md).</span></span>

<span data-ttu-id="76ebc-118">WMI 腳本物件 [**SWbemObject**](swbemobject.md) 的方法具有特殊狀態，因為它們可以套用至任何 WMI 資料類別。</span><span class="sxs-lookup"><span data-stu-id="76ebc-118">The methods of the WMI scripting object [**SWbemObject**](swbemobject.md) have a special status because they can apply to any WMI data class.</span></span> <span data-ttu-id="76ebc-119">如需詳細資訊，請參閱 [使用 SWbemObject 編寫腳本](scripting-with-swbemobject.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-119">For more information, see [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

<span data-ttu-id="76ebc-120">下列程式碼範例會呼叫 WMI 和提供者方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-120">The following code example calls both WMI and provider methods.</span></span>

<span data-ttu-id="76ebc-121">下列 WMI 和提供者方法位於 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)：</span><span class="sxs-lookup"><span data-stu-id="76ebc-121">The following WMI and provider methods are located in the [Scripting API for WMI](scripting-api-for-wmi.md):</span></span>

-   <span data-ttu-id="76ebc-122">**objWMIService.ExecQuery** 會呼叫 WMI 腳本方法 [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span><span class="sxs-lookup"><span data-stu-id="76ebc-122">**objWMIService.ExecQuery** calls the WMI scripting method [**SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)</span></span>
-   <span data-ttu-id="76ebc-123">**objService. StopService ()** 會呼叫提供者方法 [ **Win32 \_ Service. StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span><span class="sxs-lookup"><span data-stu-id="76ebc-123">**objService.StopService()** calls the provider method [**Win32\_Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)</span></span>

<span data-ttu-id="76ebc-124">您可以在 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)的 [傳回碼] 區段中，查詢可能出現在 [傳回] 中的程式碼。</span><span class="sxs-lookup"><span data-stu-id="76ebc-124">You can look up the code that may appear in "Return" in the Return Codes section for [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a><span data-ttu-id="76ebc-125">WMI 中的 Method-Calling 模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-125">Method-Calling Modes in WMI</span></span>

<span data-ttu-id="76ebc-126">半同步呼叫模式通常會在安全性與效能之間提供最佳平衡。</span><span class="sxs-lookup"><span data-stu-id="76ebc-126">The semisynchronous calling mode usually provides the best balance between security and performance.</span></span>

<span data-ttu-id="76ebc-127">如需每個可能模式的詳細資訊，請參閱下列各項：</span><span class="sxs-lookup"><span data-stu-id="76ebc-127">For more information about each of the possible modes, see the following:</span></span>

-   [<span data-ttu-id="76ebc-128">同步</span><span class="sxs-lookup"><span data-stu-id="76ebc-128">Synchronous</span></span>](#synchronous-mode)
-   [<span data-ttu-id="76ebc-129">非同步</span><span class="sxs-lookup"><span data-stu-id="76ebc-129">Asynchronous</span></span>](#asynchronous-mode)
-   [<span data-ttu-id="76ebc-130">半同步</span><span class="sxs-lookup"><span data-stu-id="76ebc-130">Semisynchronous</span></span>](#semisynchronous-mode)

### <a name="synchronous-mode"></a><span data-ttu-id="76ebc-131">同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-131">Synchronous Mode</span></span>

<span data-ttu-id="76ebc-132">當程式或腳本在方法呼叫傳回 [**swbemobjectset 搭配使用**](swbemobjectset.md) 集合物件之前暫停時，就會發生同步模式。</span><span class="sxs-lookup"><span data-stu-id="76ebc-132">Synchronous mode occurs when the program or scripts pauses until the method call returns a [**SWbemObjectSet**](swbemobjectset.md) collection object.</span></span> <span data-ttu-id="76ebc-133">WMI 會在記憶體中建立此集合，然後將集合物件傳回給呼叫的程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="76ebc-133">WMI builds this collection in memory before returning the collection object to the calling program or script.</span></span>

<span data-ttu-id="76ebc-134">在執行程式或腳本的電腦上，同步模式可能會對程式或腳本效能造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="76ebc-134">Synchronous mode can have an adverse effect of program or script performance on the computer running the program or script.</span></span> <span data-ttu-id="76ebc-135">例如，從事件記錄檔同步取出上千個事件可能需要很長的時間，而且會耗用大量的記憶體，因為 WMI 會從每個事件建立一個物件，然後將這些物件放入集合，然後再將集合傳遞給方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-135">For example, synchronously retrieving thousands of events from the event log can take a long time and use a lot of memory because WMI creates an object from each event and then puts those objects into a collection before passing the collection to the method.</span></span>

<span data-ttu-id="76ebc-136">您應該只呼叫不會在同步模式中傳回大型資料集的方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-136">You should only call methods that do not return large data sets in synchronous mode.</span></span> <span data-ttu-id="76ebc-137">您可以在同步模式中安全地呼叫下列 [**SWbemServices**](swbemservices.md) 方法：</span><span class="sxs-lookup"><span data-stu-id="76ebc-137">The following [**SWbemServices**](swbemservices.md) methods can be safely called in synchronous mode:</span></span>

-   [<span data-ttu-id="76ebc-138">**SWbemServices。刪除**</span><span class="sxs-lookup"><span data-stu-id="76ebc-138">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="76ebc-139">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="76ebc-139">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="76ebc-140">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="76ebc-140">**SWbemServices.Get**</span></span>](swbemservices-get.md)

<span data-ttu-id="76ebc-141">您可以藉由在 *iFlags* 參數中設定 **wbemFlagReturnWhenComplete** 值，在名稱中使用 "Async" 這個字的任何 [**SWbemServices**](swbemservices.md)方法，都可以在同步模式中呼叫。</span><span class="sxs-lookup"><span data-stu-id="76ebc-141">Any [**SWbemServices**](swbemservices.md) methods without the word, "Async" in the name can be called in synchronous mode by setting the **wbemFlagReturnWhenComplete** value in the *iFlags* parameter.</span></span>

### <a name="asynchronous-mode"></a><span data-ttu-id="76ebc-142">非同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-142">Asynchronous Mode</span></span>

<span data-ttu-id="76ebc-143">當程式或腳本在呼叫方法之後繼續執行時，就會發生非同步模式。</span><span class="sxs-lookup"><span data-stu-id="76ebc-143">Asynchronous mode occurs when the program or script continues to run after calling the method.</span></span> <span data-ttu-id="76ebc-144">當建立每個物件時，WMI 會將所有物件從方法傳回 [**SWbemSink**](swbemsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="76ebc-144">WMI returns all objects from the method to a [**SWbemSink**](swbemsink.md) object as each object is created.</span></span> <span data-ttu-id="76ebc-145">呼叫程式或腳本必須有 **SWbemSink** 物件和 [**SWbemSink OnObjectReady**](swbemsink-onobjectready.md) 事件處理常式，才能處理傳回的物件。</span><span class="sxs-lookup"><span data-stu-id="76ebc-145">The calling program or script must have an **SWbemSink** object and an [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event handler to process the returned objects.</span></span> <span data-ttu-id="76ebc-146">如需有關為非同步模式建立事件處理常式的詳細資訊，請參閱 [接收 WMI 事件](receiving-a-wmi-event.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-146">For more information about creating an event handler for asynchronous mode, see [Receiving a WMI Event](receiving-a-wmi-event.md).</span></span>

<span data-ttu-id="76ebc-147">雖然此模式沒有同步模式的效能和資源影響，但非同步模式可能會造成嚴重的安全性風險，因為儲存在 [**SWbemSink**](swbemsink.md) 物件中的結果可能不是來自呼叫的程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="76ebc-147">While this mode does not have the performance and resource penalty of synchronous mode, asynchronous mode can create serious security risks because the results stored in the [**SWbemSink**](swbemsink.md) object may not come from the calling program or script.</span></span> <span data-ttu-id="76ebc-148">WMI 會減少 **SWbemSink** 物件的驗證層級，直到方法成功為止。</span><span class="sxs-lookup"><span data-stu-id="76ebc-148">WMI lowers the authentication level on the **SWbemSink** object until the method succeeds.</span></span> <span data-ttu-id="76ebc-149">如需如何減輕這些安全性風險的詳細資訊，請參閱 [在非同步呼叫上設定安全性](setting-security-on-an-asynchronous-call.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-149">For more information about how to mitigate these security risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="76ebc-150">以 Async 這個字附加的方法是非同步模式的方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-150">Methods appended with the word Async are methods for asynchronous mode.</span></span> <span data-ttu-id="76ebc-151">以下是非同步呼叫的方法：</span><span class="sxs-lookup"><span data-stu-id="76ebc-151">The following methods are asynchronous calls:</span></span>

-   [<span data-ttu-id="76ebc-152">**SWbemServices. AssociatorsOfAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-152">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md)
-   [<span data-ttu-id="76ebc-153">**SWbemServices. DeleteAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-153">**SWbemServices.DeleteAsync**</span></span>](swbemservices-deleteasync.md)
-   [<span data-ttu-id="76ebc-154">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-154">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
-   [<span data-ttu-id="76ebc-155">**SWbemServices.ExecNotificationQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-155">**SWbemServices.ExecNotificationQueryAsync**</span></span>](swbemservices-execnotificationqueryasync.md)
-   [<span data-ttu-id="76ebc-156">**SWbemServices.ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-156">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)
-   [<span data-ttu-id="76ebc-157">**SWbemServices. InstancesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-157">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)
-   [<span data-ttu-id="76ebc-158">**SWbemServices. ReferencesToAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-158">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="76ebc-159">**SWbemServices. SubclassesOfAsync**</span><span class="sxs-lookup"><span data-stu-id="76ebc-159">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)

<span data-ttu-id="76ebc-160">如需非同步模式的詳細資訊，請參閱：</span><span class="sxs-lookup"><span data-stu-id="76ebc-160">For more information about asynchronous mode, see:</span></span>

-   [<span data-ttu-id="76ebc-161">使用 c + + 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="76ebc-161">Making an Asynchronous Call with C++</span></span>](making-an-asynchronous-call-with-c--.md)
-   [<span data-ttu-id="76ebc-162">使用 VBScript 進行非同步呼叫</span><span class="sxs-lookup"><span data-stu-id="76ebc-162">Making an Asynchronous Call with VBScript</span></span>](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a><span data-ttu-id="76ebc-163">半同步模式</span><span class="sxs-lookup"><span data-stu-id="76ebc-163">Semisynchronous Mode</span></span>

<span data-ttu-id="76ebc-164">最半同步模式與非同步模式類似，因為程式或腳本會在呼叫方法之後繼續執行。</span><span class="sxs-lookup"><span data-stu-id="76ebc-164">Semisynchronous mode is similar to asynchronous mode in that the program or script continues to run after calling the method.</span></span> <span data-ttu-id="76ebc-165">在半同步模式中，WMI 會在您的腳本或程式繼續執行時，在背景中抓取物件。</span><span class="sxs-lookup"><span data-stu-id="76ebc-165">In semisynchronous mode, WMI retrieves the objects in the background as your script or program continues to run.</span></span> <span data-ttu-id="76ebc-166">WMI 會在建立物件之後，將傳回的每個物件傳回給呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="76ebc-166">WMI returns each object returned to the calling method right after the object is created.</span></span>

<span data-ttu-id="76ebc-167">由於 WMI 會管理物件，因此，半同步模式比非同步模式更安全。</span><span class="sxs-lookup"><span data-stu-id="76ebc-167">Because WMI manages the object, semisynchronous mode is more secure than asynchronous mode.</span></span> <span data-ttu-id="76ebc-168">但是，如果您使用的是超過1000個實例的半同步模式，實例抓取可以獨佔可用的資源，這可能會降低程式或腳本的效能，以及使用程式或腳本的電腦。</span><span class="sxs-lookup"><span data-stu-id="76ebc-168">However, if you use semisynchronous mode with more than 1,000 instances, instance retrieval can monopolize the available resources, which can degrade the performance of the program or script and the computer using the program or script.</span></span> <span data-ttu-id="76ebc-169">在釋放記憶體之前，每個物件都會佔用必要的資源。</span><span class="sxs-lookup"><span data-stu-id="76ebc-169">Each object takes up the necessary resources until the memory is released.</span></span>

<span data-ttu-id="76ebc-170">若要解決此狀況，您可以使用 *iFlags* 參數設定的 **wbemFlagForwardOnly** 和 **wbemFlagReturnImmediately** 旗標來呼叫方法，以指示 WMI 傳回順向 [**swbemobjectset 搭配使用**](swbemobjectset.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-170">To work around this condition, you can call the method with the *iFlags* parameter set with the **wbemFlagForwardOnly** and **wbemFlagReturnImmediately** flags to instruct WMI to return a forward-only [**SWbemObjectSet**](swbemobjectset.md).</span></span> <span data-ttu-id="76ebc-171">順向 **swbemobjectset 搭配使用** 可在列舉物件之後釋放記憶體，以消除大型資料集所造成的效能問題。</span><span class="sxs-lookup"><span data-stu-id="76ebc-171">A forward-only **SWbemObjectSet** eliminates the performance problem caused by a large data set by releasing the memory after the object is enumerated.</span></span>

<span data-ttu-id="76ebc-172">任何無法在同步或非同步模式中呼叫的 [**SWbemServices**](swbemservices.md) 方法，都會以半同步模式來呼叫。</span><span class="sxs-lookup"><span data-stu-id="76ebc-172">Any [**SWbemServices**](swbemservices.md) method that cannot be called in either synchronous or asynchronous mode is called in semisynchronous mode.</span></span>

<span data-ttu-id="76ebc-173">以半同步模式呼叫下列方法：</span><span class="sxs-lookup"><span data-stu-id="76ebc-173">The following methods are called in semisynchronous mode:</span></span>

-   [<span data-ttu-id="76ebc-174">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="76ebc-174">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="76ebc-175">**SWbemServices。刪除**</span><span class="sxs-lookup"><span data-stu-id="76ebc-175">**SWbemServices.Delete**</span></span>](swbemservices-delete.md)
-   [<span data-ttu-id="76ebc-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="76ebc-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
-   [<span data-ttu-id="76ebc-177">**SWbemServices.ExecNotificationQuery**</span><span class="sxs-lookup"><span data-stu-id="76ebc-177">**SWbemServices.ExecNotificationQuery**</span></span>](swbemservices-execnotificationquery.md)
-   [<span data-ttu-id="76ebc-178">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="76ebc-178">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="76ebc-179">**SWbemServices。 Get**</span><span class="sxs-lookup"><span data-stu-id="76ebc-179">**SWbemServices.Get**</span></span>](swbemservices-get.md)
-   [<span data-ttu-id="76ebc-180">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="76ebc-180">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="76ebc-181">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="76ebc-181">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="76ebc-182">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="76ebc-182">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)
-   [<span data-ttu-id="76ebc-183">**SWbemServices。 Put**</span><span class="sxs-lookup"><span data-stu-id="76ebc-183">**SWbemServices.Put**</span></span>](swbemservicesex-put.md)

<span data-ttu-id="76ebc-184">如需有關半同步處理模式的詳細資訊，請參閱使用 [c + + 進行半進行呼叫](making-a-semisynchronous-call-with-c--.md) ，並 [使用 VBScript 進行半同步呼叫](making-a-semisynchronous-call-with-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="76ebc-184">For more information about semisynchronous mode, see [Making a Semisynchronous Call with C++](making-a-semisynchronous-call-with-c--.md) and [Making a Semisynchronous Call with VBScript](making-a-semisynchronous-call-with-vbscript.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76ebc-185">相關主題</span><span class="sxs-lookup"><span data-stu-id="76ebc-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76ebc-186">改善列舉效能</span><span class="sxs-lookup"><span data-stu-id="76ebc-186">Improving Enumeration Performance</span></span>](improving-enumeration-performance.md)
</dt> <dt>

[<span data-ttu-id="76ebc-187">使用 SWbemObject 編寫腳本</span><span class="sxs-lookup"><span data-stu-id="76ebc-187">Scripting with SWbemObject</span></span>](scripting-with-swbemobject.md)
</dt> <dt>

[<span data-ttu-id="76ebc-188">**WbemFlagEnum**</span><span class="sxs-lookup"><span data-stu-id="76ebc-188">**WbemFlagEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 

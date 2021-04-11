---
description: 更新 WMI 類別實例最常見的方法，就是一次更新整個實例。
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: 更新整個實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193859"
---
# <a name="updating-an-entire-instance"></a><span data-ttu-id="e8576-103">更新整個實例</span><span class="sxs-lookup"><span data-stu-id="e8576-103">Updating an Entire Instance</span></span>

<span data-ttu-id="e8576-104">更新 WMI 類別實例最常見的方法，就是一次更新整個實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-104">The most common means of updating a WMI class instance is to update the entire instance at once.</span></span> <span data-ttu-id="e8576-105">藉由更新整個實例，WMI 不需要將實例剖析為個別的屬性，並將其傳送至您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e8576-105">By updating an entire instance, WMI does not have to parse the instance into individual properties and send them to your application.</span></span> <span data-ttu-id="e8576-106">相反地，WMI 可以直接傳送整個實例給您。</span><span class="sxs-lookup"><span data-stu-id="e8576-106">Instead, WMI can simply send you the entire instance.</span></span> <span data-ttu-id="e8576-107">當您完成時，WMI 可以將整個變更的實例複製到原始實例上。</span><span class="sxs-lookup"><span data-stu-id="e8576-107">When you finish, WMI can then copy your entire changed instance over the original instance.</span></span>

<span data-ttu-id="e8576-108">下列程式描述如何使用 PowerShell 修改或更新實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-108">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

<span data-ttu-id="e8576-109">**使用 PowerShell 修改或更新實例**</span><span class="sxs-lookup"><span data-stu-id="e8576-109">**To modify or update an instance using PowerShell**</span></span>

1.  <span data-ttu-id="e8576-110">使用 >get-wmiobject 的呼叫取出物件的本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-110">Retrieve a local copy of the object with a call to Get-WmiObject.</span></span>

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  <span data-ttu-id="e8576-111">如有必要，請使用屬性集合的呼叫來查看物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8576-111">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8576-112">雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-112">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  <span data-ttu-id="e8576-113">對本機物件屬性進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-113">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8576-114">這麼做只會變更本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-114">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8576-115">若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-115">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  <span data-ttu-id="e8576-116">使用 Put 方法的呼叫，將物件放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-116">Place the object back into the WMI repository using a call to the Put method.</span></span>

    ```PowerShell
    $mySettings.Put()
    ```

    

<span data-ttu-id="e8576-117">下列程式說明如何使用 c # 來修改或更新實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-117">The following procedure describes how to modify or update an instance using C#.</span></span>

<span data-ttu-id="e8576-118">**若要使用 c # (的) 修改或更新實例，請使用基礎結構**</span><span class="sxs-lookup"><span data-stu-id="e8576-118">**To modify or update an instance using C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="e8576-119">使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85))的呼叫來取出物件的本機複本，如抓取 [WMI 實例](retrieving-an-instance.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="e8576-119">Retrieve a local copy of the object with a call to [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), as described in [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  <span data-ttu-id="e8576-120">如有必要，請使用屬性集合的呼叫來查看物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8576-120">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8576-121">雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-121">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="e8576-122">對本機物件屬性進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-122">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8576-123">這麼做只會變更本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-123">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8576-124">若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-124">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  <span data-ttu-id="e8576-125">使用 [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85))的呼叫，將物件放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-125">Place the object back into the WMI repository using a call to [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).</span></span>

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

<span data-ttu-id="e8576-126">下列程式描述如何使用 PowerShell 修改或更新實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-126">The following procedure describes how to modify or update an instance using PowerShell.</span></span>

> [!Note]  
> <span data-ttu-id="e8576-127">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="e8576-127">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="e8576-128">**若要使用 c # (Microsoft. 管理) 來修改或更新實例**</span><span class="sxs-lookup"><span data-stu-id="e8576-128">**To modify or update an instance using C# (Microsoft.Management)**</span></span>

1.  <span data-ttu-id="e8576-129">使用 [system.management.managementobject](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get)的呼叫取出物件的本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-129">Retrieve a local copy of the object with a call to [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  <span data-ttu-id="e8576-130">如有必要，請使用屬性集合的呼叫來查看物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8576-130">If necessary, view the properties of the object with a call to the Properties collection.</span></span>

    <span data-ttu-id="e8576-131">雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-131">Although not required, you may wish to know the value of the property before you change it.</span></span>

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  <span data-ttu-id="e8576-132">對本機物件屬性進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-132">Make any changes to the local object properties.</span></span>

    <span data-ttu-id="e8576-133">這麼做只會變更本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-133">Doing so changes only the local copy.</span></span> <span data-ttu-id="e8576-134">若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-134">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  <span data-ttu-id="e8576-135">使用 [system.management.managementobject](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) 或方法的呼叫，將物件放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-135">Place the object back into the WMI repository using a call to the [ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) or method.</span></span>

    ```CSharp
    myDisk.Put();
    ```

    

<span data-ttu-id="e8576-136">下列程式描述如何使用 VBScript 修改或更新實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-136">The following procedure describes how to modify or update an instance using VBScript.</span></span>

<span data-ttu-id="e8576-137">**使用 VBScript 修改或更新實例**</span><span class="sxs-lookup"><span data-stu-id="e8576-137">**To modify or update an instance using VBScript**</span></span>

1.  <span data-ttu-id="e8576-138">使用 **GetObject** 的呼叫來取出物件的本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-138">Retrieve a local copy of the object with a call to **GetObject**.</span></span>
2.  <span data-ttu-id="e8576-139">如有必要，請使用 [**屬性 \_**](swbemobject-properties-.md)方法的呼叫來查看物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8576-139">If necessary, view the properties of the object with a call to the [**Properties\_**](swbemobject-properties-.md) method.</span></span>

    <span data-ttu-id="e8576-140">雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-140">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="e8576-141">使用 [**swbempropertyset**](swbemproperty-value.md) 方法的呼叫對物件屬性進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-141">Make any changes to the object properties with a call to the [**SWbemProperty.Value**](swbemproperty-value.md) method.</span></span>

    <span data-ttu-id="e8576-142">**Value** 方法只會變更本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-142">The **Value** method changes only the local copy.</span></span> <span data-ttu-id="e8576-143">若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-143">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="e8576-144">使用呼叫 [**\_ SWbemObject**](swbemobject-put-.md)或 [**SWbemObject PutAsync \_**](swbemobject-putasync-.md)方法，將物件放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-144">Place the object back into the WMI repository with a call the [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md) methods.</span></span>

<span data-ttu-id="e8576-145">顧名思義， [**PutAsync \_**](swbemobject-putasync-.md)更新時，會以同步方式 [**放置 \_**](swbemobject-put-.md)更新。</span><span class="sxs-lookup"><span data-stu-id="e8576-145">As the names imply, [**Put\_**](swbemobject-put-.md) updates synchronously while [**PutAsync\_**](swbemobject-putasync-.md) updates asynchronously.</span></span> <span data-ttu-id="e8576-146">這兩種方法都會使用已修改的實例複製原始實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-146">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="e8576-147">不過，若要利用非同步處理，您必須建立 [**SWbemSink**](swbemsink.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="e8576-147">However, to take advantage of asynchronous processing, you must create an [**SWbemSink**](swbemsink.md) object.</span></span> <span data-ttu-id="e8576-148">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e8576-148">For more information, see [Calling a method](calling-a-method.md).</span></span>

<span data-ttu-id="e8576-149">下列程式描述如何使用 c + + 修改或更新實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-149">The following procedure describes how to modify or update an instance using C++.</span></span>

<span data-ttu-id="e8576-150">**使用 c + + 修改或更新實例**</span><span class="sxs-lookup"><span data-stu-id="e8576-150">**To modify or update an instance using C++**</span></span>

1.  <span data-ttu-id="e8576-151">藉由呼叫 [**IWbemServices：： GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**Iwbemservices：： GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)，取出實例的本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-151">Retrieve a local copy of the instance with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>
2.  <span data-ttu-id="e8576-152">如有必要，請使用 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get)的呼叫來查看物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8576-152">If necessary, view the properties of the object with a call to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).</span></span>

    <span data-ttu-id="e8576-153">雖然並非必要，但您可能會想要知道屬性的值，然後再進行變更。</span><span class="sxs-lookup"><span data-stu-id="e8576-153">Although not required, you may wish to know the value of the property before you change it.</span></span>

3.  <span data-ttu-id="e8576-154">使用 IWbemClassObject 的呼叫對複製進行任何必要的變更 [**：:P 的內容**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)。</span><span class="sxs-lookup"><span data-stu-id="e8576-154">Make any necessary changes to the copy with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>

    <span data-ttu-id="e8576-155">**Put** 方法只會變更本機複本。</span><span class="sxs-lookup"><span data-stu-id="e8576-155">The **Put** method changes only the local copy.</span></span> <span data-ttu-id="e8576-156">若要將變更儲存至 WMI，您必須將整個複本放回 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="e8576-156">To save your changes to WMI, you must place the entire copy back into the WMI repository.</span></span>

4.  <span data-ttu-id="e8576-157">將您的複本放回 WMI 儲存機制中，並呼叫 [**iwbemservices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 或 [**IWbemServices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="e8576-157">Place your copy back into the WMI repository with a call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) methods.</span></span>

    <span data-ttu-id="e8576-158">顧名思義，在以非同步方式 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)更新時， **PutInstance** 會同步更新。</span><span class="sxs-lookup"><span data-stu-id="e8576-158">As the names imply, **PutInstance** updates synchronously while [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) updates asynchronously.</span></span> <span data-ttu-id="e8576-159">這兩種方法都會使用已修改的實例複製原始實例。</span><span class="sxs-lookup"><span data-stu-id="e8576-159">Either method copies over the original instance with your modified instance.</span></span> <span data-ttu-id="e8576-160">不過，若要利用非同步處理，您必須執行 [**IWbemObjectSink**](iwbemobjectsink.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="e8576-160">However, to take advantage of asynchronous processing, you must implement the [**IWbemObjectSink**](iwbemobjectsink.md) interface.</span></span>

    <span data-ttu-id="e8576-161">請注意，屬於類別階層的實例上的更新作業可能會因為與階層中另一個類別有關的錯誤而無法成功。</span><span class="sxs-lookup"><span data-stu-id="e8576-161">You should be aware that an update operation on an instance belonging to a class hierarchy might not succeed due to an error involving another class in the hierarchy.</span></span> <span data-ttu-id="e8576-162">WMI 會呼叫每個提供者的 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) 方法，這些提供者負責衍生原始實例之類別的類別。</span><span class="sxs-lookup"><span data-stu-id="e8576-162">WMI calls the [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method of each of the providers responsible for the classes from which the class owning the original instance derives.</span></span> <span data-ttu-id="e8576-163">如果有任何這些提供者失敗，原始的更新要求就會失敗。</span><span class="sxs-lookup"><span data-stu-id="e8576-163">If any of these providers fail, the original update request fails.</span></span> <span data-ttu-id="e8576-164">如需詳細資訊，請參閱 [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="e8576-164">For more information, see the Remarks section of [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

<span data-ttu-id="e8576-165">如需詳細資訊，請參閱 [呼叫提供者方法](calling-a-provider-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e8576-165">For more information, see [Calling a Provider Method](calling-a-provider-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="e8576-166">由於接收端的回呼可能不會與用戶端所需的驗證層級傳回，因此建議您使用 [半同步] 而非 [非同步通訊]。</span><span class="sxs-lookup"><span data-stu-id="e8576-166">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="e8576-167">如需詳細資訊，請參閱 [呼叫方法](calling-a-method.md)。</span><span class="sxs-lookup"><span data-stu-id="e8576-167">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 

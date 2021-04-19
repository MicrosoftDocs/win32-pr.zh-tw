---
description: 辨識符號是一種標記，可提供 WMI 物件、方法或屬性的詳細資訊。
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: 存取 WMI 辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978134"
---
# <a name="accessing-a-wmi-qualifier"></a><span data-ttu-id="36676-103">存取 WMI 辨識符號</span><span class="sxs-lookup"><span data-stu-id="36676-103">Accessing a WMI Qualifier</span></span>

<span data-ttu-id="36676-104">辨識符號是一種標記，可提供 WMI 物件、方法或屬性的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="36676-104">A qualifier is a tag that provides more information about a WMI object, method, or property.</span></span> <span data-ttu-id="36676-105">有時，您可能需要存取儲存在辨識符號中的資料。</span><span class="sxs-lookup"><span data-stu-id="36676-105">At times, you may need to access the data stored in a qualifier.</span></span> <span data-ttu-id="36676-106">例如，一般工作是藉由嘗試抓取該方法的已實限定詞來判斷提供者是否要 **執行** 方法。</span><span class="sxs-lookup"><span data-stu-id="36676-106">For example, a common task is to determine if a provider implements a method by attempting to retrieve the **Implemented** qualifier for that method.</span></span> <span data-ttu-id="36676-107">如需詳細資訊，請參閱 [WMI 限定詞](wmi-qualifiers.md) 和 [新增限定詞](adding-a-qualifier.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-107">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Adding a Qualifier](adding-a-qualifier.md).</span></span>

<span data-ttu-id="36676-108">您可以先抓取物件，然後檢查限定詞，如同任何其他屬性一樣，在 PowerShell 中取出 WMI 物件的限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-108">You can retrieve the qualifiers on a WMI object in PowerShell by first retrieving the object, and then examining the qualifiers as you would any other property.</span></span>

<span data-ttu-id="36676-109">**使用 PowerShell 取出辨識符號**</span><span class="sxs-lookup"><span data-stu-id="36676-109">**To retrieve a qualifier using PowerShell**</span></span>

-   <span data-ttu-id="36676-110">使用 [>get-wmiobject](https://technet.microsoft.com/library/dd315379.aspx)抓取您想要查看其辨識符號的物件，然後透過 **限定詞** 屬性存取限定詞：</span><span class="sxs-lookup"><span data-stu-id="36676-110">Retrieve the object whose qualifiers you want to view using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), and then access the qualifiers through the **Qualifiers** property:</span></span>

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    <span data-ttu-id="36676-111">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-111">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="36676-112">您可以藉由先取得物件，然後檢查限定詞是否為集合，以 c # 取出 WMI 實例上的限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-112">You can retrieve the qualifiers on a WMI instance in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

<span data-ttu-id="36676-113">**若要使用 c # 取出辨識符號 (Microsoft.System。管理)**</span><span class="sxs-lookup"><span data-stu-id="36676-113">**To retrieve a qualifier using C# (Microsoft.System.Management)**</span></span>

1.  <span data-ttu-id="36676-114">使用指定的類別名稱和命名空間來建立 CimInstance 物件，以抓取您想要查看其限定詞的類別。</span><span class="sxs-lookup"><span data-stu-id="36676-114">Retrieve the class whose qualifiers you want to view by creating a CimInstance object, using the specified class name and namespace.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    <span data-ttu-id="36676-115">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-115">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="36676-116">您可以從 [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85))、 [CimInstance. CimClass.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))CimClassProperties 的屬性限定詞，以及 [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)). CimClass 的方法限定詞取得類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-116">You can retrieve the class qualifiers from the [CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), the property qualifiers from [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85)), and the method qualifiers from [CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).</span></span>

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    <span data-ttu-id="36676-117">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-117">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="36676-118">您可以先取得物件，然後檢查限定詞是否為集合，以在 c # 中抓取 WMI 物件上的限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-118">You can retrieve the qualifiers on a WMI object in C# by first retrieving the object, and then examining the qualifiers as a collection.</span></span>

> [!Note]  
> <span data-ttu-id="36676-119">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="36676-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="36676-120">**若要使用 c # (System. 管理來取得限定詞)**</span><span class="sxs-lookup"><span data-stu-id="36676-120">**To retrieve a qualifier using C# (System.Management)**</span></span>

1.  <span data-ttu-id="36676-121">使用 [system.management.managementobject](/dotnet/api/system.management.managementobject)抓取您想要查看其限定詞的物件。</span><span class="sxs-lookup"><span data-stu-id="36676-121">Retrieve the object whose qualifiers you want to view using [ManagementObject](/dotnet/api/system.management.managementobject).</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    <span data-ttu-id="36676-122">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-122">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="36676-123">將限定詞放入 [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)，並列舉 [QualifierData](/dotnet/api/system.management.qualifierdata) 值。</span><span class="sxs-lookup"><span data-stu-id="36676-123">Place the qualifiers into a [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection), and enumerate through the [QualifierData](/dotnet/api/system.management.qualifierdata) values.</span></span>

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    <span data-ttu-id="36676-124">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-124">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

<span data-ttu-id="36676-125">下列程式描述如何使用 VBScript 取出辨識符號。</span><span class="sxs-lookup"><span data-stu-id="36676-125">The following procedure describes how to retrieve a qualifier using VBScript.</span></span>

<span data-ttu-id="36676-126">**使用 VBScript 取出辨識符號**</span><span class="sxs-lookup"><span data-stu-id="36676-126">**To retrieve a qualifier using VBScript**</span></span>

1.  <span data-ttu-id="36676-127">取得您想要查看其限定詞的物件，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="36676-127">Retrieve the object whose qualifiers you want to view, as shown in the following example:</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    <span data-ttu-id="36676-128">取得物件最常見的方式是使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 方法。</span><span class="sxs-lookup"><span data-stu-id="36676-128">The most common way to retrieve an object is by using the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method.</span></span> <span data-ttu-id="36676-129">如需詳細資訊，請參閱抓取 [WMI 實例](retrieving-an-instance.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-129">For more information, see [Retrieving a WMI Instance](retrieving-an-instance.md).</span></span>

2.  <span data-ttu-id="36676-130">透過 [**SWbemObject \_**](swbemobject-qualifiers-.md)的限定詞屬性存取物件的限定詞，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="36676-130">Access the qualifiers of the object through the [**SWbemObject.Qualifiers\_**](swbemobject-qualifiers-.md) property, as shown in the following example:</span></span>

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

<span data-ttu-id="36676-131">下列程式碼範例說明如何存取 [**Win32 \_ 處理**](/windows/desktop/CIMWin32Prov/win32-process) 程式物件上的所有限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-131">The following code example describes how to access all the qualifiers on a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object.</span></span>


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



<span data-ttu-id="36676-132">下列程式說明如何使用 c + + 來取得限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-132">The following procedure describes how to retrieve a qualifier using C++.</span></span>

<span data-ttu-id="36676-133">**使用 c + + 取出辨識符號**</span><span class="sxs-lookup"><span data-stu-id="36676-133">**To retrieve a qualifier using C++**</span></span>

1.  <span data-ttu-id="36676-134">取得您想要查看其限定詞的物件。</span><span class="sxs-lookup"><span data-stu-id="36676-134">Retrieve the object whose qualifiers you want to view.</span></span>

    <span data-ttu-id="36676-135">取得物件最常見的方式是使用 [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) 或 [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="36676-135">The most common way to retrieve an object is by using a call to [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span> <span data-ttu-id="36676-136">如需詳細資訊，請參閱抓取 [WMI 類別或實例資料](retrieving-class-or-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="36676-136">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="36676-137">藉由呼叫 [**IWbemClassObject：： GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) 或 [**IWbemClassObject：： GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) 方法，取得指定屬性的限定詞集合。</span><span class="sxs-lookup"><span data-stu-id="36676-137">Retrieve the qualifier set for a given property with a call to [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) or [**IWbemClassObject::GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) methods.</span></span>

3.  <span data-ttu-id="36676-138">透過傳回的 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 介面存取物件的限定詞。</span><span class="sxs-lookup"><span data-stu-id="36676-138">Access the qualifiers of the object through the returned [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="36676-139">範例</span><span class="sxs-lookup"><span data-stu-id="36676-139">Examples</span></span>

<span data-ttu-id="36676-140">如需有關如何抓取限定詞的詳細資訊，請參閱 TechNet 資源庫上的 [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell 程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="36676-140">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

 

 

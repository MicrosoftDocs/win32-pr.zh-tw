---
description: WMI 提供各種不同的技術，可讓您使用 Microsoft PowerShell、Visual&160，來取得和操作 WMI 類別和實例資訊 \# ;Basic 腳本撰寫版 (VBScript) 和 c + +。
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: 操作類別和實例資訊
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987774"
---
# <a name="manipulating-class-and-instance-information"></a><span data-ttu-id="0b7f0-103">操作類別和實例資訊</span><span class="sxs-lookup"><span data-stu-id="0b7f0-103">Manipulating Class and Instance Information</span></span>

<span data-ttu-id="0b7f0-104">WMI 提供各種不同的技術，可讓您使用 Microsoft PowerShell Visual Basic Scripting Edition (VBScript) 和 c + +，來取得和操作 WMI 類別和實例資訊。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-104">WMI provides a variety of techniques to retrieve and manipulate WMI class and instance information, using Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) and C++.</span></span>

<span data-ttu-id="0b7f0-105">下表列出的主題將討論取得和操作 WMI 類別和實例資訊的技術。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-105">The following table lists the topics that discuss the techniques to retrieve and manipulate WMI class and instance information.</span></span>



| <span data-ttu-id="0b7f0-106">主題</span><span class="sxs-lookup"><span data-stu-id="0b7f0-106">Topic</span></span>                                                                                  | <span data-ttu-id="0b7f0-107">描述</span><span class="sxs-lookup"><span data-stu-id="0b7f0-107">Description</span></span>                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b7f0-108">正在抓取 WMI 類別或實例資料</span><span class="sxs-lookup"><span data-stu-id="0b7f0-108">Retrieving WMI Class or Instance Data</span></span>](retrieving-class-or-instance-data.md)         | <span data-ttu-id="0b7f0-109">從 WMI 資訊儲存機制取出和設定資料。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-109">Retrieve and set data from and to the WMI information repository.</span></span>                                                                                                                 |
| [<span data-ttu-id="0b7f0-110">修改實例屬性</span><span class="sxs-lookup"><span data-stu-id="0b7f0-110">Modifying an Instance Property</span></span>](modifying-an-instance-property.md)                   | <span data-ttu-id="0b7f0-111">在實例抓取之後變更其資訊。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-111">Change the information in the instance after it is retrieved.</span></span>                                                                                                                     |
| [<span data-ttu-id="0b7f0-112">變更實例的繼承</span><span class="sxs-lookup"><span data-stu-id="0b7f0-112">Changing the Inheritance of an Instance</span></span>](changing-the-inheritance-of-an-instance.md) | <span data-ttu-id="0b7f0-113">變更實例的父類別。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-113">Change the parent class of an instance.</span></span>                                                                                                                                           |
| [<span data-ttu-id="0b7f0-114">修改方法</span><span class="sxs-lookup"><span data-stu-id="0b7f0-114">Modifying a Method</span></span>](modifying-a-method.md)                                           | <span data-ttu-id="0b7f0-115">修改實例的參數。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-115">Modify the parameters of an instance.</span></span>                                                                                                                                             |
| [<span data-ttu-id="0b7f0-116">列舉 WMI</span><span class="sxs-lookup"><span data-stu-id="0b7f0-116">Enumerating WMI</span></span>](enumerating-wmi.md)                                                 | <span data-ttu-id="0b7f0-117">列舉 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-117">Enumerate WMI objects.</span></span>                                                                                                                                                            |
| [<span data-ttu-id="0b7f0-118">查詢 WMI</span><span class="sxs-lookup"><span data-stu-id="0b7f0-118">Querying WMI</span></span>](querying-wmi.md)                                                       | <span data-ttu-id="0b7f0-119">查詢 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-119">Query WMI objects.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="0b7f0-120">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="0b7f0-120">Calling a Method</span></span>](calling-a-method.md)                                               | <span data-ttu-id="0b7f0-121">使用由 Microsoft 或其他協力廠商開發人員建立的相關方法來進一步操作 WMI 物件，否則會直接影響 WMI 物件所代表的物件。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-121">Use associated methods created by Microsoft or other third-party developers to further manipulate WMI objects, or else directly affect the object that the WMI object represents.</span></span> |
| [<span data-ttu-id="0b7f0-122">存取集合</span><span class="sxs-lookup"><span data-stu-id="0b7f0-122">Accessing a Collection</span></span>](accessing-a-collection.md)                                   | <span data-ttu-id="0b7f0-123">列舉腳本中的集合。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-123">Enumerate collections in script.</span></span>                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a><span data-ttu-id="0b7f0-124">使用 VBScript 運算元據</span><span class="sxs-lookup"><span data-stu-id="0b7f0-124">Manipulating Data Using VBScript</span></span>

<span data-ttu-id="0b7f0-125">您可以直接在 [**SWbemObject**](swbemobject.md)上使用直接存取來存取 wmi 類別或實例的 wmi 屬性，而不是透過該物件的屬性 [集合](accessing-a-collection.md) 。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-125">You can use direct access to access the WMI properties of a WMI class or instance directly on an [**SWbemObject**](swbemobject.md), rather than through the property [collection](accessing-a-collection.md) of that object.</span></span> <span data-ttu-id="0b7f0-126">您也可以使用程式設計語言的原生樣式來執行該物件的方法，而不是使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) 呼叫。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-126">You can also execute methods on that object in the native style of the programming language rather than using the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) call.</span></span> <span data-ttu-id="0b7f0-127">例如， [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)中的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法在 windows 2000 中有三個參數，但是在 windows Server 2003 中有四個參數。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-127">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method in [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) had three parameters in Windows 2000 but has four parameters in Windows Server 2003.</span></span>

<span data-ttu-id="0b7f0-128">使用直接存取時，您可以將 WMI 屬性和方法視為 [**SWbemObject**](swbemobject.md)的自動化屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-128">Using direct access, you can treat WMI properties and methods as if they were automation properties and methods of [**SWbemObject**](swbemobject.md).</span></span>

<span data-ttu-id="0b7f0-129">下列範例會顯示如何存取屬性。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-129">The following example shows how you can access a property.</span></span>


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



<span data-ttu-id="0b7f0-130">下列範例顯示當您有直接存取權時，可以如何存取屬性。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-130">The following example shows how you can access a property when you have direct access.</span></span>


```VB
VolumeName = MyDisk.VolumeName
```



<span data-ttu-id="0b7f0-131">物件的連結也是可接受的。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-131">Chaining of objects is also acceptable.</span></span>

<span data-ttu-id="0b7f0-132">下列範例示範如何存取內嵌在另一個物件中之物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-132">The following example shows how to access a property of an object that is embedded in another object.</span></span>


```VB
value = MyComputer.MyDisk.VolumeName
```



<span data-ttu-id="0b7f0-133">下列範例示範如何使用陣列注標標記法來存取屬性。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-133">The following example shows how to access a property with array subscript notation.</span></span>


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



<span data-ttu-id="0b7f0-134">下列 VBScript 程式碼範例示範如何將輸入參數的實例產生到 [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process)類別中的 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process)方法做為 [**SWbemObject**](swbemobject.md)、填入輸入屬性，然後使用 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)來執行 **create** 方法。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-134">The following VBScript code example shows how to spawn an instance of the input parameters to the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method in the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class as an [**SWbemObject**](swbemobject.md), populate the input properties, and then execute the **Create** method using [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="0b7f0-135">[**SWbemObject 方法 \_**](swbemobject-methods-.md)屬性會傳回 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)方法的 [**SWbemMethodSet**](swbemmethodset.md)集合。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-135">The [**SWbemObject.Methods\_**](swbemobject-methods-.md) property returns an [**SWbemMethodSet**](swbemmethodset.md) collection of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) methods.</span></span> <span data-ttu-id="0b7f0-136">方法集合的成員是 [**SWbemMethod**](swbemmethod.md) 物件，而 [**SWbemMethod**](swbemmethod-inparameters.md) 則會傳回 [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) 方法的輸入參數。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-136">The members of the method set are [**SWbemMethod**](swbemmethod.md) objects and [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) returns the input parameters for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method.</span></span> <span data-ttu-id="0b7f0-137">必要的 *命令列* 輸入參數設定為 "calc.exe"。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-137">The required *CommandLine* input parameter is set to "calc.exe".</span></span> <span data-ttu-id="0b7f0-138">方法接著會由 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)執行，以產生 calc.exe 的進程。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-138">The method is then executed by [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), resulting in the launch of a calc.exe process.</span></span>


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



<span data-ttu-id="0b7f0-139">下列程式碼範例示範如何使用直接存取來執行先前的作業。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-139">The following code example shows how to perform the previous operation using direct access.</span></span>


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



<span data-ttu-id="0b7f0-140">如需詳細資訊，請參閱[使用 SWbemObject](scripting-with-swbemobject.md)[呼叫提供者方法](calling-a-provider-method.md)和腳本。</span><span class="sxs-lookup"><span data-stu-id="0b7f0-140">For more information, see [Calling a Provider Method](calling-a-provider-method.md) and [Scripting with SWbemObject](scripting-with-swbemobject.md).</span></span>

 

 

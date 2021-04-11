---
description: InParameters 物件包含使用 ExecMethod 類型的呼叫時，呼叫提供者方法的參數清單。
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: 建立 InParameters 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf9a351caec1ca7af3113bead4078670c88a5f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848749"
---
# <a name="constructing-inparameters-objects"></a><span data-ttu-id="d8718-103">建立 InParameters 物件</span><span class="sxs-lookup"><span data-stu-id="d8718-103">Constructing InParameters Objects</span></span>

<span data-ttu-id="d8718-104">[**InParameters**](swbemmethod-inparameters.md)物件包含使用 **ExecMethod** 類型的呼叫時，呼叫提供者方法的參數清單。</span><span class="sxs-lookup"><span data-stu-id="d8718-104">An [**InParameters**](swbemmethod-inparameters.md) object contains the parameter list for calling provider methods when using an **ExecMethod** type of call.</span></span> <span data-ttu-id="d8718-105">[**\_SWbemObject.ExecMethod**](swbemobject-execmethod-.md)、 [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md)、 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)和 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)方法都需要 **InParameters** 物件。</span><span class="sxs-lookup"><span data-stu-id="d8718-105">The [**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods all require an **InParameters** object.</span></span>

<span data-ttu-id="d8718-106">下列程式說明如何建立 [**InParameters**](swbemmethod-inparameters.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d8718-106">The following procedure describes how to construct an [**InParameters**](swbemmethod-inparameters.md) object.</span></span>

<span data-ttu-id="d8718-107">**若要建立 *objwbemInParams* 參數**</span><span class="sxs-lookup"><span data-stu-id="d8718-107">**To construct the *objwbemInParams* parameter**</span></span>

1.  <span data-ttu-id="d8718-108">連接到 WMI。</span><span class="sxs-lookup"><span data-stu-id="d8718-108">Connect to WMI.</span></span>
2.  <span data-ttu-id="d8718-109">取得 WMI 類別的定義，以定義您想要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="d8718-109">Obtain the definition of the WMI class that defines the method you want to execute.</span></span>
3.  <span data-ttu-id="d8718-110">取得您想要執行之 WMI 類別方法特定的 [**InParameters**](swbemmethod-inparameters.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="d8718-110">Obtain an [**InParameters**](swbemmethod-inparameters.md) object specific to the WMI class method you want to execute.</span></span>

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  <span data-ttu-id="d8718-111">將實例的屬性設定為任何適當的值。</span><span class="sxs-lookup"><span data-stu-id="d8718-111">Set the properties of the instance to whatever values are appropriate.</span></span> <span data-ttu-id="d8718-112">請務必將值提供給 WMI 類別中的索引鍵屬性，其中包含您想要執行的方法。</span><span class="sxs-lookup"><span data-stu-id="d8718-112">Be sure to give values to the key properties in the WMI class that contains the method you want to execute.</span></span>

    <span data-ttu-id="d8718-113">例如，如果您想要在名為 "INST" 的 [**InParameters**](swbemmethod-inparameters.md) 實例中，將名為 myinputparam 的輸入參數設定為 "abc" 值，程式碼看起來會像這樣。</span><span class="sxs-lookup"><span data-stu-id="d8718-113">For example, if you want to set an input parameter named myinputparam to the value "abc" in an instance of [**InParameters**](swbemmethod-inparameters.md) called "INST", the code would look like this.</span></span>

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  <span data-ttu-id="d8718-114">執行方法，並取得您正在執行之方法的傳回狀態。</span><span class="sxs-lookup"><span data-stu-id="d8718-114">Execute the method and obtain the return status of the method you are executing.</span></span>

<span data-ttu-id="d8718-115">下列程式碼範例說明如何設定 [**InParameters**](swbemmethod-inparameters.md) 物件，以建立代表共用的新 WMI 物件。</span><span class="sxs-lookup"><span data-stu-id="d8718-115">The following code example illustrates setting up the [**InParameters**](swbemmethod-inparameters.md) object to create a new WMI object that represents a share.</span></span> <span data-ttu-id="d8718-116">如需 [**OutParameters**](swbemmethod-outparameters.md) 物件的詳細資訊，請參閱 [剖析 OutParameters 物件](parsing-outparameters-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="d8718-116">For more information about the [**OutParameters**](swbemmethod-outparameters.md) object, see [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="d8718-117">如果 "C：/Share" 位置有一個名為 "Share" 的資料夾，此範例會傳回成功的傳回值 (0) 。</span><span class="sxs-lookup"><span data-stu-id="d8718-117">This example returns a successful return value (0) if there is a folder named "Share" at the location "C:/Share".</span></span> <span data-ttu-id="d8718-118">此範例可讓此資料夾與其他使用者共用。</span><span class="sxs-lookup"><span data-stu-id="d8718-118">This example enables this folder to be shared with other users.</span></span>


```VB
' Connect to WMI.
Set objServices = GetObject("winmgmts:root\cimv2")

' Obtain the definition of the WMI class that defines
' the method you want to execute.
Set objShare = objServices.Get("Win32_Share")

' Obtain an InParameters object specific
' to the WMI class method you want to execute.
Set objInParam = objShare.Methods_("Create"). _
    inParameters.SpawnInstance_()

' Set the properties of the instance to whatever
' values are appropriate.
objInParam.Properties_.Item("Access") = objSecDescriptor
objInParam.Properties_.Item("Description") = _
    "New share created by WMI script"
objInParam.Properties_.Item("Name") = "share"
objInParam.Properties_.Item("Path") = "C:\share"
objInParam.Properties_.Item("Type") = 0
'optional - default is 'max allowed'
objInParam.Properties_.Item("MaximumAllowed") = 100
'optional - default is no password
objInParam.Properties_.Item("Password") = "Password"

' Execute the method and obtain the return status. 
' The OutParameters object in objOutParams
' is created by the provider. 
Set objOutParams = objShare.ExecMethod_("Create", objInParam)    
wscript.echo objOutParams.ReturnValue
```



 

 




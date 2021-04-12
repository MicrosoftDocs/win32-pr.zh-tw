---
title: 在 Visual Basic 中註冊回呼
description: 在 Visual Basic 中加入回呼，與 VBScript 中使用的方法不同。
ms.assetid: 6aebb855-cf5b-4134-b7f6-3a8b404b7ae8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa754235458820a3c16eea73eec247aed90a103f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093008"
---
# <a name="registering-a-callback-in-visual-basic"></a><span data-ttu-id="ccafb-103">在 Visual Basic 中註冊回呼</span><span class="sxs-lookup"><span data-stu-id="ccafb-103">Registering a Callback in Visual Basic</span></span>

<span data-ttu-id="ccafb-104">在 Visual Basic 中加入回呼，與 VBScript 中使用的方法不同。</span><span class="sxs-lookup"><span data-stu-id="ccafb-104">Adding a callback in Visual Basic is different from the method used in VBScript.</span></span> <span data-ttu-id="ccafb-105">VBScript 中使用的 **GetRef** 函數與 Visual Basic 中使用的函式不同。</span><span class="sxs-lookup"><span data-stu-id="ccafb-105">The **GetRef** function used in VBScript is different than the one used in Visual Basic.</span></span> <span data-ttu-id="ccafb-106">因此，開發人員必須建立以回呼函式作為預設方法的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 物件。</span><span class="sxs-lookup"><span data-stu-id="ccafb-106">Therefore, a developer must create an [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) object that has the callback function as the default method.</span></span> <span data-ttu-id="ccafb-107">本主題提供開發 Visual Basic 應用程式所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="ccafb-107">This topic provides the necessary information to develop Visual Basic applications.</span></span>

<span data-ttu-id="ccafb-108">**在應用程式中執行此回呼**</span><span class="sxs-lookup"><span data-stu-id="ccafb-108">**To implement this callback in an application**</span></span>

1.  <span data-ttu-id="ccafb-109">將參考加入至兩個物件程式庫： TLBTypes. .olb 和 VboostTypes6. .olb。</span><span class="sxs-lookup"><span data-stu-id="ccafb-109">Add references to two object libraries: TLBTypes.olb and VboostTypes6.olb.</span></span> <span data-ttu-id="ccafb-110">這些物件程式庫隨附于控制點範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="ccafb-110">These object libraries are provided with the Control Point sample code.</span></span>
2.  <span data-ttu-id="ccafb-111">新增 Cbklib 的參考。</span><span class="sxs-lookup"><span data-stu-id="ccafb-111">Add a reference to Cbklib.tlb.</span></span> <span data-ttu-id="ccafb-112">這個檔案會定義回呼函數的結構。</span><span class="sxs-lookup"><span data-stu-id="ccafb-112">This file defines the structure of the callback function.</span></span>

    <span data-ttu-id="ccafb-113">Cbklib 會使用包含在控制點範例程式碼中的 cbklib .idl 檔案來建立。</span><span class="sxs-lookup"><span data-stu-id="ccafb-113">The cbklib.tlb is created using the cbklib.idl file that is included as part of the Control Point sample code.</span></span> <span data-ttu-id="ccafb-114">建議您針對其參數結構中不同的回呼函式，變更此檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ccafb-114">It is recommended that the name of this file change for callback functions that differ in the structure of their parameters.</span></span> <span data-ttu-id="ccafb-115">這個範例會使用 MIDL 來建立類型程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="ccafb-115">This example uses MIDL to create the type library file.</span></span>

3.  <span data-ttu-id="ccafb-116">撰寫回呼函數。</span><span class="sxs-lookup"><span data-stu-id="ccafb-116">Write the callback function.</span></span> <span data-ttu-id="ccafb-117">這些參數與 [註冊回呼](registering-a-callback.md)的 VBScript 範例中的參數相同。</span><span class="sxs-lookup"><span data-stu-id="ccafb-117">The parameters are the same as in the VBScript example in [Registering a Callback](registering-a-callback.md).</span></span> <span data-ttu-id="ccafb-118">此範例會在每次事件到達時列印字串。</span><span class="sxs-lookup"><span data-stu-id="ccafb-118">This example prints a string whenever an event arrives.</span></span>
    ```VB
    Function eventHandler(ByVal callbackType As Variant, _
    ByVal svcObj As Variant, ByVal varName As Variant, _
    ByVal value As Variant) As Long

        On Error GoTo Error
        'Write some interesting code to do actual work here

        MsgBox "Event Handler Called"
        Exit Function

    Error:
        With Err
            If .Number > 0 Then
                eventHandler = .Number Or &H800A0000
            Else
                eventHandler = .Number
            End If
        End With
    End Function
    ```

    

4.  <span data-ttu-id="ccafb-119">在 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) 物件中加入回呼函式（如下列範例所示），或在另一個物件（例如 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)）中使用適當的回呼類型程式庫 (cbklib mdm.tbl.user) 。</span><span class="sxs-lookup"><span data-stu-id="ccafb-119">Add the callback function to the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object, as shown in the following example, or in another object such as [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder), using the appropriate callback type library (cbklib.tbl).</span></span>
    ```VB
    Public Sub AddCbFunction(upnpSvc As UPnPService)

        Dim X As CallbackIUnknownLib.CallBackInterface
        Dim obj As Object
        Dim ptinfo As ITypeInfo
        Dim ptcomp As ITypeComp

        With LoadTypeLibEx(App.Path & "\cbklib.tlb", _
          REGKIND_NONE).GetTypeComp
            .BindType "CallBackInterface", 0, ptinfo, ptcomp
        End With

        'NewDelegator is defined in FunctionDelegator.bas
        Set X = NewDelegator(AddressOf eventHandler) 
        Set obj = CreateStdDispatch(Nothing, ObjPtr(X), ptinfo)
        upnpSvc.AddCallback obj
    End Sub
    ```

    

<span data-ttu-id="ccafb-120">在下列範例中， [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) 物件會傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="ccafb-120">In the following example, the [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) object is passed to the function.</span></span> <span data-ttu-id="ccafb-121">回呼函數接著會加入做為參數。</span><span class="sxs-lookup"><span data-stu-id="ccafb-121">The callback function is then added as the parameter.</span></span>


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a><span data-ttu-id="ccafb-122">範例程式碼中使用的物件程式庫</span><span class="sxs-lookup"><span data-stu-id="ccafb-122">Object Libraries Used in the Sample Code</span></span>

<span data-ttu-id="ccafb-123">先前的範例和控制點範例程式碼會使用下列部分物件程式庫：</span><span class="sxs-lookup"><span data-stu-id="ccafb-123">The previous examples and the Control Point sample code use some of the following object libraries:</span></span>

1.  <span data-ttu-id="ccafb-124">TLBTypes. .olb-這個程式庫定義了範例程式碼中所使用的一些類型程式庫類型和介面。</span><span class="sxs-lookup"><span data-stu-id="ccafb-124">TLBTypes.olb — This library defines some of the type library types and interfaces that are used in the sample code.</span></span> <span data-ttu-id="ccafb-125">它會定義一些在 C 或 c + + 中已可使用的 Visual Basic （例如 [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)）中使用的函數。</span><span class="sxs-lookup"><span data-stu-id="ccafb-125">It defines some of the functions to be used in Visual Basic, such as [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex), that are already available in C or C++.</span></span>
2.  <span data-ttu-id="ccafb-126">VboostTypes6. .olb-這個程式庫會定義 TLBTypes. .olb 和 FunctionDelegator 中使用的一些基底類型。如需有關 TLBTypes 的詳細資訊，請參閱《 *Advanced Visual Basic 6：每日方案的電源技巧*》，Matthew Curland (Addison-Wesley，2000年7月，ISBN： 0-201-70712-8) 。</span><span class="sxs-lookup"><span data-stu-id="ccafb-126">VboostTypes6.olb — This library defines some base types which are used in TLBTypes.olb and FunctionDelegator.bas. Further information regarding TLBTypes can be found in the book *Advanced Visual Basic 6: Power Techniques for Everyday Programs*, by Matthew Curland (Addison-Wesley, July 2000, ISBN: 0-201-70712-8).</span></span> <span data-ttu-id="ccafb-127"> (本書籍可能無法在某些語言及國家/地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="ccafb-127">(This book may not be available in some languages and countries.)</span></span>

<span data-ttu-id="ccafb-128">控制點範例程式碼和下列程式庫與本節相關，而且是執行此回呼所需的程式庫。</span><span class="sxs-lookup"><span data-stu-id="ccafb-128">The Control Point sample code and the following libraries are related to this section and are needed to implement this callback.</span></span> <span data-ttu-id="ccafb-129">您可以使用控制點範例程式碼找到它們：</span><span class="sxs-lookup"><span data-stu-id="ccafb-129">They can be found with the Control Point sample code:</span></span>

-   <span data-ttu-id="ccafb-130">Cbklib .idl</span><span class="sxs-lookup"><span data-stu-id="ccafb-130">Cbklib.idl</span></span>
-   <span data-ttu-id="ccafb-131">Cbklib .tlb</span><span class="sxs-lookup"><span data-stu-id="ccafb-131">Cbklib.tlb</span></span>
-   <span data-ttu-id="ccafb-132">VboostTypes6. .olb</span><span class="sxs-lookup"><span data-stu-id="ccafb-132">VboostTypes6.olb</span></span>
-   <span data-ttu-id="ccafb-133">TLBTypes. .olb</span><span class="sxs-lookup"><span data-stu-id="ccafb-133">TLBTypes.olb</span></span>
-   <span data-ttu-id="ccafb-134">FunctionDelegator bas</span><span class="sxs-lookup"><span data-stu-id="ccafb-134">FunctionDelegator.bas</span></span>

 

 
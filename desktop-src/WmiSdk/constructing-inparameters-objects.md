---
description: InParameters 物件包含使用 ExecMethod 類型的呼叫時，呼叫提供者方法的參數清單。
ms.assetid: 8cc65129-1698-4ada-b493-672772c94045
ms.tgt_platform: multiple
title: 建立 InParameters 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc13a51687954331a050337fe785bab29b23ee9c72785ffde78d4f8a8e0d198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131580"
---
# <a name="constructing-inparameters-objects"></a>建立 InParameters 物件

[**InParameters**](swbemmethod-inparameters.md)物件包含使用 **ExecMethod** 類型的呼叫時，呼叫提供者方法的參數清單。 [**\_SWbemObject.ExecMethod**](swbemobject-execmethod-.md)、 [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md)、 [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)和 [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)方法都需要 **InParameters** 物件。

下列程式說明如何建立 [**InParameters**](swbemmethod-inparameters.md) 物件。

**若要建立 *objwbemInParams* 參數**

1.  連線至 WMI。
2.  取得 WMI 類別的定義，以定義您想要執行的方法。
3.  取得您想要執行之 WMI 類別方法特定的 [**InParameters**](swbemmethod-inparameters.md) 物件。

    ```VB
    Set objInParam = objShare.Methods_("Create"). _
        inParameters.SpawnInstance_()
    ```

    

4.  將實例的屬性設定為任何適當的值。 請務必將值提供給 WMI 類別中的索引鍵屬性，其中包含您想要執行的方法。

    例如，如果您想要在名為 "INST" 的 [**InParameters**](swbemmethod-inparameters.md) 實例中，將名為 myinputparam 的輸入參數設定為 "abc" 值，程式碼看起來會像這樣。

    ```VB
    INST.Properties_.Add ("myinputparam").Value = "abc".
    ```

    

5.  執行方法，並取得您正在執行之方法的傳回狀態。

下列程式碼範例說明如何設定 [**InParameters**](swbemmethod-inparameters.md) 物件，以建立代表共用的新 WMI 物件。 如需 [**OutParameters**](swbemmethod-outparameters.md) 物件的詳細資訊，請參閱 [剖析 OutParameters 物件](parsing-outparameters-objects.md)。 如果 "C：/Share" 位置有一個名為 "Share" 的資料夾，此範例會傳回成功的傳回值 (0) 。 此範例可讓此資料夾與其他使用者共用。


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



 

 




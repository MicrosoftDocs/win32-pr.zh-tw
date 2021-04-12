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
# <a name="registering-a-callback-in-visual-basic"></a>在 Visual Basic 中註冊回呼

在 Visual Basic 中加入回呼，與 VBScript 中使用的方法不同。 VBScript 中使用的 **GetRef** 函數與 Visual Basic 中使用的函式不同。 因此，開發人員必須建立以回呼函式作為預設方法的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 物件。 本主題提供開發 Visual Basic 應用程式所需的資訊。

**在應用程式中執行此回呼**

1.  將參考加入至兩個物件程式庫： TLBTypes. .olb 和 VboostTypes6. .olb。 這些物件程式庫隨附于控制點範例程式碼。
2.  新增 Cbklib 的參考。 這個檔案會定義回呼函數的結構。

    Cbklib 會使用包含在控制點範例程式碼中的 cbklib .idl 檔案來建立。 建議您針對其參數結構中不同的回呼函式，變更此檔案的名稱。 這個範例會使用 MIDL 來建立類型程式庫檔案。

3.  撰寫回呼函數。 這些參數與 [註冊回呼](registering-a-callback.md)的 VBScript 範例中的參數相同。 此範例會在每次事件到達時列印字串。
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

    

4.  在 [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) 物件中加入回呼函式（如下列範例所示），或在另一個物件（例如 [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)）中使用適當的回呼類型程式庫 (cbklib mdm.tbl.user) 。
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

    

在下列範例中， [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice) 物件會傳遞至函式。 回呼函數接著會加入做為參數。


```VB
    Dim device as UPnPDevice
    Dim svcObj as UpnPService

    ' Initialize the device using the FindByType or using other methods of finding the devices
    Set svcObj = device.Services("appropriateService")
    Call AddCbFunction(svcObj)
```



## <a name="object-libraries-used-in-the-sample-code"></a>範例程式碼中使用的物件程式庫

先前的範例和控制點範例程式碼會使用下列部分物件程式庫：

1.  TLBTypes. .olb-這個程式庫定義了範例程式碼中所使用的一些類型程式庫類型和介面。 它會定義一些在 C 或 c + + 中已可使用的 Visual Basic （例如 [**LoadTypeLibEx**](/windows/win32/api/oleauto/nf-oleauto-loadtypelibex)）中使用的函數。
2.  VboostTypes6. .olb-這個程式庫會定義 TLBTypes. .olb 和 FunctionDelegator 中使用的一些基底類型。如需有關 TLBTypes 的詳細資訊，請參閱《 *Advanced Visual Basic 6：每日方案的電源技巧*》，Matthew Curland (Addison-Wesley，2000年7月，ISBN： 0-201-70712-8) 。  (本書籍可能無法在某些語言及國家/地區使用。 ) 

控制點範例程式碼和下列程式庫與本節相關，而且是執行此回呼所需的程式庫。 您可以使用控制點範例程式碼找到它們：

-   Cbklib .idl
-   Cbklib .tlb
-   VboostTypes6. .olb
-   TLBTypes. .olb
-   FunctionDelegator bas

 

 
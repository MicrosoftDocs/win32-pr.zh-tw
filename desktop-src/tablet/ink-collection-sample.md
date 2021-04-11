---
description: 此應用程式是以 InkCollector 物件為基礎，並示範筆墨的集合。
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: 筆墨集合範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112880"
---
# <a name="ink-collection-sample"></a>筆墨集合範例

此應用程式是以 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件為基礎，並示範筆墨的集合。 應用程式會建立一個視窗、附加 InkCollector 物件給它，並提供使用者可用來變更筆墨色彩、筆墨寬度以及啟用和停用筆墨集合的功能表選項。

> [!Note]  
> 本節中所討論的版本是 Visual Basic .NET。 範例程式庫中的其他語言版本之間的概念相同。

 

## <a name="declaring-the-inkcollector"></a>宣告 InkCollector

應用程式會先匯入 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間。 然後，應用程式會宣告 `myInkCollector` ，它會保留表單的 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件。


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>設定專案

表單的 `InkCollection_Load` 方法會處理表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件。 它會建立指派給表單的 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件，以修改 InkCollector 物件的 [system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10)) 屬性，並啟用 InkCollector 物件。


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



[InkCollector](/previous-versions/ms836493(v=msdn.10))會指派給表單的視窗，方法是將表單的視窗控制碼指派給 InkCollector 物件的[handle](/previous-versions/ms836504(v=msdn.10))屬性。 將 InkCollector 物件的 [Enabled](/previous-versions/ms836503(v=msdn.10)) 屬性設定為 **TRUE**，即可開啟筆墨集合。

[InkCollector](/previous-versions/ms836493(v=msdn.10))物件的[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10))屬性會設定指派給新資料指標的預設屬性。 若要在新的資料指標上設定不同的屬性，請使用資料[指標](/previous-versions/ms839521(v=msdn.10))物件的[DrawingAttributes](/previous-versions/ms839523(v=msdn.10))屬性。 若要變更單一筆劃的繪圖屬性，請使用[筆劃](/previous-versions/ms827842(v=msdn.10))物件的[DrawingAttributes](/previous-versions/ms827846(v=msdn.10))屬性。

## <a name="changing-the-properties"></a>變更屬性

這個簡單應用程式的其餘部分是由使用者可進行之各種功能表選項的處理常式所組成。 例如，當使用者選擇將筆墨色彩變更為紅色時，從 [筆跡] 功能表中選取 [紅色]，就會在功能表的事件處理常式中，使用 [ [InkCollector](/previous-versions/ms836493(v=msdn.10)) ] 物件的 [ [system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10)) ] 屬性上的 [[色彩](/previous-versions/ms837933(v=msdn.10))] 屬性來變更色彩。


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件 `myInkCollector` 。

 

 

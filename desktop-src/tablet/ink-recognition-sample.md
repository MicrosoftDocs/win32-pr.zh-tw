---
description: 此應用程式會示範如何建立手寫辨識應用程式。Windows Vista SDK 也會在 C 和 Visual Basic .net 中提供此範例的版本 \# 。
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: 筆跡辨識範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c151c92c9f407461c34ecffb015af179e57b5c9ed4735b36f70c9a4d26c78088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935118"
---
# <a name="ink-recognition-sample"></a>筆跡辨識範例

此應用程式會示範如何建立手寫辨識應用程式。Windows Vista SDK 也會在 C 和 Visual Basic .net 中提供此範例的版本 \# 。 本主題是指 Visual Basic .net 範例，但版本之間的概念相同。

## <a name="access-the-tablet-pc-interfaces"></a>存取 Tablet PC 介面

首先，參考與 SDK 一起安裝的 Tablet PC API。


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>將 InkCollector 初始化

此範例會將程式碼加入至表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式，此處理程式會將 [InkCollector](/previous-versions/ms583683(v=vs.100))、myInkCollector 和群組方塊視窗建立關聯，並啟用 InkCollector。


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>辨識筆觸

[按鈕](/dotnet/api/system.windows.forms.button?view=netcore-3.1)物件的[Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1)事件處理常式會檢查辨識[器集合的](/previous-versions/ms828520(v=msdn.10)) [Count](/previous-versions/ms828521(v=msdn.10))屬性，以確定使用者已安裝至少一個辨識器。

文字方塊的[SelectedText](/previous-versions/windows/)屬性會設定為在[筆劃](/previous-versions/ms552701(v=vs.100))集合上使用[ToString](/previous-versions/ms827836(v=msdn.10))方法的筆劃最符合項。 辨識筆觸之後，就會將其刪除。 最後，程式碼會強制繪製區域重新繪製，並清除它以供進一步使用筆墨。


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>關閉表單

表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。

 

 

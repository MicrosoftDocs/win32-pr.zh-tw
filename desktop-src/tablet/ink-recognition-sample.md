---
description: 此應用程式會示範如何建立手寫辨識應用程式。Windows Vista SDK 也會在 C 和 Visual Basic .NET 中提供此範例的版本 \# 。
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: 筆跡辨識範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191300"
---
# <a name="ink-recognition-sample"></a><span data-ttu-id="17516-103">筆跡辨識範例</span><span class="sxs-lookup"><span data-stu-id="17516-103">Ink Recognition Sample</span></span>

<span data-ttu-id="17516-104">此應用程式會示範如何建立手寫辨識應用程式。Windows Vista SDK 也會在 C 和 Visual Basic .NET 中提供此範例的版本 \# 。</span><span class="sxs-lookup"><span data-stu-id="17516-104">This application demonstrates how you can build a handwriting recognition application.The Windows Vista SDK provides versions of this sample in C\# and Visual Basic .NET, as well.</span></span> <span data-ttu-id="17516-105">本主題是指 Visual Basic .NET 範例，但版本之間的概念相同。</span><span class="sxs-lookup"><span data-stu-id="17516-105">This topic refers to the Visual Basic .NET sample, but the concepts are the same between versions.</span></span>

## <a name="access-the-tablet-pc-interfaces"></a><span data-ttu-id="17516-106">存取 Tablet PC 介面</span><span class="sxs-lookup"><span data-stu-id="17516-106">Access the Tablet PC Interfaces</span></span>

<span data-ttu-id="17516-107">首先，參考與 SDK 一起安裝的 Tablet PC API。</span><span class="sxs-lookup"><span data-stu-id="17516-107">First, reference the Tablet PC API, which are installed with the SDK.</span></span>


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a><span data-ttu-id="17516-108">將 InkCollector 初始化</span><span class="sxs-lookup"><span data-stu-id="17516-108">Initialize the InkCollector</span></span>

<span data-ttu-id="17516-109">此範例會將程式碼加入至表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件處理常式，此處理程式會將 [InkCollector](/previous-versions/ms583683(v=vs.100))、myInkCollector 和群組方塊視窗建立關聯，並啟用 InkCollector。</span><span class="sxs-lookup"><span data-stu-id="17516-109">The sample adds code to the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler that serves to associate the [InkCollector](/previous-versions/ms583683(v=vs.100)), myInkCollector, with the group box window and enable the InkCollector.</span></span>


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



## <a name="recognize-the-strokes"></a><span data-ttu-id="17516-110">辨識筆觸</span><span class="sxs-lookup"><span data-stu-id="17516-110">Recognize the Strokes</span></span>

<span data-ttu-id="17516-111">[按鈕](/dotnet/api/system.windows.forms.button?view=netcore-3.1)物件的[Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1)事件處理常式會檢查辨識[器集合的](/previous-versions/ms828520(v=msdn.10)) [Count](/previous-versions/ms828521(v=msdn.10))屬性，以確定使用者已安裝至少一個辨識器。</span><span class="sxs-lookup"><span data-stu-id="17516-111">The [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) object's [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event handler checks to ensure that the user has at least one recognizer installed by examining the [Count](/previous-versions/ms828521(v=msdn.10)) property of the [Recognizers](/previous-versions/ms828520(v=msdn.10)) collection.</span></span>

<span data-ttu-id="17516-112">文字方塊的[SelectedText](/previous-versions/windows/)屬性會設定為在[筆劃](/previous-versions/ms552701(v=vs.100))集合上使用[ToString](/previous-versions/ms827836(v=msdn.10))方法的筆劃最符合項。</span><span class="sxs-lookup"><span data-stu-id="17516-112">The [SelectedText](/previous-versions/windows/) property of the text box is set to the best match for the strokes using the [ToString](/previous-versions/ms827836(v=msdn.10)) method on the [Strokes](/previous-versions/ms552701(v=vs.100)) collection.</span></span> <span data-ttu-id="17516-113">辨識筆觸之後，就會將其刪除。</span><span class="sxs-lookup"><span data-stu-id="17516-113">After the strokes have been recognized, they are deleted.</span></span> <span data-ttu-id="17516-114">最後，程式碼會強制繪製區域重新繪製，並清除它以供進一步使用筆墨。</span><span class="sxs-lookup"><span data-stu-id="17516-114">Finally, the code forces drawing area repaint, clearing it for further ink use.</span></span>


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



## <a name="closing-the-form"></a><span data-ttu-id="17516-115">關閉表單</span><span class="sxs-lookup"><span data-stu-id="17516-115">Closing the Form</span></span>

<span data-ttu-id="17516-116">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms583683(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="17516-116">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 

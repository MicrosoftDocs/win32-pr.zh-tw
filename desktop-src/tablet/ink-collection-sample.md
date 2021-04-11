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
# <a name="ink-collection-sample"></a><span data-ttu-id="13716-103">筆墨集合範例</span><span class="sxs-lookup"><span data-stu-id="13716-103">Ink Collection Sample</span></span>

<span data-ttu-id="13716-104">此應用程式是以 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件為基礎，並示範筆墨的集合。</span><span class="sxs-lookup"><span data-stu-id="13716-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="13716-105">應用程式會建立一個視窗、附加 InkCollector 物件給它，並提供使用者可用來變更筆墨色彩、筆墨寬度以及啟用和停用筆墨集合的功能表選項。</span><span class="sxs-lookup"><span data-stu-id="13716-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="13716-106">本節中所討論的版本是 Visual Basic .NET。</span><span class="sxs-lookup"><span data-stu-id="13716-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="13716-107">範例程式庫中的其他語言版本之間的概念相同。</span><span class="sxs-lookup"><span data-stu-id="13716-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="13716-108">宣告 InkCollector</span><span class="sxs-lookup"><span data-stu-id="13716-108">Declaring the InkCollector</span></span>

<span data-ttu-id="13716-109">應用程式會先匯入 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="13716-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="13716-110">然後，應用程式會宣告 `myInkCollector` ，它會保留表單的 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件。</span><span class="sxs-lookup"><span data-stu-id="13716-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="13716-111">設定專案</span><span class="sxs-lookup"><span data-stu-id="13716-111">Setting Things Up</span></span>

<span data-ttu-id="13716-112">表單的 `InkCollection_Load` 方法會處理表單的 [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) 事件。</span><span class="sxs-lookup"><span data-stu-id="13716-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="13716-113">它會建立指派給表單的 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件，以修改 InkCollector 物件的 [system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10)) 屬性，並啟用 InkCollector 物件。</span><span class="sxs-lookup"><span data-stu-id="13716-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


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



<span data-ttu-id="13716-114">[InkCollector](/previous-versions/ms836493(v=msdn.10))會指派給表單的視窗，方法是將表單的視窗控制碼指派給 InkCollector 物件的[handle](/previous-versions/ms836504(v=msdn.10))屬性。</span><span class="sxs-lookup"><span data-stu-id="13716-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="13716-115">將 InkCollector 物件的 [Enabled](/previous-versions/ms836503(v=msdn.10)) 屬性設定為 **TRUE**，即可開啟筆墨集合。</span><span class="sxs-lookup"><span data-stu-id="13716-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="13716-116">[InkCollector](/previous-versions/ms836493(v=msdn.10))物件的[system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10))屬性會設定指派給新資料指標的預設屬性。</span><span class="sxs-lookup"><span data-stu-id="13716-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="13716-117">若要在新的資料指標上設定不同的屬性，請使用資料[指標](/previous-versions/ms839521(v=msdn.10))物件的[DrawingAttributes](/previous-versions/ms839523(v=msdn.10))屬性。</span><span class="sxs-lookup"><span data-stu-id="13716-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="13716-118">若要變更單一筆劃的繪圖屬性，請使用[筆劃](/previous-versions/ms827842(v=msdn.10))物件的[DrawingAttributes](/previous-versions/ms827846(v=msdn.10))屬性。</span><span class="sxs-lookup"><span data-stu-id="13716-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="13716-119">變更屬性</span><span class="sxs-lookup"><span data-stu-id="13716-119">Changing the Properties</span></span>

<span data-ttu-id="13716-120">這個簡單應用程式的其餘部分是由使用者可進行之各種功能表選項的處理常式所組成。</span><span class="sxs-lookup"><span data-stu-id="13716-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="13716-121">例如，當使用者選擇將筆墨色彩變更為紅色時，從 [筆跡] 功能表中選取 [紅色]，就會在功能表的事件處理常式中，使用 [ [InkCollector](/previous-versions/ms836493(v=msdn.10)) ] 物件的 [ [system.windows.controls.inkcanvas.defaultdrawingattributes](/previous-versions/ms836500(v=msdn.10)) ] 屬性上的 [[色彩](/previous-versions/ms837933(v=msdn.10))] 屬性來變更色彩。</span><span class="sxs-lookup"><span data-stu-id="13716-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="13716-122">關閉表單</span><span class="sxs-lookup"><span data-stu-id="13716-122">Closing the Form</span></span>

<span data-ttu-id="13716-123">表單的 [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) 方法會處置 [InkCollector](/previous-versions/ms836493(v=msdn.10)) 物件 `myInkCollector` 。</span><span class="sxs-lookup"><span data-stu-id="13716-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 

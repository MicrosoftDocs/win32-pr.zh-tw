---
description: 自動宣告範例可解決保險評估者的假設案例。
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: 自動宣告表單範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319732"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="ec47c-103">自動宣告表單範例</span><span class="sxs-lookup"><span data-stu-id="ec47c-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="ec47c-104">自動宣告範例可解決保險評估者的假設案例。</span><span class="sxs-lookup"><span data-stu-id="ec47c-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="ec47c-105">評估者的工作需要他或她造訪家裡或公司的用戶端，並將其宣告資訊輸入表單中。</span><span class="sxs-lookup"><span data-stu-id="ec47c-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="ec47c-106">為了提高評估者的生產力，他的 IT 部門開發了一個 tablet 應用程式，可讓他或她透過兩個筆墨控制項快速且準確地輸入理賠資訊： [InkEdit](/previous-versions/ms835842(v=msdn.10)) 和 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="ec47c-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="ec47c-107">在此範例中，會針對每一個文字輸入欄位使用 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="ec47c-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="ec47c-108">使用者可使用畫筆，在這些欄位中輸入保險政策和車輛的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ec47c-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="ec47c-109">[InkPicture](/previous-versions/ms583740(v=vs.100))控制項是用來將筆墨新增至汽車影像，以反白顯示受損的汽車區域。</span><span class="sxs-lookup"><span data-stu-id="ec47c-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="ec47c-110">自動宣告範例適用于 C \# 和 Microsoft Visual Basic .net。</span><span class="sxs-lookup"><span data-stu-id="ec47c-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="ec47c-111">本主題說明 Visual Basic .NET。</span><span class="sxs-lookup"><span data-stu-id="ec47c-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="ec47c-112">AutoClaims 類別會定義為 system.string 的子類別 [，並](/dotnet/api/system.windows.forms.form?view=netcore-3.1) 定義一個嵌套類別來建立和管理不同類型之損毀的筆墨層。</span><span class="sxs-lookup"><span data-stu-id="ec47c-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="ec47c-113">定義四個事件處理常式來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="ec47c-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="ec47c-114">初始化表單和筆墨圖層。</span><span class="sxs-lookup"><span data-stu-id="ec47c-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="ec47c-115">重繪 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="ec47c-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="ec47c-116">透過清單方塊選取筆跡圖層。</span><span class="sxs-lookup"><span data-stu-id="ec47c-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="ec47c-117">變更筆墨圖層的可見度。</span><span class="sxs-lookup"><span data-stu-id="ec47c-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="ec47c-118">此範例的版本可在 C \# 和 Visual Basic .net 中取得。</span><span class="sxs-lookup"><span data-stu-id="ec47c-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="ec47c-119">本節中所討論的版本是 Visual Basic .NET。</span><span class="sxs-lookup"><span data-stu-id="ec47c-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="ec47c-120">版本之間的概念相同。</span><span class="sxs-lookup"><span data-stu-id="ec47c-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="ec47c-121">定義表單和筆墨圖層</span><span class="sxs-lookup"><span data-stu-id="ec47c-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="ec47c-122">您必須匯入 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間：</span><span class="sxs-lookup"><span data-stu-id="ec47c-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="ec47c-123">接下來，在 AutoClaims 類別中， `InkLayer` 會定義一個嵌套類別，並宣告四個物件的陣列 `InkLayer` 。</span><span class="sxs-lookup"><span data-stu-id="ec47c-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="ec47c-124"> (InkLayer 包含用來儲存筆墨的筆墨物件，以及用來儲存圖層 [色彩和隱藏](/dotnet/api/system.drawing.color?view=netcore-3.1)狀態 **的布林** 值。 ) 當所有筆墨圖層都隱藏時，會宣告第五個 [筆墨物件來](/previous-versions/ms583670(v=vs.100))處理 [InkPicture](/previous-versions/ms583740(v=vs.100))的筆墨。</span><span class="sxs-lookup"><span data-stu-id="ec47c-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="ec47c-125">每個圖層都有自己的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="ec47c-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="ec47c-126">宣告形式有四個不同的區域， (主體、windows、輪和車頭燈) ，因此會使用四個 InkLayer 物件。</span><span class="sxs-lookup"><span data-stu-id="ec47c-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="ec47c-127">使用者可以一次查看圖層的任何組合。</span><span class="sxs-lookup"><span data-stu-id="ec47c-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="ec47c-128">初始化表單和筆墨圖層</span><span class="sxs-lookup"><span data-stu-id="ec47c-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="ec47c-129">`Load`事件處理常式會初始化[筆墨](/previous-versions/ms583670(v=vs.100))物件和四個 `InkLayer` 物件。</span><span class="sxs-lookup"><span data-stu-id="ec47c-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="ec47c-130">然後，選取清單方塊中 (主體) 的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="ec47c-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="ec47c-131">最後，將 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項的筆墨色彩設定為目前選取的清單方塊專案。</span><span class="sxs-lookup"><span data-stu-id="ec47c-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="ec47c-132">重繪 InkPicture 控制項</span><span class="sxs-lookup"><span data-stu-id="ec47c-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="ec47c-133">在 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項的繼承 [油漆](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) 事件處理常式中，會檢查筆墨圖層以判斷哪些是隱藏的。</span><span class="sxs-lookup"><span data-stu-id="ec47c-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="ec47c-134">如果未隱藏圖層，事件程式會使用轉譯 [器屬性的](/previous-versions/ms582196(v=vs.100)) [Draw](/previous-versions/ms828488(v=msdn.10)) 方法來顯示它。</span><span class="sxs-lookup"><span data-stu-id="ec47c-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="ec47c-135">如果您在 [物件瀏覽器] 中查看，就會看到 InkPicture 轉譯器屬性已定義為「 [Microsoft ink](/previous-versions/ms828481(v=msdn.10)) 轉譯器」物件：</span><span class="sxs-lookup"><span data-stu-id="ec47c-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="ec47c-136">透過清單方塊選取筆跡圖層</span><span class="sxs-lookup"><span data-stu-id="ec47c-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="ec47c-137">當使用者在清單方塊中選取專案時， [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) 事件處理常式會先檢查選取專案是否已變更，而且 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項目前不會收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="ec47c-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="ec47c-138">然後，它會將 InkPicture 控制項的筆墨色彩設定為所選筆墨圖層的適當色彩。</span><span class="sxs-lookup"><span data-stu-id="ec47c-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="ec47c-139">此外，它也會更新 [隱藏圖層] 核取方塊，以反映選取的筆墨圖層的隱藏狀態。</span><span class="sxs-lookup"><span data-stu-id="ec47c-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="ec47c-140">最後，InkPicture 控制項的繼承 [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) 方法是用來只顯示控制項內所需的圖層。</span><span class="sxs-lookup"><span data-stu-id="ec47c-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="ec47c-141">變更筆墨圖層的可見度</span><span class="sxs-lookup"><span data-stu-id="ec47c-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="ec47c-142">`CheckedChanged`事件處理常式會先檢查選取範圍是否已變更，而且[InkPicture](/previous-versions/ms583740(v=vs.100))控制項目前不會收集筆跡。</span><span class="sxs-lookup"><span data-stu-id="ec47c-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="ec47c-143">然後，它會更新選取的筆墨圖層的隱藏狀態，並將 InkPicture 控制項的 InkEnabled 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="ec47c-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="ec47c-144">接下來，InkPicture 控制項的 InkEnabled 屬性會設定為 **FALSE** ，然後再更新其筆墨屬性。</span><span class="sxs-lookup"><span data-stu-id="ec47c-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="ec47c-145">最後，根據是否選取 [隱藏圖層] 核取方塊來啟用或停用特定車輛部分的 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項，而且 InkPicture 控制項的重新 [整理方法是](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) 用來只顯示控制項內所需的圖層。</span><span class="sxs-lookup"><span data-stu-id="ec47c-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="ec47c-146">關閉表單</span><span class="sxs-lookup"><span data-stu-id="ec47c-146">Closing the Form</span></span>

<span data-ttu-id="ec47c-147">在 Windows Form 設計工具產生的程式碼中，會在表單初始化時，將 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 和 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項加入表單的元件清單中。</span><span class="sxs-lookup"><span data-stu-id="ec47c-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="ec47c-148">當表單關閉時，會以表單的 [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) 方法處置 InkEdit 和 InkPicture 控制項，以及表單的其他元件。</span><span class="sxs-lookup"><span data-stu-id="ec47c-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="ec47c-149">表單的 Dispose 方法也會處置為表單建立的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。</span><span class="sxs-lookup"><span data-stu-id="ec47c-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec47c-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="ec47c-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ec47c-151">[Microsoft Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="ec47c-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="ec47c-152">InkPicture 控制項</span><span class="sxs-lookup"><span data-stu-id="ec47c-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="ec47c-153">InkEdit 控制項</span><span class="sxs-lookup"><span data-stu-id="ec47c-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 

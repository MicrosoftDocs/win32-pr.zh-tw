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
# <a name="auto-claims-form-sample"></a>自動宣告表單範例

自動宣告範例可解決保險評估者的假設案例。 評估者的工作需要他或她造訪家裡或公司的用戶端，並將其宣告資訊輸入表單中。 為了提高評估者的生產力，他的 IT 部門開發了一個 tablet 應用程式，可讓他或她透過兩個筆墨控制項快速且準確地輸入理賠資訊： [InkEdit](/previous-versions/ms835842(v=msdn.10)) 和 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項。

在此範例中，會針對每一個文字輸入欄位使用 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 控制項。 使用者可使用畫筆，在這些欄位中輸入保險政策和車輛的相關資訊。 [InkPicture](/previous-versions/ms583740(v=vs.100))控制項是用來將筆墨新增至汽車影像，以反白顯示受損的汽車區域。 自動宣告範例適用于 C \# 和 Microsoft Visual Basic .net。 本主題說明 Visual Basic .NET。

AutoClaims 類別會定義為 system.string 的子類別 [，並](/dotnet/api/system.windows.forms.form?view=netcore-3.1) 定義一個嵌套類別來建立和管理不同類型之損毀的筆墨層。 定義四個事件處理常式來執行下列工作：

-   初始化表單和筆墨圖層。
-   重繪 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項。
-   透過清單方塊選取筆跡圖層。
-   變更筆墨圖層的可見度。

> [!Note]  
> 此範例的版本可在 C \# 和 Visual Basic .net 中取得。 本節中所討論的版本是 Visual Basic .NET。 版本之間的概念相同。

 

## <a name="defining-the-form-and-ink-layers"></a>定義表單和筆墨圖層

您必須匯入 [Microsoft Ink](/previous-versions/ms826516(v=msdn.10)) 命名空間：


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



接下來，在 AutoClaims 類別中， `InkLayer` 會定義一個嵌套類別，並宣告四個物件的陣列 `InkLayer` 。  (InkLayer 包含用來儲存筆墨的筆墨物件，以及用來儲存圖層 [色彩和隱藏](/dotnet/api/system.drawing.color?view=netcore-3.1)狀態 **的布林** 值。 ) 當所有筆墨圖層都隱藏時，會宣告第五個 [筆墨物件來](/previous-versions/ms583670(v=vs.100))處理 [InkPicture](/previous-versions/ms583740(v=vs.100))的筆墨。


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



每個圖層都有自己的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。 宣告形式有四個不同的區域， (主體、windows、輪和車頭燈) ，因此會使用四個 InkLayer 物件。 使用者可以一次查看圖層的任何組合。

## <a name="initializing-the-form-and-ink-layers"></a>初始化表單和筆墨圖層

`Load`事件處理常式會初始化[筆墨](/previous-versions/ms583670(v=vs.100))物件和四個 `InkLayer` 物件。


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



然後，選取清單方塊中 (主體) 的第一個專案。


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



最後，將 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項的筆墨色彩設定為目前選取的清單方塊專案。


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>重繪 InkPicture 控制項

在 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項的繼承 [油漆](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) 事件處理常式中，會檢查筆墨圖層以判斷哪些是隱藏的。 如果未隱藏圖層，事件程式會使用轉譯 [器屬性的](/previous-versions/ms582196(v=vs.100)) [Draw](/previous-versions/ms828488(v=msdn.10)) 方法來顯示它。 如果您在 [物件瀏覽器] 中查看，就會看到 InkPicture 轉譯器屬性已定義為「 [Microsoft ink](/previous-versions/ms828481(v=msdn.10)) 轉譯器」物件：


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>透過清單方塊選取筆跡圖層

當使用者在清單方塊中選取專案時， [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) 事件處理常式會先檢查選取專案是否已變更，而且 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項目前不會收集筆跡。 然後，它會將 InkPicture 控制項的筆墨色彩設定為所選筆墨圖層的適當色彩。 此外，它也會更新 [隱藏圖層] 核取方塊，以反映選取的筆墨圖層的隱藏狀態。 最後，InkPicture 控制項的繼承 [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) 方法是用來只顯示控制項內所需的圖層。


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>變更筆墨圖層的可見度

`CheckedChanged`事件處理常式會先檢查選取範圍是否已變更，而且[InkPicture](/previous-versions/ms583740(v=vs.100))控制項目前不會收集筆跡。 然後，它會更新選取的筆墨圖層的隱藏狀態，並將 InkPicture 控制項的 InkEnabled 設定為 **FALSE**。

接下來，InkPicture 控制項的 InkEnabled 屬性會設定為 **FALSE** ，然後再更新其筆墨屬性。

最後，根據是否選取 [隱藏圖層] 核取方塊來啟用或停用特定車輛部分的 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項，而且 InkPicture 控制項的重新 [整理方法是](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) 用來只顯示控制項內所需的圖層。


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



## <a name="closing-the-form"></a>關閉表單

在 Windows Form 設計工具產生的程式碼中，會在表單初始化時，將 [InkEdit](/previous-versions/ms835842(v=msdn.10)) 和 [InkPicture](/previous-versions/ms583740(v=vs.100)) 控制項加入表單的元件清單中。 當表單關閉時，會以表單的 [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) 方法處置 InkEdit 和 InkPicture 控制項，以及表單的其他元件。 表單的 Dispose 方法也會處置為表單建立的 [筆墨](/previous-versions/ms583670(v=vs.100)) 物件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[InkPicture 控制項](inkpicture-control.md)
</dt> <dt>

[InkEdit 控制項](inkedit-control.md)
</dt> </dl>

 

 

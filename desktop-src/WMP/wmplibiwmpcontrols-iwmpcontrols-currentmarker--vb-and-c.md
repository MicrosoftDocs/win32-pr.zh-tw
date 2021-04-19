---
title: IWMPControls currentMarker 屬性
description: CurrentMarker 屬性會取得或設定目前的標記編號。
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- currentMarker 屬性 Windows Media Player
- currentMarker 屬性 Windows Media Player，IWMPControls 介面
- IWMPControls 介面 Windows Media Player，currentMarker 屬性
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996053"
---
# <a name="iwmpcontrolscurrentmarker-property"></a>IWMPControls：： currentMarker 屬性

**CurrentMarker** 屬性會取得或設定目前的標記編號。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a>屬性值

System.string **，這是標記編號。**

## <a name="remarks"></a>備註

設定 **currentMarker** 會導致播放從指定的標記開始。 嘗試設定 **currentMarker** 之前，請先判斷檔案是否有標記，以及它有多少使用 **IWMPMedia. markerCount**。 如果檔案沒有標記，請將 **currentMarker** 設定為任何值，但不會產生錯誤。 將 **currentMarker** 設定為大於 **markerCount** 的數位也會導致錯誤。

**CurrentMarker** 屬性一律會傳回目前的或最後一個標記，這表示實際的檔案位置可以是目前標記或下一個標記之前的位置。 標記從1開始編號，因此，如果檔案有標記，您可以將 **currentMarker** 設定為零，將檔案位置變更為零。

在目前的媒體專案設定 (使用 **AxWindowsMediaPlayer. URL** 或 **AxWindowsMediaPlayer. currentMedia**) 之前， **currentMarker** 會傳回零。

## <a name="examples"></a>範例

下列範例會使用 **currentMarker** ，從對應至清單方塊（已填入標記識別項）之 SelectedIndex 屬性的標記開始播放影片。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[**IWMPControls 介面 (VB 和 c # )**](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[**IWMPMedia. markerCount (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 






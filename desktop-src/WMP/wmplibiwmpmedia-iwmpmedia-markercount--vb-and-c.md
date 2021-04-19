---
title: IWMPMedia markerCount 屬性
description: MarkerCount 屬性會取得媒體專案中的標記數目。
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- markerCount 屬性 Windows Media Player
- markerCount 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，markerCount 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987934"
---
# <a name="iwmpmediamarkercount-property"></a>IWMPMedia：： markerCount 屬性

**MarkerCount** 屬性會取得媒體專案中的標記數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a>屬性值

為標記計數的 **system.object** 。

## <a name="remarks"></a>備註

如果檔案沒有標記，或媒體專案與 AxWindowsMediaPlayer. currentMedia 中所指定的不同，則這個屬性會傳回零。

標記數位從1開始。

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **markerCount** 來取出目前媒體專案中的標記數目。 該值接著會用來做為迴圈結構的上限，這會逐一查看標記清單以抓取每個標記名稱，並將其顯示在多行文字方塊中。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
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

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






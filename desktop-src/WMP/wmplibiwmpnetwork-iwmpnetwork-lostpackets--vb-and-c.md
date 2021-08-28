---
title: IWMPNetwork lostPackets 屬性
description: LostPackets 屬性會取得遺失的封包數目。
ms.assetid: 611218d3-c4d3-4d4e-835c-1e7a956b2718
keywords:
- lostPackets 屬性 Windows Media Player
- lostPackets 屬性 Windows Media Player，IWMPNetwork 介面
- IWMPNetwork 介面 Windows Media Player，lostPackets 屬性
topic_type:
- apiref
api_name:
- IWMPNetwork.lostPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a60c85920d647f99ed8ba8478da51183c3ba63efa733c0bc627c16b040b70965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745909"
---
# <a name="iwmpnetworklostpackets-property"></a>IWMPNetwork：： lostPackets 屬性

**LostPackets** 屬性會取得遺失的封包數目。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 lostPackets {get; set;}
```


```VB

Public ReadOnly Property lostPackets As System.Int32
```





## <a name="property-value"></a>屬性值

會遺失封包數的 **system.object** 。

## <a name="remarks"></a>備註

這個屬性只包含串流媒體封包，而且在使用 HTTP 通訊協定時，會傳回零，而這是不失真的。

封包可能因為許多原因而遺失，例如網路連線的類型和品質。

每次播放都會停止並重新啟動，這個屬性會重設為零。 如果播放暫停，則不會重設此值。 這個屬性只會在執行時間使用 **AxWindowsMediaPlayer** url 屬性來設定播放的 URL 時，才會取得有效的資訊。

## <a name="examples"></a>範例

下列程式碼範例使用 **lostPackets** 來顯示播放期間遺失的封包總數。 當使用者按一下按鈕時，此資訊就會顯示在標籤中。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void showLostPackets_Click(object sender, System.EventArgs e)
{
    lostPacketsLabel.Text = ("Packets lost: " + player.network.lostPackets.ToString());
}
```


```VB

Public Sub showLostPackets_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles showLostPackets.Click

    lostPacketsLabel.Text = (&quot;Packets lost: &quot; + player.network.lostPackets.ToString())

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

[**IWMPNetwork 介面 (VB 和 c # )**](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer (VB 和 c # )**](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> </dl>

 

 






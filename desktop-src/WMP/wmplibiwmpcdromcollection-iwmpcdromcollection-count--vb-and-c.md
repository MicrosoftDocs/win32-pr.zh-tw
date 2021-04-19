---
title: IWMPCdromCollection count 屬性
description: Count 屬性會取得系統上的可用 CD 和 DVD 光碟機數目。
ms.assetid: 1359ab7e-fbe3-461c-801b-7c986f6e5687
keywords:
- count 屬性 Windows Media Player
- count 屬性 Windows Media Player，IWMPCdromCollection 介面
- IWMPCdromCollection 介面 Windows Media Player，count 屬性
topic_type:
- apiref
api_name:
- IWMPCdromCollection.count
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2da4d4d443c730d19c791a486fed4be0241b8c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992977"
---
# <a name="iwmpcdromcollectioncount-property"></a>IWMPCdromCollection：： count 屬性

**Count** 屬性會取得系統上的可用 CD 和 DVD 光碟機數目。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 count {get; set;}
```


```VB

Public ReadOnly Property count As System.Int32
```





## <a name="property-value"></a>屬性值

是可用磁片磁碟機計數的 **system.object** 。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

DVD 磁片磁碟機的計算方式與 CD 光碟機完全一樣。 不過，Windows Media Player ActiveX 控制項只支援 Windows XP 或更新版本的 DVD 功能。 DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。

## <a name="examples"></a>範例

下列範例會使用 count 來顯示訊息方塊中可用 CD 和 DVD 光碟機的數目。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show("Number of available CD and DVD drives:  " + numDrives.ToString());
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Display the number of drives as a string.
System.Windows.Forms.MessageBox.Show(&quot;Number of available CD and DVD drives:  &quot; + numDrives.ToString())
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPCdromCollection 介面 (VB 和 c # )**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






---
title: IWMPCdrom 退出方法
description: 退出方法會從磁片磁碟機中取出 CD 或 DVD。 |IWMPCdrom 退出方法
ms.assetid: c0a69252-fd79-452c-bc61-3c3e8bcaaf48
keywords:
- 退出方法 Windows Media Player
- 退出方法 Windows Media Player，IWMPCdrom 介面
- IWMPCdrom 介面 Windows Media Player、退出方法
topic_type:
- apiref
api_name:
- IWMPCdrom.eject
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00dbdf22d8eb0ba4073a1b74c25c0d610f3091477e5921dd0856fa835a9bccc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119246758"
---
# <a name="iwmpcdromeject-method"></a>IWMPCdrom：：退出方法

**退出** 方法會從磁片磁碟機中取出 CD 或 DVD。

## <a name="syntax"></a>語法


```CSharp
public void eject();
```


```VB

Public Sub eject()
Implements IWMPCdrom.eject
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果磁片磁碟機門已開啟，這個方法會關閉門。

若要使用此方法，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用「 **退出** 」來開啟索引為零的 CD 或 DVD 光碟機的門，以回應按鈕的 Click 事件。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void ejectButton_Click(object o, System.EventArgs args)
{
    player.cdromCollection.Item(0).eject();
}
```


```VB

Public Sub ejectButton_Click(ByVal o As Object, ByVal args As System.EventArgs) Handles ejectButton.Click

    player.cdromCollection.Item(0).eject()

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

[**AxWindowsMediaPlayer. playState (VB 和 c # )**](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom 介面 (VB 和 c # )**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






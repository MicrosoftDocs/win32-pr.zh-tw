---
title: AxWindowsMediaPlayer. mediaCollection 屬性
description: MediaCollection 屬性會取得 IWMPMediaCollection 介面，以提供一種方式來組織大型的媒體專案集合。
ms.assetid: ec37e1da-a843-4b89-88fc-ec9255baa98a
keywords:
- mediaCollection 屬性 Windows Media Player
- mediaCollection 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，mediaCollection 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.mediaCollection
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ad0cc720c49926ddbd75fe71d47738a9e8af43fa97670a0b9915a50716ed0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902628"
---
# <a name="axwindowsmediaplayermediacollection-property"></a>AxWindowsMediaPlayer. mediaCollection 屬性

MediaCollection 屬性會取得 **IWMPMediaCollection** 介面，以提供一種方式來組織大型的媒體專案集合。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public IWMPMediaCollection mediaCollection {get;}
```


```VB

Public ReadOnly Property mediaCollection As IWMPMediaCollection
```





## <a name="property-value"></a>屬性值

WMPLib IWMPMediaCollection 介面，指向媒體專案的集合。

## <a name="remarks"></a>備註

若要取得這個屬性的值，需要有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection 介面 (VB 和 c # )**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB 和 c # )**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 






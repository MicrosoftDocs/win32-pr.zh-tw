---
title: AxWindowsMediaPlayer. newMedia 方法
description: NewMedia 方法會傳回新媒體專案的 IWMPMedia 介面。
ms.assetid: d10a517e-b4da-4f0b-9d51-9d387578d7dd
keywords:
- newMedia 方法 Windows Media Player
- newMedia 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，newMedia 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.newMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdde19a6cb5da5113cb580c1916052c7ae0d38756bbc120368ffdfd464105591
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618738"
---
# <a name="axwindowsmediaplayernewmedia-method"></a>AxWindowsMediaPlayer. newMedia 方法

NewMedia 方法會傳回新媒體專案的 IWMPMedia 介面。

## <a name="syntax"></a>語法


```CSharp
public IWMPMedia newMedia(
  System.String bstrURL
);
```


```VB

Public Function newMedia( _
  ByVal bstrURL As System.String _
) As IWMPMedia
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.string** ，此為用來初始化新媒體專案之數位媒體檔案的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

表示新建立之媒體專案的 WMPLib IWMPMedia 介面。

## <a name="remarks"></a>備註

*BstrURL* 參數不得為長度為零的字串 ( "" ) 或 null。

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

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 






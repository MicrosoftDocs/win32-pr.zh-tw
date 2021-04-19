---
title: IWMPClosedCaption2 getSAMIStyleName 方法
description: GetSAMIStyleName 方法會傳回目前的薩米文檔案所支援的樣式名稱。
ms.assetid: e7678ca6-f52f-45f4-bd1c-7fbcdf1cc47c
keywords:
- getSAMIStyleName 方法 Windows Media Player
- getSAMIStyleName 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMIStyleName 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMIStyleName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ceb3f598ae603d478af5cad9c78333952530a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991210"
---
# <a name="iwmpclosedcaption2getsamistylename-method"></a>IWMPClosedCaption2：： getSAMIStyleName 方法

**GetSAMIStyleName** 方法會傳回目前的薩米文檔案所支援的樣式名稱。

## <a name="syntax"></a>語法


```CSharp
public System.String getSAMIStyleName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMIStyleName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMIStyleName
```





## <a name="parameters"></a>參數

<dl> <dt>

*nIndex* \[在\]
</dt> <dd>

要抓取之樣式名稱以零為基底之索引的 **system.object。**

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是以薩米文檔案指定的樣式名稱。

## <a name="remarks"></a>備註

薩米文檔案中的樣式會依照檔案中顯示的順序編制索引，從零開始。

除非數位媒體檔案已開啟 (AxWindowsMediaPlayer，否則這個方法會傳回長度為零的字串 ( "" ) 。 openState 等於 13) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**將隱藏式輔助字幕新增至數位媒體**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**IWMPClosedCaption 介面 (VB 和 c # )**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption. SAMIStyle (VB 和 c # )**](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






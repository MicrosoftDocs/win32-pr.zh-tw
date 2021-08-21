---
title: IWMPClosedCaption2 getSAMILangName 方法
description: GetSAMILangName 方法會傳回目前的薩米文檔案所支援的語言名稱。
ms.assetid: 52aaf1cc-89ef-4c4c-af43-3f88dc4a9539
keywords:
- getSAMILangName 方法 Windows Media Player
- getSAMILangName 方法 Windows Media Player，IWMPClosedCaption2 介面
- IWMPClosedCaption2 介面 Windows Media Player，getSAMILangName 方法
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.getSAMILangName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99941c7c8c62480ea13572b22083a2d64bda9924cdf3d26200dbc9ac6ba9bdf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930301"
---
# <a name="iwmpclosedcaption2getsamilangname-method"></a>IWMPClosedCaption2：： getSAMILangName 方法

**GetSAMILangName** 方法會傳回目前的薩米文檔案所支援的語言名稱。

## <a name="syntax"></a>語法


```CSharp
public System.String getSAMILangName(
  System.Int32 nIndex
);
```


```VB

Public Function getSAMILangName( _
  ByVal nIndex As System.Int32 _
) As System.String
Implements IWMPClosedCaption2.getSAMILangName
```





## <a name="parameters"></a>參數

<dl> <dt>

*nIndex* \[在\]
</dt> <dd>

要抓取之語言名稱以零為基底之索引的 **system.object** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

**System.string** ，這是以薩米文檔案指定的語言名稱。

## <a name="remarks"></a>備註

薩米文檔案中的語言會依照檔案中顯示的順序編制索引，從零開始。

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

[**IWMPClosedCaption. SAMILang (VB 和 c # )**](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[**IWMPClosedCaption2 介面 (VB 和 c # )**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 






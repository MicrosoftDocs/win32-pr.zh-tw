---
title: 'MOM_CLOSE 訊息 (Mmsystem .h) '
description: '\_當 midi 輸出裝置關閉時，MOM 關閉訊息會傳送至 midi 輸出回呼函式。'
ms.assetid: 229b3701-16f1-4ec8-920e-cd8231561541
keywords:
- MOM_CLOSE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbabd0cae61c1b1ea3d88df3cd2e52524b779eb7cdb5ac2c1e1a371546724f44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038868"
---
# <a name="mom_close-message"></a>MOM \_ 關閉訊息

當 MIDI 輸出裝置關閉時， **MOM \_ 關閉** 訊息會傳送至 midi 輸出回呼函式。


```C++
MOM_CLOSE 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

保護請勿使用。

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

保護請勿使用。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="remarks"></a>備註

傳送此訊息之後，裝置控制碼已不再有效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Mmsystem (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MIDI 訊息](midi-messages.md)
</dt> </dl>

 

 






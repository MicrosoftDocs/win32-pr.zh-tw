---
description: RefreshDisplayType 方法會更新物件的影片格式，以符合指定的顯示。
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: 'CImageDisplay. RefreshDisplayType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9184d5e8a0e0ad6c0242ec1dc4b7590f1bc0d39a0a9cd6a09b2676563a2796e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055468"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a>CImageDisplay. RefreshDisplayType 方法

`RefreshDisplayType`方法會更新物件的影片格式，以符合指定的顯示。

## <a name="syntax"></a>語法


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*szDeviceName* 
</dt> <dd>

字串的指標，其中包含由 GDI **EnumDisplayDevices** 函式所傳回之顯示裝置的名稱。 若要使用主顯示器裝置，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回 [確定]，如果失敗，則傳回 E \_ 失敗。

## <a name="remarks"></a>備註

這個方法會將 **m \_ 顯示** 成員初始化為與指定裝置上的顯示模式相對應的影片類型。

每次收到 WM DISPLAYCHANGED 訊息時呼叫此方法 \_ ，或指定次要顯示裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 





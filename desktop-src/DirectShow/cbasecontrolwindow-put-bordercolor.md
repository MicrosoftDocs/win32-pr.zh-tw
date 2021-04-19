---
description: Put 邊框 \_ 型方法會變更框線色彩。
ms.assetid: bb19d338-7fd1-448c-be94-1c71d4a9a330
title: 'CBaseControlWindow.put_BorderColor 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54db6de704f2ee0fde1a5087e83df4b362a57959
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000814"
---
# <a name="cbasecontrolwindowput_bordercolor-method"></a>CBaseControlWindow。 put \_ 邊框方法

`put_BorderColor`方法會變更框線色彩。

## <a name="syntax"></a>語法


```C++
HRESULT put_BorderColor(
   long Color
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*色彩* 
</dt> <dd>

新的框線色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

應用程式可以建立應顯示影片的目的地矩形。 這個矩形相對於視窗的工作區。 如果這樣做 (預設為一律繪製整個視窗) ，則會在影片周圍加上框線。 這個屬性會影響框線所使用的色彩。 雖然參數指定為 **LONG** 類型，但其實是 **COLORREF** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 





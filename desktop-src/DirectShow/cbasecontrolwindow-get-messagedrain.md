---
description: Get \_ MessageDrain 方法會抓取目前的訊息清空。
ms.assetid: d679e7f7-4628-479b-b722-843cdd91ffe6
title: 'CBaseControlWindow.get_MessageDrain 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_MessageDrain
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aaf51c3f4297f238e51bbe8677303730c04b89d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001514"
---
# <a name="cbasecontrolwindowget_messagedrain-method"></a>CBaseControlWindow. 取得 \_ MessageDrain 方法

方法會抓取 `get_MessageDrain` 目前的訊息清空。

## <a name="syntax"></a>語法


```C++
HRESULT get_MessageDrain(
   OAHWND *Drain
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*清空* 
</dt> <dd>

目前視窗的指標，接收視窗訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

傳送至影片轉譯器篩選器的訊息可以張貼至另一個視窗。 使用 **CBaseControlWindow：： get \_ MessageDrain** 成員函式註冊來接收這些訊息 (的視窗) 是目前的訊息清空。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 





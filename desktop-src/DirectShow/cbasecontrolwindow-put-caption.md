---
description: Put \_ Caption 方法會設定視窗標題或標題。
ms.assetid: 6671805a-e1ef-40f1-bc3f-bf7954ff9851
title: 'CBaseControlWindow.put_Caption 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Caption
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aca8e5e7ad04acae9fab1cfe2d44f982266805e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984071"
---
# <a name="cbasecontrolwindowput_caption-method"></a>CBaseControlWindow。 put \_ Caption 方法

`put_Caption`方法會設定視窗標題或標題。

## <a name="syntax"></a>語法


```C++
HRESULT put_Caption(
   BSTR strCaption
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*strCaption* 
</dt> <dd>

新的視窗標題。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

Windows 桌上型電腦上大部分的最上層視窗都有標題 (標題) 與其相關聯。 您可以透過 [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) 介面來查詢和設定這個屬性。 只有在視窗已套用 WS 標題樣式時，才會顯示任何標題集 \_ 。 如果沒有，標題仍可 (設定，並) 抓取，但使用者看不到它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlWindow 類別**](cbasecontrolwindow.md)
</dt> </dl>

 

 





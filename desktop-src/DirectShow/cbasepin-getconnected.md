---
description: GetConnected 方法會抓取連接至此釘選的 pin。
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: 'CBasePin. GetConnected 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995942"
---
# <a name="cbasepingetconnected-method"></a>CBasePin. GetConnected 方法

方法會抓取 `GetConnected` 連接至此 pin 的 pin。

## <a name="syntax"></a>語法


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回其他釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

## <a name="remarks"></a>備註

如果未連接 pin，這個方法會傳回 **Null**。 呼叫 [**CBasePin：： IsConnected**](cbasepin-isconnected.md) 方法來判斷釘選是否已連接。

方法不會在 **IPin** 介面上呼叫 **AddRef** ，因此呼叫端不應該釋放介面。

## <a name="examples"></a>範例

因為傳回的指標上的參考計數不會遞增，所以您可以將方法呼叫串連在一起：


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



這種編碼模式非常方便;但如範例所示，當 pin 未連線時，您必須小心不要對 **Null** 指標進行取值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePin 類別**](cbasepin.md)
</dt> </dl>

 

 





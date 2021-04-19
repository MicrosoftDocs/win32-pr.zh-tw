---
description: PassNotify 方法會將品質控制訊息傳遞至適當的物件。
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: 'CBaseInputPin. PassNotify 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998392"
---
# <a name="cbaseinputpinpassnotify-method"></a>CBaseInputPin. PassNotify 方法

方法會將 `PassNotify` 品質控制訊息傳遞至適當的物件。

## <a name="syntax"></a>語法


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*問* 
</dt> <dd>

包含品質控制訊息的 [**品質**](/windows/win32/api/strmif/ns-strmif-quality)結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所列的值。



| 傳回碼                                                                                       | Description                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                                        |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到接受訊息的物件。<br/> |



 

## <a name="remarks"></a>備註

如果篩選器不會處理品質控制訊息，請呼叫這個方法。 這個方法會依照喜好設定，將訊息傳遞至下列其中一個物件：

-   外部品質控制管理員（如果呼叫 [**IQualityControl：： SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) 方法）。
-   上游輸出圖釘。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseInputPin 類別**](cbaseinputpin.md)
</dt> <dt>

[品質控制管理](quality-control-management.md)
</dt> </dl>

 

 





---
description: Skip 方法會略過列舉順序中指定的 pin 數目。 這個方法會實 IEnumPins：： Skip 方法。
ms.assetid: d42f958c-f488-4730-ab84-fc4e4150b186
title: 'CEnumPins. Skip 方法 (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.Skip
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02a499c38564fba4671e5c6dbf53bc59dcf9a1acd925f9cef4d558456b675efd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119389638"
---
# <a name="cenumpinsskip-method"></a>CEnumPins. Skip 方法

`Skip`方法會在列舉順序中略過指定數目的釘選。 這個方法會實 [**IEnumPins：： Skip**](/windows/desktop/api/Strmif/nf-strmif-ienumpins-skip) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
   ULONG cPins
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*cPins* 
</dt> <dd>

要略過的 pin 數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                                | 描述                                                                            |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | 略過序列結尾的尾端。<br/>                                       |
| <dl> <dt>**S \_ 確定**</dt> </dl>                       | 成功。<br/>                                                                    |
| <dl> <dt>**VFW \_ E \_ 列舉 \_ 不 \_ \_ 同步**</dt> </dl> | 篩選的狀態已變更，且現在與列舉值不一致。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CEnumPins 類別**](cenumpins.md)
</dt> </dl>

 

 





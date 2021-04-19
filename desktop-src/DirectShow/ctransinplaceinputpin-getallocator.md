---
description: GetAllocator 方法會抓取此 pin 提議的記憶體配置器。 這個方法會實 IMemInputPin：： GetAllocator 方法。
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: 'CTransInPlaceInputPin. GetAllocator 方法 (Transip .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993278"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>CTransInPlaceInputPin. GetAllocator 方法

方法會抓取 `GetAllocator` 此 pin 提議的記憶體配置器。 這個方法會實 [**IMemInputPin：： GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppAllocator* 
</dt> <dd>

接收配置器之 [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                          | Description                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                 | 成功。<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO 配置器 \_**</dt> </dl> | 沒有配置器可供使用。<br/> |



 

## <a name="remarks"></a>備註

如果篩選的輸出釘選連線，此方法會向下游篩選器的輸入 pin 要求配置器。

如果篩選的輸出針腳未連接，這個方法會建立暫存配置器。 稍後，當輸出連接時，篩選器會重新連接輸入 pin，並重新協商配置器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transip (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CTransInPlaceInputPin 類別**](ctransinplaceinputpin.md)
</dt> </dl>

 

 





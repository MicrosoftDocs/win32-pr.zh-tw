---
description: CBaseFilter. FindPin 方法-FindPin 方法會以指定的識別碼抓取 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: 152e4ff3-2809-4c57-b9c8-f51fc50b3703
title: 'CBaseFilter. FindPin 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3818ef4356f11a2d003abe4e9442c4de06108aa32e50f480a3d097ea5db0c343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017186"
---
# <a name="cbasefilterfindpin-method"></a>CBaseFilter. FindPin 方法

`FindPin`方法會使用指定的識別碼抓取 pin。 這個方法會實 [**IBaseFilter：： FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

常數、以 null 終止的 Unicode 字串的指標，可識別 pin。

</dd> <dt>

*ppPin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面指標的變數位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | 描述                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                       |
| <dl> <dt>**E \_ 指標**</dt> </dl>         | **Null** 指標引數。<br/>     |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到相符的 pin。<br/> |



 

## <a name="remarks"></a>備註

這個方法會呼叫 [**CBasePin：： Name**](cbasepin-name.md) 方法，以根據 *Id* 參數所指定的字串來比較每個 pin 的名稱。

如果方法成功，則 **IPin** 介面具有未處理的參考計數。 當您完成時，請務必放開。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 





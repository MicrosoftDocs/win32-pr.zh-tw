---
description: QueryId 方法會抓取 pin 識別碼。 這個方法會覆寫 CBasePin：： QueryId 方法。
ms.assetid: 9543234c-5349-49d0-b410-1c461ee4eabe
title: 'CRendererInputPin. QueryId 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 732bf7aa6d0d247c93c0334db48b86bccd2ac15715dd2da9a4d60a0d315966bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054569"
---
# <a name="crendererinputpinqueryid-method"></a>CRendererInputPin. QueryId 方法

方法會抓取 `QueryId` pin 識別碼。 這個方法會覆寫 [**CBasePin：： QueryId**](cbasepin-queryid.md) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT QueryId(
   LPWSTR *Id
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

接收包含 pin 識別碼的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                   | 描述                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

這個方法會配置 "In" 的寬字元字串，並將它指派給 *Id* 參數。 呼叫端必須使用 **CoTaskMemFree** 函式釋放已配置的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRendererInputPin 類別**](crendererinputpin.md)
</dt> </dl>

 

 





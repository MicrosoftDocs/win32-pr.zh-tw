---
description: CTransformOutputPin. QueryId 方法-QueryId 方法會抓取 pin 的識別碼。 這個方法會實 IPin：： QueryId 方法。
ms.assetid: 3d83db3a-b919-454d-a91a-91f33a952a22
title: 'CTransformOutputPin. QueryId 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4c2d222ca4dd184adfe41f9f610b10f15ee9f02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094846"
---
# <a name="ctransformoutputpinqueryid-method"></a>CTransformOutputPin. QueryId 方法

方法會抓取 `QueryId` pin 的識別碼。 這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。

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



| 傳回碼                                                                                   | Description                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | Success<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數<br/> |



 

## <a name="remarks"></a>備註

Pin 識別碼會用於圖形持續性。 此類別的 pin 識別碼為 Out。這個類別會覆寫 [**CBasePin**](cbasepin.md) 類別的行為。 在 **CBasePin** 類別中，pin 識別碼與在類別的函式中指定的 pin 碼名稱相同。 在 **CTransformInputPin** 類別中，pin 識別碼和 pin 名稱不相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Transfrm (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 





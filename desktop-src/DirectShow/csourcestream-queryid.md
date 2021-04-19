---
description: QueryId 方法會抓取 pin 的識別碼。
ms.assetid: 6050292e-6203-4a79-87bf-47394624cb32
title: 'CSourceStream. QueryId 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.QueryId
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 267748fe4ce1eeec4650544a2f72069df897a366
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995386"
---
# <a name="csourcestreamqueryid-method"></a>CSourceStream. QueryId 方法

方法會抓取 `QueryId` pin 的識別碼。

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

變數的指標，此變數會接收包含 pin 識別碼的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                                       | Description                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | 記憶體不足。<br/>             |
| <dl> <dt>**E \_ 指標**</dt> </dl>         | **Null** 指標引數。<br/>       |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 在篩選準則中找不到 Pin。<br/> |



 

## <a name="remarks"></a>備註

這個方法會實 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid) 方法。 為了建立識別碼字串，pin 會呼叫 [**CSource：： FindPinNumber**](csource-findpinnumber.md) 方法，並以其本身做為參數。 **FindPinNumber** 方法會傳回從零開始編制索引的 pin 碼。 `QueryId` 將傳回值遞增1，並將結果轉換成字串。 例如，第一個 pin 變成 "1";第二個 pin 會變成 "2";等等。

如果這個方法傳回 VFW \_ E 找 \_ 不到 \_ ，則表示篩選的釘選陣列無效，可能是因為篩選器中的錯誤所造成。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 





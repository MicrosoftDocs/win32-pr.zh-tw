---
description: CSource. FindPin 方法-FindPin 方法會以指定的識別碼抓取 pin。 這個方法會實 IBaseFilter：： FindPin 方法。
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: 'CSource. FindPin 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098856"
---
# <a name="csourcefindpin-method"></a>CSource. FindPin 方法

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

識別 pin 之以 null 結束的字串指標。

</dd> <dt>

*ppPin* 
</dt> <dd>

接收釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。 如果方法失敗， \* *ppPin* 會設為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下表所示的其中一個 **HRESULT** 值。



| 傳回碼                                                                                       | Description                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>              | 成功。<br/>                                   |
| <dl> <dt>**E \_ 指標**</dt> </dl>         | **Null** 指標引數。<br/>                 |
| <dl> <dt>**\_ \_ 找不到 VFW E \_**</dt> </dl> | 找不到具有此識別碼的 pin。<br/> |



 

## <a name="remarks"></a>備註

第一個 pin 一律名為 "1";第二個 pin 名為 "2";等等。 如需詳細資訊，請參閱 [**CSourceStream：： QueryId**](csourcestream-queryid.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSource 類別**](csource.md)
</dt> </dl>

 

 





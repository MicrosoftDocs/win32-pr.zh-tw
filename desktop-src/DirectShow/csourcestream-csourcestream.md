---
description: CSourceStream。 CSourceStream 函式-函數方法。
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: CSourceStream)  (Source .h 的函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75d94bb89ca109c2a7974c294153d46235f92f23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085186"
---
# <a name="csourcestreamcsourcestream-constructor"></a>CSourceStream. CSourceStream 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pObjectName* 
</dt> <dd>

字串的指標，其中包含釘選的偵錯工具名稱。

</dd> <dt>

*phr* 
</dt> <dd>

變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。 在建立物件之前，將值初始化為「 \_ 確定」。 只有在發生錯誤時，才會變更此值。

</dd> <dt>

*Pms* 
</dt> <dd>

建立此釘選的 [**CSource**](csource.md) 篩選指標。

</dd> <dt>

*pName* 
</dt> <dd>

包含釘選名稱之字串的指標。

</dd> </dl>

## <a name="remarks"></a>備註

*PObjectName* 參數中提供的字串僅供進行偵錯工具之用。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

*PName* 參數中提供的字串是 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)方法所傳回的名稱。 `CSourceStream`此類別不會將此名稱用於 [**CSourceStream：： QueryId**](csourcestream-queryid.md)方法所傳回的 pin 識別碼。 相反地， **QueryId** 會根據 pin 碼來計算 pin 識別碼。  (Pin 識別碼支援圖形持續性。 如需詳細資訊，請參閱 [**IPin：： QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)。 ) 

此函式會藉由呼叫 [**CSource：： AddPin**](csource-addpin.md)，自動將釘選新增至擁有篩選準則。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 





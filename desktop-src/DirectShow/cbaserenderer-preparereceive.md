---
description: PrepareReceive 方法會準備篩選以轉譯範例。
ms.assetid: 873b6b3b-623e-4cec-91ea-fa628618348d
title: 'CBaseRenderer. PrepareReceive 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareReceive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b15f2a83d8cb20f7204e58dd12d5f94491904c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991025"
---
# <a name="cbaserendererpreparereceive-method"></a>CBaseRenderer. PrepareReceive 方法

`PrepareReceive`方法會準備篩選以呈現範例。

## <a name="syntax"></a>語法


```C++
virtual HRESULT PrepareReceive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMediaSample* 
</dt> <dd>

範例 [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                                             | Description                                |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                        |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                  | 失敗。<br/>                         |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>            | 非預期的錯誤。<br/>               |
| <dl> <dt>**已 \_ 拒絕 VFW 電子 \_ 範例 \_**</dt> </dl> | 篩選器正在卸載此範例。<br/> |



 

## <a name="remarks"></a>備註

篩選會在呈現範例之前，從 [**CBaseRenderer：： Receive**](cbaserenderer-receive.md) 方法內呼叫這個方法。 如果篩選器正在執行，這個方法會排程轉譯的範例。

如果篩選已經有暫止的範例，或已到達資料流程結尾，則方法會傳回 E 非 \_ 預期的。 上游篩選器可能未正確地序列化其串流呼叫。

如果排程演算法判斷應該卸載範例 (請參閱 [**CBaseRenderer：： ScheduleSample**](cbaserenderer-schedulesample.md)) ，方法會傳回已拒絕的 VFW \_ E \_ 範例 \_ 。 但是，輸入 pin 的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法不會將此錯誤碼傳遞給上游篩選器，因為卸載範例並不是錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 





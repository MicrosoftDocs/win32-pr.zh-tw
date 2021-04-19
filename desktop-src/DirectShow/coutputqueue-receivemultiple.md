---
description: ReceiveMultiple 方法會將一批媒體範例傳遞給輸入圖釘。
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: 'COutputQueue. ReceiveMultiple 方法 (Outputq .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982077"
---
# <a name="coutputqueuereceivemultiple-method"></a>COutputQueue. ReceiveMultiple 方法

方法會將 `ReceiveMultiple` 一批媒體範例傳遞給輸入圖釘。

## <a name="syntax"></a>語法


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppSamples* 
</dt> <dd>

範例陣列的指標位址。

</dd> <dt>

*nSamples* 
</dt> <dd>

陣列中的樣本數目。

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

變數的指標，此變數會接收成功傳遞的樣本數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | Description                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 在處理這個範例之前，收到的資料流程結束通知。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                                           |



 

## <a name="remarks"></a>備註

如果物件使用執行緒，這個方法會將陣列中傳遞的所有範例排入佇列。 否則，方法會在輸入釘選上呼叫 [**IMemInputPin：： ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Outputq (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COutputQueue 類別**](coutputqueue.md)
</dt> </dl>

 

 





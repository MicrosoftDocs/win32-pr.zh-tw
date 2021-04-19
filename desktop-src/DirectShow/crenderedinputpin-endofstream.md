---
description: 在將新的 run 命令發出至篩選器之前，EndOfStream 方法會通知 pin 不需要其他資料。 這個方法會實 IPin：： EndOfStream 方法。
ms.assetid: 915beab4-2fc3-4acd-bb30-c0851df058db
title: 'CRenderedInputPin. EndOfStream 方法 (Amextra .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c836b1098c92a69fa720fb7b87e4a63b3c05a526
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978759"
---
# <a name="crenderedinputpinendofstream-method"></a>CRenderedInputPin. EndOfStream 方法

在將 `EndOfStream` 新的 run 命令發出至篩選器之前，方法會通知 pin 不需要其他資料。 這個方法會實 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) 方法。

## <a name="syntax"></a>語法


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則傳回錯誤碼。

## <a name="remarks"></a>備註

如果篩選器正在執行，這個方法會將 [**EC \_ 完成**](ec-complete.md) 事件傳送至篩選圖形管理員。 否則，會設定旗標，以便在 \_ 下次執行篩選時傳送 EC 完成事件。 清除篩選器會清除旗標。

您應覆寫此方法以保存釘選的串流鎖定：


```C++
class CMyInputPin : public CRenderedInputPin
{
private:
    CCritSec * const m_pReceiveLock; // Streaming lock.
public:
    STDMETHODIMP EndOfStream(void);

    /* (Remainder of the class declaration not shown.) */
};

STDMETHODIMP CMyInputPin::EndOfStream(void)
{
    CAutoLock lock(m_pReceiveLock);  
    return CRenderedInputPin::EndOfStream();
} 
```



此外，如果篩選器以非同步方式處理 **接收** 呼叫，則在 \_ 篩選處理所有暫止的範例之前，釘選應該等候傳送 EC 完成事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amextra (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRenderedInputPin 類別**](crenderedinputpin.md)
</dt> </dl>

 

 





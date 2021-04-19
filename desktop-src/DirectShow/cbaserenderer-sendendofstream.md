---
description: 如果已到達資料流程結尾，SendEndOfStream 方法會 \_ 為篩選圖形管理員排程 EC 完成事件。
ms.assetid: 3c10c956-e352-4796-a8cd-cc69a02066f2
title: 'CBaseRenderer. SendEndOfStream 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f04e4c8c90796aafb64870a9d59d38b0a33e7435
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998760"
---
# <a name="cbaserenderersendendofstream-method"></a>CBaseRenderer. SendEndOfStream 方法

如果已到達資料流程結尾，則方法會排程 `SendEndOfStream` \_ 篩選圖形管理員的 EC 完成事件。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SendEndOfStream();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                             | Description                                                               |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 篩選圖形管理員不接受事件通知。<br/> |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                                       |



 

## <a name="remarks"></a>備註

篩選可能會在目前範例的停止時間之前接收資料流程結束通知。 如果是這樣，篩選器應該在將 [**EC \_ 完成**](ec-complete.md) 通知張貼至篩選圖形管理員之前等候。

因此：

-   如果篩選已收到早期的資料流程結尾 (EOS) 通知，這個方法會排定計時器事件。 當計時器事件啟動時，篩選會張貼 EC \_ COMPLETE 事件。
-   如果篩選器收到非早期的 EOS 通知，這個方法會立即張貼 EC \_ 完成事件。
-   如果篩選沒有任何擱置中的 EOS 通知，則方法會傳回而不會執行任何作業。

計時器回呼方法是 [**CBaseRenderer：： TimerCallback**](cbaserenderer-timercallback.md)。 為了傳遞 EC \_ COMPLETE 事件，篩選準則會呼叫 [**CBaseRenderer：： NotifyEndOfStream**](cbaserenderer-notifyendofstream.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 





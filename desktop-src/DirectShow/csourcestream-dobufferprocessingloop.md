---
description: DoBufferProcessingLoop 方法會產生媒體資料，並將其傳遞至下游輸入 pin。
ms.assetid: a8dce761-eed6-402d-9115-e21822d7a853
title: 'CSourceStream. DoBufferProcessingLoop 方法 (Source .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.DoBufferProcessingLoop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d23df592abd125fd64362af89b6f81c5e9dcc20f0aa6cc998974a8fd2d4d87f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953737"
---
# <a name="csourcestreamdobufferprocessingloop-method"></a>CSourceStream. DoBufferProcessingLoop 方法

`DoBufferProcessingLoop`方法會產生媒體資料，並將其傳遞至下游輸入 pin。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DoBufferProcessingLoop();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表所示的值。



| 傳回碼                                                                             | 描述                                                             |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 執行緒收到停止要求。<br/>                              |
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 資料流程已結束，或下游篩選不接受範例。<br/> |



 

## <a name="remarks"></a>備註

這個方法會實處理資料並將它傳遞給下游的主要迴圈。 每次通過迴圈時，方法都會從配置器取出空白媒體範例。 它會將範例傳遞給 [**CSourceStream：： FillBuffer**](csourcestream-fillbuffer.md) 方法。 衍生類別必須執行的 **FillBuffer** 方法會產生媒體資料，並將它放在範例緩衝區中。

當發生下列任何情況時，迴圈就會結束：

-   輸入 pin 的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法會拒絕範例。
-   **FillBuffer** 方法會傳回 \_ FALSE，表示資料流程的結尾，或傳回錯誤碼。
-   執行緒收到 [**CSourceStream：： Stop**](csourcestream-stop.md) 要求。

`DoBufferProcessingLoop`方法會處理結束資料流程的通知。 如果發生錯誤，它會將 [**EC \_ ERRORABORT**](ec-errorabort.md) 事件傳送至篩選圖形管理員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>來源 .h (包含) 的資料流程 </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceStream 類別**](csourcestream.md)
</dt> </dl>

 

 





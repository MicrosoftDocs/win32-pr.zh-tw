---
description: Run 方法會執行篩選。
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: 'CBaseRenderer： Run 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987849"
---
# <a name="cbaserendererrun-method"></a>CBaseRenderer 方法

`Run`方法會執行篩選。

## <a name="syntax"></a>語法


```C++
HRESULT Run();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：： Run**](cbasefilter-run.md) 方法。 其會執行下列動作：

-   呼叫 **CBaseFilter：： Run** 方法。
-   認可配置器。  (參閱 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)。 ) 
-   如果先前的狀態為 [已停止]，則篩選會釋放它所持有的任何範例。  (範例不再有效。 ) 
-   呼叫 [**CBaseRenderer：： StartStreaming**](cbaserenderer-startstreaming.md) 方法，並傳回結果。 如果範例暫止， **StartStreaming** 方法會排程它以進行轉譯。

如果篩選未連接，則會立即張貼 [**EC \_ 完成**](ec-complete.md) 事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 





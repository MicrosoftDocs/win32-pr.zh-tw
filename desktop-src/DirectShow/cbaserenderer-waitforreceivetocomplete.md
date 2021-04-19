---
description: WaitForReceiveToComplete 方法會等候 CBaseRenderer：： Receive 方法完成。
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: 'CBaseRenderer. WaitForReceiveToComplete 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986572"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>CBaseRenderer. WaitForReceiveToComplete 方法

`WaitForReceiveToComplete`方法 [**會等候 CBaseRenderer：： Receive**](cbaserenderer-receive.md)方法完成。

## <a name="syntax"></a>語法


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**CBaseRenderer：： Stop**](cbaserenderer-stop.md)和 [**CBaseRenderer：： BeginFlush**](cbaserenderer-beginflush.md)方法會呼叫這個方法，將狀態變更與 **Receive** 方法進行同步處理。

具體來說，這個方法會在等候 [**CBaseRenderer：： m \_ bInReceive**](cbaserenderer-m-binreceive.md) 旗標變成 **FALSE** 時，分派訊息。 [**CBaseRenderer：:P reparereceive**](cbaserenderer-preparereceive.md)方法中的旗標會變成 **TRUE** ，並在 **Receive** 方法呼叫 [**CBaseRenderer：:P reparerender**](cbaserenderer-preparerender.md)方法之後切換回 **FALSE** 。 衍生的類別可以使用 **PrepareRender** 來設定調色板。 等候 **PrepareRender** 完成可確保在狀態變更發生之前，會先分派元件變更訊息。 這樣可以避免潛在的鎖死。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 





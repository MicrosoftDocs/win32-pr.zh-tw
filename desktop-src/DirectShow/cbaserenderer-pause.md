---
description: Pause 方法會暫停篩選。
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: 'CBaseRenderer： Pause 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9769a1243fdbd69037e275fc083a9b1b0766f7f404190b2e68920f238e2bf140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586078"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer. Pause 方法

`Pause`方法會暫停篩選。

## <a name="syntax"></a>語法


```C++
HRESULT Pause();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值包括下表中的值。



| 傳回碼                                                                             | 描述                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 轉換已完成。<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 轉換未完成。<br/> |



 

## <a name="remarks"></a>備註

這個方法會覆寫 [**CBaseFilter：:P ause**](cbasefilter-pause.md) 方法。 它會執行下列步驟：

-   呼叫 **CBaseFilter：:P ause** 方法。
-   認可配置器。  (參閱 [**IMemAllocator：： Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)。 ) 
-   如果先前的狀態為 [已停止]，則篩選會釋放它所持有的任何範例。  (範例不再有效。 ) 
-   呼叫 [**CBaseRenderer：： CompleteStateChange**](cbaserenderer-completestatechange.md) 方法，並傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 





---
description: 通知方法會收到要求品質變更的通知。
ms.assetid: bb9aa1c3-caef-42fb-87d2-75cc3691f64f
title: 'CBaseVideoRenderer： Notify 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8674ecbf7951ca0c208f9ffb50c0e5d9591b16552fda266c7d641905edd09a4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052188"
---
# <a name="cbasevideorenderernotify-method"></a>CBaseVideoRenderer。通知方法

`Notify`方法會收到要求品質變更的通知。

## <a name="syntax"></a>語法


```C++
HRESULT Notify(
  [in] IBaseFilter *pSelf,
  [in] Quality     q
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSelf* \[在\]
</dt> <dd>

傳送品質通知的篩選準則指標。

</dd> <dt>

*q* \[ in\]
</dt> <dd>

品質通知結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會在影片轉譯器上 [**執行 IQualityControl：： Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) 方法。 當品質必須剪下時，通常會由篩選圖形管理員呼叫這項功能。 當音訊播放品質已增加到必須降低影片播放品質的點時，就可能發生這種情況。

`Notify` 將 **m \_ trThrottle** 資料成員設定為要依 [**ThrottleWait**](cbasevideorenderer-throttlewait.md)在框架之間插入的延遲值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 





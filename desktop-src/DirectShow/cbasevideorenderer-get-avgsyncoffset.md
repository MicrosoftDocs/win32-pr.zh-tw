---
description: Get \_ AvgSyncOffset 方法會以毫秒為單位，抓取每個畫面格的到期時間，以及自從串流開始之後，針對所有框架實際呈現的時間。
ms.assetid: b41741e9-e0b5-4c49-93ef-cb8c0cf2ddeb
title: 'CBaseVideoRenderer.get_AvgSyncOffset 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_AvgSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35c682b8f4bb60ec629db5489e879d1ca7968b77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000730"
---
# <a name="cbasevideorendererget_avgsyncoffset-method"></a>CBaseVideoRenderer. 取得 \_ AvgSyncOffset 方法

`get_AvgSyncOffset`方法會以毫秒為單位，抓取每個框架的到期時間，以及自從串流開始之後，針對所有框架實際轉譯的時間。

## <a name="syntax"></a>語法


```C++
HRESULT get_AvgSyncOffset(
   int *piAvg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piAvg* 
</dt> <dd>

先前所述的平均時間指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IQualProp：： get \_ AvgSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_avgsyncoffset) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 





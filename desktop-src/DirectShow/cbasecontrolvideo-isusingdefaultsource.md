---
description: IsUsingDefaultSource 方法會判斷轉譯器是否使用預設的來源視窗。
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: 'CBaseControlVideo. IsUsingDefaultSource 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991248"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>CBaseControlVideo. IsUsingDefaultSource 方法

`IsUsingDefaultSource`方法會判斷轉譯器是否使用預設的來源視窗。

## <a name="syntax"></a>語法


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果轉譯器 \_ 使用預設來源，則傳回 [確定]，否則傳回 \_ FALSE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 





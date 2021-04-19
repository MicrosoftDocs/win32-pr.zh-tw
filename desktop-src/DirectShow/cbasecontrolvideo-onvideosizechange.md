---
description: 將 EC \_ 影片 \_ 大小變更的訊息傳遞 \_ 至篩選圖形管理員。
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: 'CBaseControlVideo. OnVideoSizeChange 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985955"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>CBaseControlVideo. OnVideoSizeChange 方法

將 EC \_ 影片 \_ 大小變更的訊息傳遞 \_ 至篩選圖形管理員。

## <a name="syntax"></a>語法


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回相依于實值的 **HRESULT** 值。可以是下列其中一個值，或其他未列出的值。



| 傳回碼                                                                                   | Description               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 失敗。<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/> |



 

## <a name="remarks"></a>備註

影片轉譯器會在每次影片大小變更時呼叫此成員函式;這通常會在初始連接之後呼叫一次。 如果轉譯器可支援從 320 x 240 到 160 x 120)  (動態格式變更，它也應該在每次變更之後呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 





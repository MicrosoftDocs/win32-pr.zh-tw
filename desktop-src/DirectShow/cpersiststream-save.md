---
description: 將篩選的資料儲存至指定的資料流程。
ms.assetid: f45c8c6e-f0bb-4358-805a-da2669706d34
title: 'CPersistStream： Save 方法 (Pstream .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.Save
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c16e4820f846d2d60382fabd6aafe3ad82880193
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989839"
---
# <a name="cpersiststreamsave-method"></a>CPersistStream。 Save 方法

將篩選的資料儲存至指定的資料流程。

## <a name="syntax"></a>語法


```C++
HRESULT Save(
   LPSTREAM pStm,
   BOOL     fClearDirty
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pStm* 
</dt> <dd>

要儲存資料的資料流程指標。

</dd> <dt>

*fClearDirty* 
</dt> <dd>

指出是否要重設目前資料流程之中途旗標的旗標; **TRUE** 表示重設它。  (在儲存作業中呼叫方法時，此值通常為 **TRUE**。當呼叫做為「另存新檔」作業的一部分時，值通常是 **FALSE**。 ) 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實行 **IPersistStream：： Save** 方法。 它會以軟體版本呼叫 **WriteInt** 、使用 *pStm* 中的串流呼叫 [**CPersistStream：： WriteToStream**](cpersiststream-writetostream.md) ，然後重設 **mp \_ fDirty**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Pstream (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPersistStream 類別**](cpersiststream.md)
</dt> </dl>

 

 





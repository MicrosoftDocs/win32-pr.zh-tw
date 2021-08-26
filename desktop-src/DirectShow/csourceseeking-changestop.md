---
description: 當停止位置變更時，會呼叫 ChangeStop 方法。
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: 'CSourceSeeking. ChangeStop 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 09473b5bbe20c6c31748f0079594424f7e0afa62e2594ff1cc80f33cb1f5e6bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103118"
---
# <a name="csourceseekingchangestop-method"></a>CSourceSeeking. ChangeStop 方法

`ChangeStop`當停止位置變更時，會呼叫方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

如果停止位置變更， [**CSourceSeeking：： SetPositions**](csourceseeking-setpositions.md) 方法會呼叫這個方法。 這個方法是純虛擬的;衍生的類別必須加以執行。 下列範例顯示可能的實作為：


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSourceSeeking 類別**](csourceseeking.md)
</dt> </dl>

 

 





---
description: 取消註冊方法會將篩選從登錄中移除。
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: 'CBaseFilter：取消註冊方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c57d08c77c9c420cdc45b158a19fa610231f53f6b409d8b650953de0de8381a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317898"
---
# <a name="cbasefilterunregister-method"></a>CBaseFilter，取消註冊方法

`Unregister`方法會從登錄中移除篩選。

> [!Note]  
> 這個方法已過時。 新的篩選器應該使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 函式來取消註冊。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

 

## <a name="syntax"></a>語法


```C++
HRESULT Unregister();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 





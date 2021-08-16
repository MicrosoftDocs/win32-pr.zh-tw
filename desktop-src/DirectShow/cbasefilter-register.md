---
description: Register 方法會將篩選準則新增至登錄。
ms.assetid: 934e421a-25a6-40fa-a48b-6d7331f34b78
title: 'CBaseFilter： Register 方法 (Amfilter) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Register
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168d84d3bfc90fb710ae65a3b887eeb5575db407361a256c48161f0f7968a53c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118403521"
---
# <a name="cbasefilterregister-method"></a>CBaseFilter 註冊方法

`Register`方法會將篩選準則新增至登錄。

> [!Note]  
> 這個方法已過時。 您應使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 函式來註冊新的篩選準則。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

 

## <a name="syntax"></a>語法


```C++
HRESULT Register();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下表所列的其中一個 **HRESULT** 值。



| 傳回碼                                                                             | Description                                          |
|-----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 成功。<br/>                                  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 沒有任何註冊資訊可供使用。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseFilter 類別**](cbasefilter.md)
</dt> </dl>

 

 





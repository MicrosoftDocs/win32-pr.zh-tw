---
description: 已過時。 請改用 AMovieSetupRegisterFilter2。
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: 'AMovieSetupRegisterFilter 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 23f3120bea744303dd95403e8642133de0681dd440c45014f8e787318ab9f857
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001873"
---
# <a name="amoviesetupregisterfilter-function"></a>AMovieSetupRegisterFilter 函式

已過時。 請改用 [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psetupdata* 
</dt> <dd>

保留的。

</dd> <dt>

*pIFM* 
</dt> <dd>

保留的。

</dd> <dt>

*bRegister* 
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dllsetup (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DLL 安裝函式**](dll-setup-functions.md)
</dt> </dl>

 

 





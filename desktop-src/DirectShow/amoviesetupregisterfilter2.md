---
description: AMovieSetupRegisterFilter2 函式會使用 IFilterMapper2 介面，在登錄中註冊篩選器的業績、釘選和媒體類型。
ms.assetid: 8e0f3485-9e5d-4b22-853d-4ad9b1fb71d2
title: 'AMovieSetupRegisterFilter2 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 272b781cf70f1dede9d4eea64b45d3d9d793a119
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976210"
---
# <a name="amoviesetupregisterfilter2-function"></a>AMovieSetupRegisterFilter2 函式

**AMovieSetupRegisterFilter2** 函式會使用 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)介面，在登錄中註冊篩選器的業績、釘選和媒體類型。

## <a name="syntax"></a>語法


```C++
HRESULT AMovieDllRegisterServer(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper2             *pIFM2,
         BOOL                       bRegister
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*psetupdata* 
</dt> <dd>

[**AMOVIESETUP \_ 篩選**](amoviesetup-filter.md)資料的指標。

</dd> <dt>

*pIFM2* 
</dt> <dd>

[**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)介面的指標。

</dd> <dt>

*bRegister* 
</dt> <dd>

指出是否要註冊篩選準則的值。 **TRUE** 表示註冊篩選準則， **FALSE** 表示將其取消註冊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

[**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)函式會在註冊 COM 伺服器之後，呼叫此 helper 函式以註冊篩選。

一般而言，篩選準則會使用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) ，且不會直接呼叫此函式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dllsetup (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DLL 安裝函式**](dll-setup-functions.md)
</dt> </dl>

 

 





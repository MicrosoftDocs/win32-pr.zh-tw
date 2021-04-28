---
description: AMovieDllRegisterServer 函式已淘汰。 請改用 AMovieDllRegisterServer2。
ms.assetid: d3be5fe0-f993-4a15-a3b8-3d761d51f289
title: 'AMovieDllRegisterServer 函式 (Dllsetup) '
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
ms.openlocfilehash: 81b6e73b1988d3eb97abdf9a5d2415ecbd62d8c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099936"
---
# <a name="amoviedllregisterserver-function"></a>AMovieDllRegisterServer 函式

已過時。 請改用 [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) 。

## <a name="syntax"></a>語法


```C++
HRESULT AMovieDllRegisterServer(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

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

 

 





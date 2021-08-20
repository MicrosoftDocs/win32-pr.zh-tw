---
description: AMovieDllRegisterServer2 函數會註冊及取消註冊篩選。
ms.assetid: 2122949d-0117-4c68-bfcd-c717b14dc970
title: 'AMovieDllRegisterServer2 函式 (Dllsetup) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieDllRegisterServer2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c47b861a47498cc29d80061c6c2da1ffc44e40b7446588cf7c3376e5ed18e837
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118001981"
---
# <a name="amoviedllregisterserver2-function"></a>AMovieDllRegisterServer2 函式

**AMovieDllRegisterServer2** 函數會註冊及取消註冊篩選。

## <a name="syntax"></a>語法


```C++
HRESULT AMovieDllRegisterServer2(
   BOOL bRegister
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bRegister* 
</dt> <dd>

**TRUE** 表示註冊篩選準則， **FALSE** 表示將其取消註冊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

您可以使用此函式來設定篩選。 如需詳細資訊，請參閱[如何註冊 DirectShow 篩選](how-to-register-directshow-filters.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dllsetup (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DLL 安裝函式**](dll-setup-functions.md)
</dt> </dl>

 

 





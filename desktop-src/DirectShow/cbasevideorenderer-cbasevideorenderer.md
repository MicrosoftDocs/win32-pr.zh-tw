---
description: CBaseVideoRenderer。 CBaseVideoRenderer 函式-函數方法。
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: 'CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec6a5e12d12b12f22cf1089d85ed4c07656da86cda071d8645355890996e2cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954757"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a>CBaseVideoRenderer. CBaseVideoRenderer 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RenderClass* 
</dt> <dd>

此轉譯器的類別識別碼。

</dd> <dt>

*pName* 
</dt> <dd>

用於偵錯工具之描述的指標。

</dd> <dt>

*朋 克* 
</dt> <dd>

匯總的擁有者物件的指標。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 





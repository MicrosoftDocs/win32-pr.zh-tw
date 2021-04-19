---
description: IsClassID 方法會判斷 CLSID 是否符合此類別範本。
ms.assetid: de560f7a-2ccb-44e2-ac32-3b0fea0d80b8
title: 'CFactoryTemplate. IsClassID 方法 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.IsClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94564d7e9db52f8be22717a10f73fffb7fb6fa14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994362"
---
# <a name="cfactorytemplateisclassid-method"></a>CFactoryTemplate. IsClassID 方法

`IsClassID`方法會判斷 CLSID 是否符合此類別範本。

## <a name="syntax"></a>語法


```C++
BOOL IsClassID(
   REFCLSID rclsid
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*rclsid* 
</dt> <dd>

CLSID 的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *rclsid* 參數與 [**CFactoryTemplate：： m \_ CLSID**](cfactorytemplate-m-clsid.md)成員變數的 Clsid 相同，則傳回 **TRUE** ，否則傳回 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 





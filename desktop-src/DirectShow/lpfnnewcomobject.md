---
description: 函數的指標，該函式會建立物件的實例。
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: 'LPFNNewCOMObject 函式指標 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: 07c0f8ab961c872c9dc0f92d2fff519b94cd049e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976163"
---
# <a name="lpfnnewcomobject-function-pointer"></a>LPFNNewCOMObject 函式指標

函數的指標，該函式會建立物件的實例。

## <a name="syntax"></a>語法


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pUnkOuter* 
</dt> <dd>

物件的 **IUnknown** 介面指標，該物件會匯總新物件（如果有的話）。 此指標可以是 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 如果函式失敗，此參數會收到錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回物件新實例的指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Combase (包含： .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 





---
description: 函數的指標，該函式會建立物件的實例。
ms.assetid: 86859bf9-e16a-4494-bf1b-1d8ddbc1c805
title: 'CFactoryTemplate：： m_lpfnNew 成員 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lpfnNew
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2299f7a87f348ac8a5fa6c6d83b6a17fbf97ca28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994361"
---
# <a name="cfactorytemplatem_lpfnnew-member"></a>CFactoryTemplate：： m \_ lpfnNew 成員

函數的指標，該函式會建立物件的實例。

## <a name="syntax"></a>語法


```C++
LPFNNewCOMObject m_lpfnNew;
```



## <a name="remarks"></a>備註

在您的 DLL 中，宣告會傳回物件新實例指標的靜態函式。 在 factory 範本中，將 **m \_ lpfnNew** 成員變數設定為這個靜態函式的位址。

函數指標型別為 [**LPFNNewCOMObject**](lpfnnewcomobject.md)。

下列範例顯示 **m \_ lpfnNew** 的一般函數：


```C++
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = 
        new CMyComponent(NAME("My Component"), pUnk, pHr );

    if (pNewObject == NULL)  
    {
        *phr = E_OUTOFMEMORY;
    }
    return pNewObject;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CFactoryTemplate 類別**](cfactorytemplate.md)
</dt> </dl>

 

 





---
description: INonDelegatingUnknown 介面是已重新命名的 IUnknown 版本，可支援 nondelegating 和委派相同 COM 物件中的 IUnknown 介面。
ms.assetid: a2faf9d1-2130-4c6c-8fcd-3e118d592b7f
title: 'INonDelegatingUnknown (Combase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INonDelegatingUnknown
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f733ba28af1b4ecb7fc0a52852b4d8663fddf1df07572c409136a9aa963ba076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051608"
---
# <a name="inondelegatingunknown"></a>INonDelegatingUnknown

`INonDelegatingUnknown`介面是已重新命名的 **IUnknown** 版本，可支援 nondelegating 以及在相同的 COM 物件中委派 **IUnknown** 介面。

## <a name="syntax"></a>語法


```C++
interface INonDelegatingUnknown
{
    virtual HRESULT NonDelegatingQueryInterface) (REFIID riid, LPVOID *ppv) PURE;
    virtual ULONG NonDelegatingAddRef)(void) PURE;
    virtual ULONG NonDelegatingRelease)(void) PURE;
};
```



## <a name="remarks"></a>備註

若要使用 `INonDelegatingUnknown` 多重繼承，請執行下列步驟。

1.  從介面衍生您的類別，例如 IMyInterface。
2.  在您的類別定義中包含 [**declare \_ IUNKNOWN**](declare-iunknown.md) ，以宣告呼叫外部未知之 **QueryInterface**、 **AddRef** 和 **Release** 的實部。
3.  覆寫 **NonDelegatingQueryInterface** 以公開具有下列程式碼的 IMyInterface：
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  宣告和執行 IMyInterface 的成員函式。

若要使用 `INonDelegatingUnknown` 于嵌套介面，請執行下列步驟：

1.  宣告衍生自 [**CUnknown**](cunknown.md)的類別。
2.  在您的類別定義中包含 [**DECLARE \_ IUNKNOWN**](declare-iunknown.md) 。
3.  覆寫 **NonDelegatingQueryInterface** 以使用下列程式碼來公開 IMyInterface：
    ```C++
         if (riid == IID_IMyInterface) {
             return GetInterface((IMyInterface *) this, ppv);
         } else {
             return CUnknown::NonDelegatingQueryInterface(riid, ppv);
         }
    ```

    

4.  執行 IMyInterface 的成員函式。 使用 [**CUnknown：： GetOwner**](cunknown-getowner.md) 存取 COM 物件類別。
5.  在您的 COM 物件類別中，將嵌套類別設為 COM 物件類別的 friend，然後將嵌套類別的實例宣告為 COM 物件類別的成員。

因為您必須一律將外部未知和 **HRESULT** 傳遞給 [**CUnknown**](cunknown.md) 的函式，所以您無法使用預設的函式。 您必須讓成員變數成為類別的指標，並在您的函式中進行新的呼叫，以實際建立它。

使用下列程式碼覆寫 **NonDelegatingQueryInterface** ：


```C++
     if (riid == IID_IMyInterface) {
         return m_pImplFilter->
            NonDelegatingQueryInterface(IID_IMyInterface, ppv);
     } else {
         return CUnknown::NonDelegatingQueryInterface(riid, ppv);
     }
```



您可以有混合類別，透過多個繼承和一些介面（透過嵌套類別）來支援某些介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Combase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**COM Helper 函數**](com-helper-functions.md)
</dt> </dl>

 

 





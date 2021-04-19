---
description: Show 方法會顯示或隱藏對話方塊。 這個方法會實 IPropertyPage：： Show 方法。
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: 'CBasePropertyPage： Show 方法 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990298"
---
# <a name="cbasepropertypageshow-method"></a>CBasePropertyPage 方法

`Show`方法會顯示或隱藏對話方塊。 這個方法會實 [IPropertyPage：： Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) 方法。

## <a name="syntax"></a>語法

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a>參數

*nCmdShow*

類型： **[UINT](../winprog/windows-data-types.md)**

指定是否要顯示或隱藏視窗的值。 如需詳細資訊，請參閱 [IPropertyPage：： Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) 方法。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。

| 傳回碼                                                                                  | Description                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 成功。<br/>            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 無效引數。<br/>   |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl> | 發生非預期的失敗。<br/> |

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫 | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |

## <a name="see-also"></a>另請參閱

[CBasePropertyPage 類別](cbasepropertypage.md)

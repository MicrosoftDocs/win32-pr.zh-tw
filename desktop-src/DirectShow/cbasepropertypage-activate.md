---
description: 啟動方法會建立對話方塊視窗。 這個方法會實 IPropertyPage：： Activate 方法。
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: 'CBasePropertyPage 啟動方法 (Cprop) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989604"
---
# <a name="cbasepropertypageactivate-method"></a>CBasePropertyPage。 Activate 方法

`Activate`方法會建立對話方塊視窗。 這個方法會實 **IPropertyPage：： Activate** 方法。

## <a name="syntax"></a>語法


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* 
</dt> <dd>

對話方塊的父視窗的控制碼。

</dd> <dt>

*prect* 
</dt> <dd>

**矩形** 結構的指標，該結構包含對話方塊的位置資訊。

</dd> <dt>

*fModal* 
</dt> <dd>

布林值，指出對話方塊框架是否為強制回應 (**TRUE**) 或非模式 (**FALSE**) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                   | Description                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 成功。<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>       |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | **Null** 指標引數。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>  | 發生非預期的失敗。<br/>        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Cprop (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBasePropertyPage 類別**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage：： OnActivate**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 





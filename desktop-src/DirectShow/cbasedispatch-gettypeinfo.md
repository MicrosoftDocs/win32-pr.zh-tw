---
description: CBaseDispatch. GetTypeInfo 方法-GetTypeInfo 方法會抓取物件的型別資訊，然後用它來取得介面的型別資訊。
ms.assetid: aa06b97c-541b-44fc-bdef-97fd1f014e85
title: 'CBaseDispatch. GetTypeInfo 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 294b9758aa79ab033c1e3cf8932056ca10e7bf2424de97a1cf9f3b509f1906bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076678"
---
# <a name="cbasedispatchgettypeinfo-method"></a>CBaseDispatch. GetTypeInfo 方法

`GetTypeInfo`方法會抓取物件的型別資訊，然後用來取得介面的型別資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetTypeInfo(
   REFIID    riid,
   UINT      itinfo,
   LCID      lcid,
   ITypeInfo **pptinfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* 
</dt> <dd>

指定介面 (IID) 的介面識別碼參考。

</dd> <dt>

*itinfo* 
</dt> <dd>

要傳回的類型資訊。 必須為零。

</dd> <dt>

*lcid* 
</dt> <dd>

地區設定識別項。

</dd> <dt>

*>pptinfo* 
</dt> <dd>

接收 **ITypeInfo** 指標之變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下。



| 傳回碼                                                                                             | 描述                                    |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                    | 成功。<br/>                            |
| <dl> <dt>**E \_ 指標**</dt> </dl>               | **Null** 指標引數。<br/>          |
| <dl> <dt>**輸入 \_ E \_ ELEMENTNOTFOUND**</dt> </dl> | *Itinfo* 參數不是零。<br/> |



 

## <a name="remarks"></a>備註

這個方法的行為類似于 **IDispatch：： GetTypeInfo** 方法。 不過，它還包含一個額外的 *參數，也* 就是指定要取得其型別資訊的介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseDispatch 類別**](cbasedispatch.md)
</dt> </dl>

 

 





---
description: CBaseDispatch. GetTypeInfoCount 方法-GetTypeInfoCount 方法會抓取物件提供的類型資訊介面數目。
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: 'CBaseDispatch. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da80cdb4810ea3e598ad9483ccf52e8033ccb1a5b7ee65351e2cfcc273a3415f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660015"
---
# <a name="cbasedispatchgettypeinfocount-method"></a>CBaseDispatch. GetTypeInfoCount 方法

方法會抓取 `GetTypeInfoCount` 物件提供的類型資訊介面數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pctinfo* 
</dt> <dd>

變數的指標，此變數會接收物件提供的類型資訊介面數目。 當方法傳回時，值為1。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列其中一個值。



| 傳回碼                                                                               | 描述                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 成功。<br/>                   |
| <dl> <dt>**E \_ 指標**</dt> </dl> | **Null** 指標引數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseDispatch 類別**](cbasedispatch.md)
</dt> </dl>

 

 





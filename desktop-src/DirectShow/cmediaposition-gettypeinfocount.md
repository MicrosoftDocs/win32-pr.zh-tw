---
description: GetTypeInfoCount 方法會抓取物件提供的類型資訊介面數目。
ms.assetid: c98368f2-ae0c-4301-be30-7332b19f53ee
title: 'CMediaPosition. GetTypeInfoCount 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cac543c49b7f2f6b9dc3357bbb1c691477d9b62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977570"
---
# <a name="cmediapositiongettypeinfocount-method"></a>CMediaPosition. GetTypeInfoCount 方法

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



| 傳回碼                                                                               | Description                           |
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

[**CMediaPosition 類別**](cmediaposition.md)
</dt> </dl>

 

 





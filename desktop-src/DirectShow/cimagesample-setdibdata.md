---
description: SetDIBData 方法會指定此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。 呼叫這個方法來初始化 CImageSample 物件。
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: 'CImageSample. SetDIBData 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 367fed37545e9498f9f6e753a57a7eeeb2ce8767779241284be9109676fafd38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655522"
---
# <a name="cimagesamplesetdibdata-method"></a>CImageSample. SetDIBData 方法

`SetDIBData`方法會指定此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。 呼叫這個方法來初始化 **CImageSample** 物件。

## <a name="syntax"></a>語法


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDibData* 
</dt> <dd>

[**DIBDATA**](dibdata.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageSample 類別**](cimagesample.md)
</dt> </dl>

 

 





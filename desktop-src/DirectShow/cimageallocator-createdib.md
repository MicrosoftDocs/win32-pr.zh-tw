---
description: CreateDIB 方法會在 DIB)  (建立與 GDI 裝置無關的點陣圖。 DIB 是在共用的 mempory 區塊中配置，可在擁有篩選器 blits 影像時排除複製作業。
ms.assetid: 8a9ab1cf-4104-48e9-ba6c-28d0f1a1d226
title: 'CImageAllocator. CreateDIB 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateDIB
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a629831ea50219b47500c0637cfeaebfbc95b1ee99a8b9d3872a655ab5485c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055478"
---
# <a name="cimageallocatorcreatedib-method"></a>CImageAllocator. CreateDIB 方法

`CreateDIB`方法會建立與 GDI 裝置無關的點陣圖 (DIB) 。 DIB 是在共用的 mempory 區塊中配置，可在擁有篩選器 blits 影像時排除複製作業。

## <a name="syntax"></a>語法


```C++
HRESULT CreateDIB(
        LONG    InSize,
  [ref] DIBDATA &DibData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*InSize* 
</dt> <dd>

點陣圖的大小。

</dd> <dt>

*DibData* \[裁判\]
</dt> <dd>

[**DIBDATA**](dibdata.md)結構的參考。 方法會在此結構中填入 DIB 的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果成功，則傳回，否則傳回錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator：：配置**](cimageallocator-alloc.md)
</dt> </dl>

 

 





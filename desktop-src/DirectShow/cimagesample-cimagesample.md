---
description: 函式方法。
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: 'CImageSample. CImageSample (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998379"
---
# <a name="cimagesamplecimagesample-constructor"></a>CImageSample. CImageSample 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAllocator* 
</dt> <dd>

建立此範例的配置器指標。

</dd> <dt>

*pName* 
</dt> <dd>

忽略。

</dd> <dt>

*phr* 
</dt> <dd>

忽略。

</dd> <dt>

*pBuffer* 
</dt> <dd>

由呼叫端配置的記憶體緩衝區指標，大小 *長度*。 緩衝區應該包含與 GDI 裝置無關的點陣圖 (DIB) 。

</dd> <dt>

*length* (長度) 
</dt> <dd>

緩衝區的長度。

</dd> </dl>

## <a name="remarks"></a>備註

[**CImageAllocator**](cimageallocator.md)類別會使用作業系統分頁檔所支援的檔案對應物件來建立 DIB。 檔案對應物件的控制碼會儲存在 **m \_ DibData** 結構的 **hMapping** 成員中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageSample 類別**](cimagesample.md)
</dt> </dl>

 

 





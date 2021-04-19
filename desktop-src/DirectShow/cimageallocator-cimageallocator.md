---
description: 函式方法。
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: 'CImageAllocator. CImageAllocator (Winutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f6873e8cc073e0b716f94c980ecceba8f4512f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993414"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>CImageAllocator. CImageAllocator 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pFilter* 
</dt> <dd>

擁有篩選準則的指標。

</dd> <dt>

*pName* 
</dt> <dd>

字串的指標，其中包含配置器的偵錯工具名稱。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 建立物件之前，請先將值設定為 \_ [確定]。 如果此函式失敗，則會將值設定為錯誤碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageAllocator 類別**](cimageallocator.md)
</dt> </dl>

 

 





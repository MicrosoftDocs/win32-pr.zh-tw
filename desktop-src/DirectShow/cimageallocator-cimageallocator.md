---
description: CImageAllocator。 CImageAllocator 函式-函數方法。
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
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085756"
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

 

 





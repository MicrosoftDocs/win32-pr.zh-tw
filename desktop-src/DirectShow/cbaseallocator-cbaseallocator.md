---
description: 函式方法。
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: 'CBaseAllocator. CBaseAllocator (Amfilter. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985933"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a>CBaseAllocator. CBaseAllocator 函數

函式方法。

## <a name="syntax"></a>語法


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

字串的指標，其中包含配置器的偵錯工具名稱。 如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標。 如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。 否則，請將此參數設定為 **Null**。

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。 建立物件之前，請先將值設定為 \_ [確定]。 如果此函式失敗，則會將值設定為錯誤碼。

</dd> <dt>

*bEvent* 
</dt> <dd>

指出是否要建立信號的布林值。 若 **為 TRUE**，配置器會建立信號 ([**CBaseAllocator：： m \_ hSem**](cbaseallocator-m-hsem.md)) ，只要範例變成可用，就會收到信號。 如果您要執行不需要信號的衍生類別，請將值設定為 **FALSE** 。

</dd> <dt>

*fEnableReleaseCallback* 
</dt> <dd>

指出是否已啟用發行回呼機制的布林值。 如果您想要提供回呼介面（當釋放緩衝區時呼叫），請將此值設定為 **TRUE** 。 藉由呼叫 [**CBaseAllocator：： SetNotify**](cbaseallocator-setnotify.md) 方法來指定回呼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Amfilter (包含： .h) </dt> </dl>                                                                                  |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseAllocator 類別**](cbaseallocator.md)
</dt> </dl>

 

 





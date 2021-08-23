---
description: GetFlags 方法會抓取與延後命令相關聯的內容旗標。
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: 'CDeferredCommand. GetFlags 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c3ee5826c1b4ff81f90c86a6db4517aafc41313e53672486c41ab4847e82674
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910188"
---
# <a name="cdeferredcommandgetflags-method"></a>CDeferredCommand. GetFlags 方法

方法會抓取 `GetFlags` 與延後命令相關聯的內容旗標。

## <a name="syntax"></a>語法


```C++
short GetFlags();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回下列項目之一：



| 傳回碼                                                                                             | 描述                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**分派 \_ 方法**</dt> </dl>         | 以方法的形式執行成員。 如果屬性具有相同的名稱，則可以設定此和分派 \_ PROPERTYGET 旗標。<br/>                                               |
| <dl> <dt>**分派 \_ PROPERTYGET**</dt> </dl>    | 正在將成員取出為屬性或資料成員。<br/>                                                                                                         |
| <dl> <dt>**分派 \_ PROPERTYPUT**</dt> </dl>    | 成員正變更為屬性或資料成員。<br/>                                                                                                           |
| <dl> <dt>**分派 \_ PROPERTYPUTREF**</dt> </dl> | 成員正在透過參考指派進行變更，而不是值指派。 只有當屬性接受物件的參考時，此旗標才會是有效的。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDeferredCommand 類別**](cdeferredcommand.md)
</dt> </dl>

 

 





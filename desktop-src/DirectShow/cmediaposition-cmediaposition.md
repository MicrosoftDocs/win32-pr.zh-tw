---
description: 瞭解 CMediaPosition. CMediaPosition (Ctlutil .h) 的方法。 這個方法會使用 ' pName ' 和 ' pUnk ' 參數。
ms.assetid: 18a7785c-30c6-43b8-9a41-542a8424522c
title: CMediaPosition. CMediaPosition (Ctlutil .h) -pName，pUnk 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0df3337c07ed678354515bdf0c665a5d6157f158ac6c2370a8981d8e5028b27e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634790"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-parameters"></a>CMediaPosition. CMediaPosition (Ctlutil .h) -pName，pUnk 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* 
</dt> <dd>

物件名稱的指標，用於偵測用途。 在靜態記憶體中配置此參數。

</dd> <dt>

*朋 克* 
</dt> <dd>

這個物件之擁有者的指標，如果物件不是匯總，則為 **Null** 。

</dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 標頭 | Ctlutil (包含： .h)  |
| 程式庫|  (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建)  |

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CMediaPosition 類別**](cmediaposition.md)
</dt> </dl>

 

 





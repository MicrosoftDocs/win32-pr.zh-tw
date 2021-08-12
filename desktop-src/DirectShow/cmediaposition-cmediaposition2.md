---
description: 瞭解 CMediaPosition. CMediaPosition (Ctlutil .h) 的方法。 這個方法會使用 ' pName '、' pUnk ' 和 ' phr ' 參數。
ms.assetid: 4074f513-d1e7-4311-8732-4d755e621e55
title: 'CMediaPosition. CMediaPosition (Ctlutil. h) '
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
ms.openlocfilehash: 101678ebcb851ef0fcdc8eeaa202435ca80eb796555c81e5e5d95eb4998131c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118655259"
---
# <a name="cmediapositioncmediaposition-constructor-ctlutilh---pname-punk-phr-parameters"></a>CMediaPosition. CMediaPosition (Ctlutil .h) -pName、pUnk、phr 參數

函式方法。

## <a name="syntax"></a>語法


```C++
CMediaPosition(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
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

</dd> <dt>

*phr* 
</dt> <dd>

**HRESULT** 值的指標。

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

 

 





---
title: IReferenceClock GetTime 方法
description: GetTime 方法會抓取目前的參考時間。
ms.assetid: 9bf5050a-ae09-4a72-a3f2-3df8339d99b9
keywords:
- GetTime 方法 windows Media 格式
- GetTime 方法 windows Media Format，IReferenceClock 介面
- IReferenceClock 介面 windows Media Format，GetTime 方法
topic_type:
- apiref
api_name:
- IReferenceClock.GetTime
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f7756240e8987199e1f1b5d79e3f0b676d4808520781fbac18dfa18dd75e88d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055438"
---
# <a name="ireferenceclockgettime-method"></a>IReferenceClock：： GetTime 方法

**GetTime** 方法會抓取目前的參考時間。

## <a name="syntax"></a>語法


```C++
HRESULT GetTime(
  [out] REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTime* \[擴展\]
</dt> <dd>

接收目前時間的變數指標，以 100-毫微秒單位表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                               | 描述                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 此方法已成功。<br/>              |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *PTime* 參數為 **Null**。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IReferenceClock 介面**](ireferenceclock.md)
</dt> </dl>

 

 






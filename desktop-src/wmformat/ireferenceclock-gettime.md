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
ms.openlocfilehash: c679ce0adbbc6cc7ddc014c12f1b0ace4be6b4b0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373405"
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



| 傳回碼                                                                               | Description                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>      | 此方法已成功。<br/>              |
| <dl> <dt>**E \_ 指標**</dt> </dl> | *PTime* 參數為 **Null**。<br/> |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IReferenceClock 介面**](ireferenceclock.md)
</dt> </dl>

 

 






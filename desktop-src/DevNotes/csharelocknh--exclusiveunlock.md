---
description: 釋放使用 ExclusiveLock 至共用模式所取得的鎖定。
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: CShareLockNH：： ExclusiveUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983165"
---
# <a name="csharelocknhexclusiveunlock-method"></a>CShareLockNH：： ExclusiveUnlock 方法

釋放使用 [**ExclusiveLock**](csharelocknh--exclusivelock.md) 至共用模式所取得的鎖定。

## <a name="syntax"></a>語法


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

對 [**ExclusiveLock**](csharelocknh--exclusivelock.md) 的每個呼叫都必須成對 **ExclusiveUnlock** ，以避免發生鎖死的風險。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 

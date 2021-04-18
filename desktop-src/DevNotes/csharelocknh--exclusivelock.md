---
description: 取得讀取器/寫入器鎖定。
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: CShareLockNH：： ExclusiveLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976205"
---
# <a name="csharelocknhexclusivelock-method"></a>CShareLockNH：： ExclusiveLock 方法

取得讀取器/寫入器鎖定。

## <a name="syntax"></a>語法


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

對 **ExclusiveLock** 的每個呼叫都必須成對 [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) ，以避免發生鎖死的風險。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 

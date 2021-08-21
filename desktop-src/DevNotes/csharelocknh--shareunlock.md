---
description: 釋放共用鎖定。
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: CShareLockNH：： ShareUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162183"
---
# <a name="csharelocknhshareunlock-method"></a>CShareLockNH：： ShareUnlock 方法

釋放共用鎖定。

## <a name="syntax"></a>語法


```C++
void ShareUnlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每次呼叫 [**ShareLock**](csharelocknh--sharelock.md) 都必須與 **ShareUnlock** 的單一呼叫配對。 只有成功呼叫 **ShareLock** 的執行緒可以呼叫 **ShareUnlock**;否則，可能會發生鎖死。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 

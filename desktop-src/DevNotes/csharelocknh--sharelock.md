---
description: 取得共用鎖定。
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: CShareLockNH：： ShareLock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992892"
---
# <a name="csharelocknhsharelock-method"></a>CShareLockNH：： ShareLock 方法

取得共用鎖定。

## <a name="syntax"></a>語法


```C++
void ShareLock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

每次呼叫 **ShareLock** 都必須與 [**ShareUnlock**](csharelocknh--shareunlock.md)的單一呼叫配對。 只有成功呼叫 **ShareLock** 的執行緒可以呼叫 **ShareUnlock**;否則，可能會發生鎖死。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 

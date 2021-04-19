---
description: 釋放部分鎖定，讓其他專有或部分鎖定商家現在可以進入。
ms.assetid: 95a3e0d1-4e8b-4e30-b4fd-709b9db465de
title: CShareLockNH：:P artialUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 930c0f51e199c1668a70f2dd017b0280939b0710
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987090"
---
# <a name="csharelocknhpartialunlock-method"></a>CShareLockNH：:P artialUnlock 方法

釋放部分鎖定，讓其他專有或部分鎖定商家現在可以進入。

## <a name="syntax"></a>語法


```C++
void PartialUnlock();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 

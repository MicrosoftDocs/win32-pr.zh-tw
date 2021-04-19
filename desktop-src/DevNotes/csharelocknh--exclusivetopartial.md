---
description: 將獨佔鎖定變更為部分鎖定。
ms.assetid: 46f0c354-6cb6-4d23-888a-88a2629a46b8
title: CShareLockNH：： ExclusiveToPartial 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: ae337917ee443544ebbd031dd0d95f4e20918570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990967"
---
# <a name="csharelocknhexclusivetopartial-method"></a>CShareLockNH：： ExclusiveToPartial 方法

將獨佔鎖定變更為部分鎖定。

## <a name="syntax"></a>語法


```C++
void ExclusiveToPartial();
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



 

 

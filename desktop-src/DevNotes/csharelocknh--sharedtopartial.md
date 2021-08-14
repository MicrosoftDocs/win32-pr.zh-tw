---
description: 將共用鎖定變更為部分鎖定。
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: CShareLockNH：： SharedToPartial 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8f2cc895786655754a3fcf56c6efe745467c12328867b1dc021a257ba1519652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162203"
---
# <a name="csharelocknhsharedtopartial-method"></a>CShareLockNH：： SharedToPartial 方法

將共用鎖定變更為部分鎖定。

## <a name="syntax"></a>語法


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果已取得部分鎖定，則傳回 **TRUE** ;否則，它會傳回 **FALSE** ，而且鎖定會維持在共用模式中。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 

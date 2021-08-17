---
description: 指出目前的使用者是否為系統管理員。
ms.assetid: e759a6b9-19c3-4a2e-b8cf-1398037f88ee
title: pSetupIsUserAdmin 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupIsUserAdmin
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 152feb3a0c473540b27e04befb2cf012bdd13aa3a0979cd88736b7521159f7bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386479"
---
# <a name="psetupisuseradmin-function"></a>pSetupIsUserAdmin 函式

\[Windows Vista 或 Windows Server 2008 中無法使用此功能。\]

指出目前的使用者是否為系統管理員。

## <a name="syntax"></a>語法


```C++
BOOL pSetupIsUserAdmin(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果目前的使用者是系統管理員，**則為 TRUE** ，否則為 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 

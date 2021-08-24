---
description: pSetupStringTableInitialize 函式-初始化字串資料表。
ms.assetid: 1a626243-b4ad-4e3d-a933-b81b75cae399
title: pSetupStringTableInitialize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitialize
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 8dd3ea3cadbcbbeccf5801538ac45720dd4ead1c31b004c9c4ac999c0af1f029
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386258"
---
# <a name="psetupstringtableinitialize-function"></a>pSetupStringTableInitialize 函式

\[Windows Vista 或 Windows Server 2008 中無法使用此功能。\]

初始化字串資料表。

## <a name="syntax"></a>語法


```C++
PVOID WINAPI pSetupStringTableInitialize(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 

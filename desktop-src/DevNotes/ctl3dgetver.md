---
description: 指出目前正在執行的 CTL3D 版本。
ms.assetid: 38c0842c-417f-4ca1-acc2-3bbadf45c804
title: Ctl3dGetVer 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dGetVer
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: f29963020290686521d5e3bd165d2c8fac6e5e0c96f34552ad11f725d95567cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654498"
---
# <a name="ctl3dgetver-function"></a>Ctl3dGetVer 函式

指出目前正在執行的 CTL3D 版本。

## <a name="syntax"></a>語法


```C++
WORD Ctl3dGetVer(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

傳回值，其中包含高序位位元組的主要版本號碼，以及低序位位元組中的次要版本號碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 

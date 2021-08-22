---
description: GetDllVersion 函式會捕獲 Cabinet.dll 的版本號碼。
ms.assetid: b324d5cd-1ede-473e-a10f-249c95eda057
title: GetDllVersion 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDllVersion
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 14f2da8c6f8c786042c2abd5f41e02bdfab6f33d9b8aa42a5b5f90a6c4357103
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119390708"
---
# <a name="getdllversion-function"></a>GetDllVersion 函式

\[不再支援此函式，因此無法保證其行為。 \]

**GetDllVersion** 函式會捕獲 Cabinet.dll 的版本號碼。

## <a name="syntax"></a>語法


```C++
LPCSTR WINAPI GetDllVersion(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

檔案的版本號碼 (參閱 [VERSIONINFO 資源](../menurc/versioninfo-resource.md)) 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DllGetVersion**](dllgetversion.md)
</dt> </dl>

 

 

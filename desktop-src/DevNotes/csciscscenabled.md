---
description: 判斷是否已啟用離線檔案。
ms.assetid: c7d3173d-ed51-4de6-ad07-4c5e6906b0f4
title: CSCIsCSCEnabled 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCIsCSCEnabled
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 8678e48aedf6bda6cdb8beb5b78bb310a16d2829ebf6f3e5b0b8525c135aaf03
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815458"
---
# <a name="csciscscenabled-function"></a>CSCIsCSCEnabled 函式

\[這項功能不受支援，因此不應該使用。\]

判斷是否已啟用離線檔案。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CSCIsCSCEnabled(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果已啟用離線檔案，此函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CSCQueryDatabaseStatus**](cscquerydatabasestatus.md)
</dt> </dl>

 

 

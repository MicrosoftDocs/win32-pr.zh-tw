---
description: 取得模組路徑。
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a10ff54d7f118dc71e12cdb5b29e28d3b3dd6e60c7b51c263af8c62c1264968c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911918"
---
# <a name="_getmodulefilename-function"></a>\_GetModuleFileName 函式

\[此函式是 **GetModuleFileName** 函數的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **GetModuleFileName** 。\]

取得模組路徑。 請參閱 [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)。

## <a name="syntax"></a>語法


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*...* 
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 

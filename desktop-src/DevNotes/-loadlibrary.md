---
description: 載入程式庫。
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 67755d96d87530f450627714de7c1526750967b87bdf51901b788662c4534045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827979"
---
# <a name="_loadlibrary-function"></a>\_LoadLibrary 函式

\[此函式是 **LoadLibrary** 函數的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **LoadLibrary** 。\]

載入程式庫。 請參閱 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)。

## <a name="syntax"></a>語法


```C++
HMODULE _LoadLibrary(
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

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 

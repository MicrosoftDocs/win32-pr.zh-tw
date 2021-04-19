---
description: 取得作業系統版本的相關資訊。
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993982"
---
# <a name="_getversionex-function"></a>\_GetVersionEx 函數

\[此函式是透過 **GetVersionEx** 函式的包裝函式。 這項功能可能會在未來變更或無法使用。 應用程式應該直接呼叫 **GetVersionEx** 。\]

取得作業系統版本的相關資訊。 請參閱 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)。

## <a name="syntax"></a>語法


```C++
BOOL _GetVersionEx(
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

[**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 

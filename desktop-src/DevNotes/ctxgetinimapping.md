---
description: 判斷終端機伺服器是否僅在 Windows 終端機 Server 4.0) 上 (安裝模式。
ms.assetid: f6cb7971-d4f5-49ca-938a-9c280028764a
title: CtxGetIniMapping 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CtxGetIniMapping
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 7085e595b1f9c1fb8ea36e59aae4a90c816b508c92bcd33a99fe5051f2b722d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654208"
---
# <a name="ctxgetinimapping-function"></a>CtxGetIniMapping 函式

\[這項功能不受支援，因此不應該使用。 它可能會在未事先通知的情況下，完全變更或消失。 相反地，請使用 **VerifyVersionInfo**。\]

判斷終端機伺服器是否僅在 Windows 終端機 Server 4.0) 上 (安裝模式。

## <a name="syntax"></a>語法


```C++
BOOLEAN CtxGetIniMapping(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

如果終端機伺服器處於 [安裝] 模式，則此函式會傳回 **FALSE** ，如果是在執行模式， **則為 TRUE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**VerifyVersionInfo**](/windows/win32/api/winbase/nf-winbase-verifyversioninfoa)
</dt> </dl>

 

 

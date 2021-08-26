---
description: 釋放 SdbGetMatchingExe 函式所使用的資源。
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 710874fc0e57775eb6ad1c9c6681a5b74dc66d133b22ce23d2ac0d27270ef7f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044918"
---
# <a name="sdbreleasematchingexe-function"></a>SdbReleaseMatchingExe 函式

釋放 [**SdbGetMatchingExe**](sdbgetmatchingexe.md) 函式所使用的資源。

## <a name="syntax"></a>語法


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSDB* \[在\]
</dt> <dd>

[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。

</dd> <dt>

*trExe* \[在\]
</dt> <dd>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)傳回的 [**TAGREF**](tagref.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbGetMatchingExe**](sdbgetmatchingexe.md)
</dt> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 





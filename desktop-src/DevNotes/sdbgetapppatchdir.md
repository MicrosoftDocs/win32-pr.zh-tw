---
description: 捕獲系統 AppPatch 目錄。
ms.assetid: 1c79411f-1f90-4b90-84c7-24a34cf0d91d
title: SdbGetAppPatchDir 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetAppPatchDir
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 60a3b14bcca1be3ecb8d33b0d3f344f08bc11b28
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109924"
---
# <a name="sdbgetapppatchdir-function"></a>SdbGetAppPatchDir 函式

捕獲系統 AppPatch 目錄。

## <a name="syntax"></a>語法


```C++
void WINAPI SdbGetAppPatchDir(
  _In_opt_ HSDB   hSDB,
  _Out_    LPTSTR szAppPatchPath,
  _In_     DWORD  cchSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSDB* \[在中，選擇性\]
</dt> <dd>

[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。

</dd> <dt>

*szAppPatchPath* \[擴展\]
</dt> <dd>

產生的路徑。

</dd> <dt>

*cchSize* \[在\]
</dt> <dd>

*SzAppPatchPath* 緩衝區的大小（以字元為單位）。 如果函式失敗，這個參數會設為空字串 ( "" ) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> </dl>

 

 





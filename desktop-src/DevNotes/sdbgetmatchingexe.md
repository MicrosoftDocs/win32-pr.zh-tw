---
description: 搜尋指定的可執行檔。
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847257"
---
# <a name="sdbgetmatchingexe-function"></a>SdbGetMatchingExe 函式

搜尋指定的可執行檔。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hSDB* \[在中，選擇性\]
</dt> <dd>

[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。

</dd> <dt>

*szPath* \[在\]
</dt> <dd>

可執行檔的路徑。

</dd> <dt>

*szModuleName* \[在中，選擇性\]
</dt> <dd>

模組名稱。

</dd> <dt>

*pszEnvironment* \[在中，選擇性\]
</dt> <dd>

要用作搜尋內容的環境變數。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

此參數可以是0或 **SDBGMEF \_ 忽略 \_ 環境** (0x1) 。

</dd> <dt>

*pQueryResult* \[擴展\]
</dt> <dd>

[**SDBQUERYRESULT**](sdbqueryresult.md)結構。 如果找不到相符項，則結構會包含 **TAGREF \_ Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

當您完成傳回的 [**TAGREF**](tagref.md)時，請使用 [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) 函式來釋放它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbInitDatabase**](sdbinitdatabase.md)
</dt> <dt>

[**SdbReleaseMatchingExe**](sdbreleasematchingexe.md)
</dt> </dl>

 

 





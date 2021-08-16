---
title: Str_GetPtr 函式
description: 將字串從一個緩衝區複製到另一個緩衝區。
ms.assetid: a3dd55a0-3f8b-4d6c-9956-666bebc3ab8d
keywords:
- Str_GetPtr 函式 Windows 控制項
topic_type:
- apiref
api_name:
- Str_GetPtr
- Str_GetPtrA
- Str_GetPtrW
api_location:
- ComCtl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77c76ad276f6cb6dfc12bc272fbbc86c83617a0d00d36d77cf2ab0ca113811d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919448"
---
# <a name="str_getptr-function"></a>Str \_ GetPtr 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在 Windows 的後續版本中變更或無法使用。\]

將字串從一個緩衝區複製到另一個緩衝區。

## <a name="syntax"></a>語法


```C++
int WINAPI Str_GetPtr(
  _In_    LPCTSTR pszSource,
  _Inout_ LPCSTR  pszDest,
  _In_    int     cchDest
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszSource* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

來源字串的指標。

</dd> <dt>

*pszDest* \[in、out\]
</dt> <dd>

類型： **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

目的地緩衝區的指標。 這個值可以是 **Null**。

</dd> <dt>

*cchDest* \[在\]
</dt> <dd>

類型： **int**

*PszDest* 的大小（以字元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果 *pszDest* 為 **Null** 或 *cchDest* 為零，則會傳回所需的緩衝區大小（以字元為單位），以包含 *pszSource* 所指向之字串的以 Null 終止的複本。

如果 *pszDest* 為非 **Null**，則會傳回成功複製的字元數，包括結束的 Null 字元。

如果 *pszDest* 無法保存 *pszSource* 所指向的整個字串，則會複製 (的 *cchDest*-1) 字元、以 null 終止的字串，以及傳回的 *cchDest* 。

## <a name="remarks"></a>備註

**Str \_GetPtr** 可做為 ANSI (**str \_ GetPtrA**) 和 Unicode (**str \_ GetPtrW**) 版本。 這些函式不會依名稱匯出，也不會在公用標頭檔中宣告。 若要使用它們，您必須使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數 233 (**Str \_ GetPtrA**) 或 235 (**str \_ GetPtrW**) 自 ComCtl32.dll 取得函式指標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>ComCtl32.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Str \_GetPtrW** (Unicode) 和 **Str \_ GetPtrA** (ANSI) <br/>                       |



 


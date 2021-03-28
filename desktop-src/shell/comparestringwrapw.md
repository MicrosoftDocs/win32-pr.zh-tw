---
description: 使用指定的地區設定，比較兩個 Unicode 字元字串。
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 0731182f5c01ad56db722972628d2cbe39373835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972064"
---
# <a name="comparestringwrapw-function"></a>CompareStringWrapW 函式

\[**CompareStringWrapW** 可用於 Windows XP。 在後續版本中將無法使用。 您應該在其位置使用 [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 。\]

使用指定的地區設定，比較兩個 Unicode 字元字串。

> [!Note]  
> **CompareStringWrapW** 是 **CompareStringW** 函數的包裝函式。 如需進一步的使用注意事項，請參閱 [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 頁面。

 

## <a name="syntax"></a>語法


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

類型： **LCID**

用於比較的地區設定識別碼。 這個參數可以是下列其中一個預先定義的地區設定識別碼，或 [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) 宏所建立的地區設定識別碼。

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**地區設定 \_ 系統 \_ 預設值**


</dt> <dd>

系統的預設地區設定。

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**地區設定 \_ 使用者 \_ 預設值**


</dt> <dd>

目前使用者的預設地區設定。

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[在\]
</dt> <dd>

類型： **DWORD**

旗標，指出函數如何比較兩個字串。 依預設，不會設定這些旗標。 設定為零以取得預設行為或下列值的任何組合。

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**標準 \_ IGNORECASE**


</dt> <dd>

忽略大小寫。

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**標準 \_ IGNOREKANATYPE**


</dt> <dd>

請勿區分平假名和片假名字元。 對應的平假名和片假名字元比較為相等。

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**標準 \_ IGNORENONSPACE**


</dt> <dd>

忽略非空白字元。

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**標準 \_ IGNORESYMBOLS**


</dt> <dd>

忽略符號。

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**標準 \_ IGNOREWIDTH**


</dt> <dd>

請勿區分單一位元組字元和與雙位元組字元相同的字元。

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**排序 \_ STRINGSORT**


</dt> <dd>

將標點符號視為與符號相同。

</dd> </dl> </dd> <dt>

*lpString1* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要比較之第一個 Unicode 字串的指標。

</dd> <dt>

*cchCount1* \[在\]
</dt> <dd>

類型： **int**

*LpString1* 參數所指向之字串中的字元數。 此計數不包含終止的 null 字元。 如果此參數為負值，則會假設字串是以 null 終止，且會自動計算長度。

</dd> <dt>

*lpString2* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要比較之第二個 Unicode 字串的指標。

</dd> <dt>

*cchCount2* \[在\]
</dt> <dd>

類型： **int**

*LpString2* 參數所指向之字串中的字元數。 此計數不包含終止的 null 字元。 如果此參數為負值，則會假設字串是以 null 終止，且會自動計算長度。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 **GetLastError** 可能會傳回下列其中一個錯誤碼。

-   錯誤 \_ 不正確 \_ 旗標
-   錯誤 \_ 不正確 \_ 參數

如果函式成功，則傳回值是下列其中一個值。 

| 需求 | 值 |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ 小於 \_    | *LpString1* 參數所指向的字串，在詞法值中小於 *lpString2* 參數所指向的字串。 |
| CSTR \_ 等於         | *LpString1* 所指向的字串在詞法值中等於 *lpString2* 所指向的字串。                              |
| CSTR \_ 大於 \_ | *LpString1* 所指向的字串在詞法值中大於 *lpString2* 所指向的字串                           |



 

## <a name="remarks"></a>備註

**安全性警告：** 使用此函式不正確，可能會危及應用程式的安全性。 未正確比較的字串可能會產生不正確輸入。 測試字串以確保它們在使用之前都有效，並提供錯誤處理常式。 如需詳細資訊，請參閱 [安全性考慮：國際功能](../intl/security-considerations--international-features.md)

慣用的方法是使用 [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 搭配適用于 UNICODE (MSLU) 的 Microsoft 層。

您必須使用序數45，直接從 Shlwapi.dll 呼叫 **CompareStringWrapW** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 

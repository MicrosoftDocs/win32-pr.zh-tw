---
description: 為指定的使用者建立使用者設定檔。
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: CreateUserProfileEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974845"
---
# <a name="createuserprofileex-function"></a>CreateUserProfileEx 函式

\[從 Windows Vista 起，無法使用此函式。\]

為指定的使用者建立使用者設定檔。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSid* \[在\]
</dt> <dd>

類型： **PSID**

新使用者的 SID。

</dd> <dt>

*lpUserName* \[在\]
</dt> <dd>

類型： **LPCTSTR**

包含新使用者的使用者名稱之緩衝區的指標。

</dd> <dt>

*lpUserHive* \[在中，選擇性\]
</dt> <dd>

類型： **LPCTSTR**

包含要使用之登錄 [hive](../sysinfo/registry-hives.md) 的緩衝區指標。 此參數可以是 **Null**。

</dd> <dt>

*lpProfileDir* \[out、optional\]
</dt> <dd>

類型： **LPTSTR**

緩衝區的指標，此函式傳回時，會接收使用者的設定檔目錄路徑。 此參數可以是 **Null**。

</dd> <dt>

*dwDirSize* \[在\]
</dt> <dd>

類型： **DWORD**

*LpProfileDir* 在 TCHARs 中指定的緩衝區大小。

</dd> <dt>

*bWin9xUpg* \[在\]
</dt> <dd>

類型： **BOOL**

如果在從 Windows 9x 進行設定檔的過程中建立使用者設定檔，則為 **TRUE** ;否則 **為 FALSE**。

若 **為 TRUE**，則會在預設的設定檔目錄（通常是 C： \\ Documents 和 Settings \\ *UserName*）中設定使用者設定檔。 如果該目錄已存在，則會使用它。 如果沒有，則會建立它。

如果 **為 FALSE**，則會建立預設的設定檔目錄（如果不存在的話）。 如果預設的設定檔目錄已存在，則會建立此使用者設定檔的新目錄。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果已成功建立新的使用者設定檔，則傳回 **TRUE** ;否則 **為 FALSE**。

## <a name="remarks"></a>備註

此函式未在軟體發展工具組中宣告 (SDK) 標頭，且沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數連結至 Userenv.dll。 函數的 ANSI 版本， **CreateUserProfileExA** 會從 Userenv.dll 參考為序數153。 Unicode 版本 **CreateUserProfileExW** 是以序數154的形式參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/>  | Windows XP<br/>                                                                  |
| DLL<br/>                    | <dl> <dt>Userenv.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/> | **CreateUserProfileExW** (Unicode) 和 **CreateUserProfileExA** (ANSI) <br/>      |



 

 

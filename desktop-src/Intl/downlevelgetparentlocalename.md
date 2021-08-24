---
description: 抓取所提供地區設定之父系的地區設定名稱。
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: 'DownlevelGetParentLocaleName 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898738"
---
# <a name="downlevelgetparentlocalename-function"></a>DownlevelGetParentLocaleName 函式

抓取所提供地區設定之父系的 [地區設定名稱](locale-names.md) 。

> [!Note]  
> 此函式僅適用于在預先 Windows Vista 作業系統上執行的應用程式。 其用途需要下載套件。 只在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SPARENT](locale-sparent.md)。

 

## <a name="syntax"></a>語法


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

地區設定的[地區設定識別碼](locale-identifiers.md)。 您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，或使用下列其中一個預先定義的值。

-   [地區設定不 \_ 變](locale-invariant.md)
-   [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)
-   [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)

**Windows Vista 和更新版本：** 也支援下列自訂地區設定識別碼。

-   [地區設定 \_ 自訂 \_ 預設值](locale-custom-constants.md)
-   [地區設定 \_ 自訂 \_ UI \_ 預設值](locale-custom-constants.md)
-   [未指定地區設定的 \_ 自訂 \_](locale-custom-constants.md)

</dd> <dt>

*lpName* \[擴展\]
</dt> <dd>

緩衝區的指標，函式會在其中抓取父地區設定名稱，或下列其中一個預先定義的值。 如果 *cchName* 設為0，則這個參數會設定為 **Null** 。

-   [地區設定 \_ 名稱不 \_ 變](locale-name-constants.md)
-   [地區設定 \_ 名稱 \_ 系統 \_ 預設值](locale-name-constants.md)
-   [地區設定 \_ 名稱 \_ 使用者 \_ 預設值](locale-name-constants.md)

</dd> <dt>

*cchName* \[在\]
</dt> <dd>

*LpName* 在 utf-16 程式碼點中指出的緩衝區大小。 這個參數的值為0時，會導致函式忽略 *lpName* 緩衝區，並傳回緩衝區的大小（以包含父地區設定名稱的字元 (null 字元) ）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回地區設定名稱中 UTF-16 程式碼點的計數，如果成功，則包含終止的 null 字元。

如果不成功，則此函式會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   \_緩衝區不足 \_ 的錯誤。 提供的緩衝區大小不夠大，或未正確設定為 **Null**。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Microsoft NLS 下層資料對應 Api 于 windows XP SP2 和更新版本<br/>  |
| 標頭<br/>                   | <dl> <dt>Nlsdl。h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[對應地區設定資料](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

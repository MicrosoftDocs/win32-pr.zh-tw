---
description: 將地區設定識別碼轉換為地區設定名稱。
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: 'DownlevelLCIDToLocaleName 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898718"
---
# <a name="downlevellcidtolocalename-function"></a>DownlevelLCIDToLocaleName 函式

將 [地區設定識別碼](locale-identifiers.md) 轉換為 [地區設定名稱](locale-names.md)。

> [!Note]  
> 此函式僅適用于在預先 Windows Vista 作業系統上執行的應用程式。 其用途需要下載套件。 只在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)來取得地區設定名稱。

 

## <a name="syntax"></a>語法


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

要轉譯的地區設定識別碼。 您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼。 此函式不支援中性地區設定或下列特定地區設定識別碼值。

-   [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)
-   [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)
-   [地區設定 \_ 自訂 \_ 預設值](locale-custom-constants.md)
-   [地區設定 \_ 自訂 \_ UI \_ 預設值](locale-custom-constants.md)
-   [未指定地區設定的 \_ 自訂 \_](locale-custom-constants.md)

</dd> <dt>

*lpName* \[擴展\]
</dt> <dd>

緩衝區的指標，此函式會在此函數中抓取地區設定名稱。 如果 *cchName* 設為0，則函式會抓取 **Null** 。

</dd> <dt>

*cchName* \[在\]
</dt> <dd>

地區設定名稱緩衝區的大小（以 UTF-16 編碼點）。 應用程式會將此參數設定為0，以傳回地區設定名稱緩衝區所需的大小。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

旗標，指定要取出的名稱類型。 預設值為下層 \_ 地區設定 \_ 名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回地區設定名稱中 UTF-16 程式碼點的計數，如果成功，則包含終止的 null 字元。 如果函式成功，而且 *cchName* 的值為0，則傳回值會是所需的大小（以字元為單位）， (包含 null 字元) ）作為地區設定名稱緩衝區。

如果不成功，函數會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   \_緩衝區不足 \_ 的錯誤。 提供的緩衝區大小不夠大，或未正確設定為 **Null**。
-   錯誤 \_ 無效 \_ 的旗標。 *DwFlags* 的值無效。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

> [!Note]  
> 此函數不支援 [自訂地區](custom-locales.md)設定。

 

必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                |
| 可轉散發套件<br/>          | Microsoft NLS 下層資料對應 Api 于 windows XP SP2 和 laterorWindows Vista<br/> |
| 標頭<br/>                   | <dl> <dt>Nlsdl。h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[對應地區設定資料](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 

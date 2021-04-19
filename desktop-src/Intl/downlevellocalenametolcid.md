---
description: 將地區設定名稱轉換成可以用來從作業系統取得資訊的地區設定識別碼。
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: 'DownlevelLocaleNameToLCID 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: c41b82c59b63a5b324e15f89c1f77118d454e428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980633"
---
# <a name="downlevellocalenametolcid-function"></a>DownlevelLocaleNameToLCID 函式

將 [地區設定名稱](locale-names.md) 轉換成可以用來從作業系統取得資訊的 [地區設定識別碼](locale-identifiers.md) 。

> [!Note]  
> 只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。 其用途需要下載套件。 只在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 來取出地區設定識別碼。

 

## <a name="syntax"></a>語法


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpName* \[在\]
</dt> <dd>

表示 [地區設定名稱](locale-names.md)之以 null 結束的字串指標。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定名稱類型的旗標。 預設值為下層 \_ 地區設定 \_ 名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回對應至地區設定名稱的地區設定識別碼。

如果不成功，函數會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ 無效 \_ 的旗標。 為旗標提供的值無效。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

> [!Note]  
> 此函數不支援中性地區設定。 對等的 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 函式支援 [自訂地區](custom-locales.md)設定，但僅適用于 Windows Vista 和更新版本。

 

必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                |
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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 

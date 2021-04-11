---
description: 抓取所提供地區設定之父系的地區設定識別碼。
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: 'DownlevelGetParentLocaleLCID 函式 (Nlsdl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320235"
---
# <a name="downlevelgetparentlocalelcid-function"></a>DownlevelGetParentLocaleLCID 函式

抓取所提供地區設定之父系的 [地區設定識別碼](locale-identifiers.md) 。

> [!Note]  
> 只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。 其用途需要下載套件。 只有在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SPARENT](locale-sparent.md)。

 

## <a name="syntax"></a>語法


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*地區* \[ 設定在\]
</dt> <dd>

要取得其父地區設定識別碼之地區設定的地區設定識別碼。 您可以使用 [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) 宏來建立地區設定識別碼，或使用下列其中一個預先定義的值。

-   [地區設定不 \_ 變](locale-invariant.md)
-   [地區設定 \_ 系統 \_ 預設值](locale-system-default.md)
-   [地區設定 \_ 使用者 \_ 預設值](locale-user-default.md)

**Windows Vista 和更新版本：** 也支援下列自訂地區設定識別碼。

-   [地區設定 \_ 自訂 \_ 預設值](locale-custom-constants.md)
-   [地區設定 \_ 自訂 \_ UI \_ 預設值](locale-custom-constants.md)
-   [未指定地區設定的 \_ 自訂 \_](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回父地區設定識別碼，否則為0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

必要的標頭檔和 DLL 是「Microsoft NLS 下層資料對應 Api」下載的一部分，可在 [Microsoft 下載中心](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Microsoft NLS 下層資料對應 Api 于 windows XPor Windows Vista<br/>     |
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

 

 

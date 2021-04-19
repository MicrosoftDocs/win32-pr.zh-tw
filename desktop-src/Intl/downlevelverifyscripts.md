---
description: 比較兩個腳本的列舉清單。
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: 'DownlevelVerifyScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 62e029576d53109e3c57faf4ec913472f8aea65e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980000"
---
# <a name="downlevelverifyscripts-function"></a>DownlevelVerifyScripts 函式

比較兩個腳本的列舉清單。

> [!Note]  
> 只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。 其用途需要下載套件。 只在 Windows Vista 和更新版本上執行的應用程式應該呼叫 [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)。

 

## <a name="syntax"></a>語法


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定腳本驗證選項的旗標。



| 值                                                                                                                                                             | 意義                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ 允許 \_ 拉丁**</dt> </dl> | 在測試清單中允許 "Latn" (拉丁腳本) ，即使它不在地區設定清單中也一樣。<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[在\]
</dt> <dd>

地區設定清單的指標，也就是指定地區設定的腳本列舉清單。 這份清單通常會藉由呼叫 [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)來填入。

</dd> <dt>

*cchLocaleScripts* \[在\]
</dt> <dd>

*LpLocaleScripts* 所表示之字串的大小（以字元為單位）。 如果字串是以 null 終止，則應用程式會將此參數設定為-1。 如果此參數設定為0，則函數會失敗。

</dd> <dt>

*lpTestScripts* \[在\]
</dt> <dd>

測試清單的指標，也就是腳本的第二個列舉清單。 這份清單通常會藉由呼叫 [**DownlevelGetStringScripts**](downlevelgetstringscripts.md)來填入。

</dd> <dt>

*cchTestScripts* \[在\]
</dt> <dd>

*LpTestScripts* 所表示之字串的大小（以字元為單位）。 如果字串是以 null 終止，則應用程式會將此參數設定為-1。 如果此參數設定為0，則函數會失敗。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果測試清單不是空白，而且清單中的所有專案也包含在地區設定清單中，則傳回 **TRUE** 。 否則，函數會傳回 **FALSE**。

如果傳回值為 **FALSE** ，則表示測試清單包含不在地區設定清單中的專案，或可能表示發生錯誤。 若要區分這兩種情況，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。 如果 **DownlevelVerifyScripts** 成功判斷出測試清單中的專案不在地區設定清單中，則 **GETLASTERROR** 會傳回錯誤 \_ SUCCESS。 否則， **GetLastError** 可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ 無效 \_ 的旗標。 為旗標提供的值無效。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

此函數會比較字串，例如 "Latn;Cyrl; "，其中包含一連串4個字元的腳本名稱，每個腳本名稱後面加上分號。 此外，它也有特殊的案例，因為拉丁腳本通常用於不是原生的語言和地區設定。

這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。

以下是此函式的傳回範例，以及在各種案例中對 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 的後續呼叫。 最後兩個範例分別說明測試清單缺少結束分號 (格式錯誤的字串) 和測試清單空白的案例。



| "Locale" 字串 | "Test" 字串 | *dwFlags*        | 傳回值 | GetLastError return       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani;Hira;區分 | Hani;         | N/A              | **TRUE**     | N/A                       |
| Hani;Hira;區分 | Hani;Latn;    | 0                | **FALSE**    | 錯誤 \_ 成功            |
| Hani;Hira;區分 | Hani;Latn;    | VS \_ 允許 \_ 拉丁 | **TRUE**     | N/A                       |
| Hani;Hira;區分 | Cyrl;         | N/A              | **FALSE**    | 錯誤 \_ 成功            |
| Hani;Hira;區分 | Cyrl;         | N/A              | **FALSE**    | 錯誤 \_ 不正確 \_ 參數 |
| Hani;Hira;區分 |               | N/A              | **FALSE**    | 錯誤 \_ 成功            |



 

必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                                         |
| 可轉散發套件<br/>          | Microsoft 國際化功能變數名稱 (IDN) 緩和 Api 于 windows XP SP2、Windows Server 2003 SP1、orWindows Vista<br/> |
| 標頭<br/>                   | <dl> <dt>Idndl。h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[處理國際化功能變數名稱 (IDNs) ](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 

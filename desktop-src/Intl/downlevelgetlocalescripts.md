---
description: 提供指定之地區設定的腳本清單。
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: 'DownlevelGetLocaleScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194550"
---
# <a name="downlevelgetlocalescripts-function"></a>DownlevelGetLocaleScripts 函式

提供指定之地區設定的腳本清單。

> [!Note]  
> 只有在 Windows Vista 之前的作業系統上執行的應用程式，才會使用此函式。 其用途需要下載套件。 只有在 Windows Vista 和更新版本上執行的應用程式，應該呼叫 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ，並將 *LCType* 設定為 [地區設定 \_ SSCRIPTS](locale-sscripts.md)。

 

## <a name="syntax"></a>語法


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpLocaleName* \[在\]
</dt> <dd>

以 null 結束之地區設定 [名稱](locale-names.md)的指標。

</dd> <dt>

*lpScripts* \[擴展\]
</dt> <dd>

緩衝區的指標，此函式會使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法，來抓取表示腳本清單的以 null 終止的字串。 每個腳本名稱都是由四個拉丁字元所組成，而且名稱會依字母順序抓取。 其中每個專案（包括最後一個）後面都會加上分號。

或者，如果 *cchScripts* 設為0，則此參數可以包含 **Null** 。 在此情況下，函數會傳回腳本緩衝區所需的大小。

</dd> <dt>

*cchScripts* \[在\]
</dt> <dd>

*LpScripts* 所指出的腳本緩衝區大小（以字元為單位）。

或者，應用程式可以將此參數設定為0。 在此情況下，此函式會在 *lpScripts* 中抓取 **Null** ，並傳回腳本緩衝區所需的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回腳本緩衝區中取出的字元數，包括結束的 null 字元。 如果函式成功，且 *cchScripts* 的值為0，則傳回值為腳本緩衝區所需的大小（以字元為單位，包括結束的 null 字元）。

如果不成功，則此函式會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ BADDB。 函數無法存取資料。 通常不會發生這種情況，通常表示安裝不良、磁片問題或類似。
-   \_緩衝區不足 \_ 的錯誤。 提供的緩衝區大小不夠大，或未正確設定為 **Null**。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。

以下是此函式之輸入和輸出的一些範例，假設有足夠的緩衝區大小：



| Locale                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| 英文 (美國) | zh-TW          | Latn;           |
| 印度文 (印度)           | hi-IN          | Deva;           |
| 日文 (日本)        | ja-JP          | Hani;Hira;區分 |



 

此清單不包含拉丁腳本，除非它是用於地區設定之書寫系統的必要部分。 但是，拉丁字元通常用於不是原生的地區設定內容中，而不是外部業務名稱。 在上述範例中，針對印度文的印度文，唯一抓取的腳本是「Deva」 (適用于梵文) ，不過拉丁字元也可以出現在印度文文字中。 [**DownlevelVerifyScripts**](downlevelverifyscripts.md)函式具有特殊旗標，可解決該情況。

必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                                                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                                                                        |
| 可轉散發套件<br/>          | Microsoft 國際化功能變數名稱 (IDN) Windows XP (SP2 或更新版本) 、Windows Server 2003 (SP1 或更新版本) 或 Windows Vista 上的緩和 Api<br/> |
| 標頭<br/>                   | <dl> <dt>Idndl。h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[處理國際化功能變數名稱 (IDNs) ](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 

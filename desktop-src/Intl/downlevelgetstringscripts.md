---
description: 提供指定之 Unicode 字串中所使用的腳本清單。
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: 'DownlevelGetStringScripts 函式 (Idndl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: 23eca82d97ac1da2d0f179c6e670ed032a57410490dcc5a52cf3005d75d65b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041618"
---
# <a name="downlevelgetstringscripts-function"></a>DownlevelGetStringScripts 函式

提供指定之 Unicode 字串中所使用的腳本清單。

> [!Note]  
> 此函式僅適用于在預先 Windows Vista 作業系統上執行的應用程式。 其用途需要下載套件。 只在 Windows Vista 和更新版本上執行的應用程式應該呼叫 [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)。

 

## <a name="syntax"></a>語法


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定腳本抓取選項的旗標。



| 值                                                                                                                                                                                                  | 意義                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ 允許 \_ 繼承 \_ 通用**</dt> </dl> | 取出 "Qaii" (繼承) 和 "Zyyy" (通用) 腳本資訊。 此值不會影響未指派字元的處理。 輸入字串中的這些字元一律會導致「Zzzz」 (未指派的腳本) 出現在腳本字串中。<br/> |



 

> [!Note]  
> 根據預設，此函式會忽略輸入 Unicode 字串中的任何繼承或一般字元。 如果 \_ \_ \_ 未設定 [GSS 允許繼承的一般]，即使輸入字串包含這類字元，腳本字串中都不會出現 "Qaii" 或 "Zyyy"。 如果 \_ 已設定 [GSS 允許 \_ 繼承 \_ 一般]，而且輸入字串包含繼承和/或通用字元，則腳本字串中會出現 "Qaii" 和/或 "Zyyy"。 請參閱＜備註＞一節。

 

</dd> <dt>

*lpString* \[在\]
</dt> <dd>

要分析的 Unicode 字串指標。

</dd> <dt>

*cchString* \[在\]
</dt> <dd>

*LpString* 所表示之 Unicode 字串的大小（以字元為單位）。 如果字串是以 null 終止，則應用程式會將此參數設定為-1。 如果應用程式將此參數設定為0，則函式會 \\ 在 *lpScripts* 中 )  (L "0" 的 null Unicode 字串，並傳回1。

</dd> <dt>

*lpScripts* \[擴展\]
</dt> <dd>

緩衝區的指標，此函式會使用 [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html)中使用的4個字元標記法，來抓取表示腳本清單的以 null 終止的字串。 每個腳本名稱都是由四個拉丁字元所組成，而且名稱會依字母順序抓取。 每個名稱（包括最後一個）後面都會加上分號。

或者，如果 *cchScripts* 設為0，則此參數可以包含 **Null** 。 在此情況下，函數會傳回腳本緩衝區所需的大小。

</dd> <dt>

*cchScripts* \[在\]
</dt> <dd>

*LpScripts* 所指出的腳本緩衝區大小（以字元為單位）。

或者，應用程式可以將此參數設定為0。 在此情況下，此函式會在 *lpScripts* 中抓取 **Null** ，並傳回腳本緩衝區所需的大小。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功且 *cchScripts* 設為非零值，則傳回在輸出緩衝區中取出的字元數，包括結束的 null 字元。 此函式會傳回1，表示找不到任何腳本，例如，當輸入字串只包含通用或繼承字元，而且 \_ \_ 未設定 GSS 允許繼承 \_ 的一般時。 假設每個找到的腳本會將五個字元加 (四個字元 + 分隔符號) ，簡單的數學運算會提供 (傳回 \_ 碼 1) /5 的腳本計數。

如果函式成功，且 *cchScripts* 的值為0，則傳回值為腳本緩衝區所需的大小（以字元為單位，包括結束的 null 字元）。 腳本計數如上所述。

如果不成功，函數會傳回0。 若要取得擴充的錯誤資訊，應用程式可以呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)，這可能會傳回下列其中一個錯誤碼：

-   錯誤 \_ BADDB。 函數無法存取資料。 通常不會發生這種情況，通常表示安裝不良、磁片問題或類似。
-   \_緩衝區不足 \_ 的錯誤。 提供的緩衝區大小不夠大，或未正確設定為 **Null**。
-   錯誤 \_ 無效 \_ 的旗標。 為旗標提供的值無效。
-   錯誤 \_ 無效 \_ 的參數。 任何參數值都無效。

## <a name="remarks"></a>備註

這項功能可作為策略的一部分，以降低與國際化功能變數名稱相關的安全性問題 [ (IDNs) ](handling-internationalized-domain-names--idns.md)。

腳本判斷是以中 Unicode 協會所發行的腳本值為基礎 <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> ，不同之處在于未指派的字元具有值 "Zzzz" (未指派) ，而不是 "Zyyy" (一般) 。

以下是此函式行為的一些範例：



輸入字串

*dwFlags*

*lpScripts*

指令碼

Microsoft.com

0

Latn;

拉丁文

Microsoft.com

GSS \_ 允許 \_ 繼承 \_ 通用

Latn;Zyyy;

拉丁 + 通用

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 0241 006F

$ {ROWSPAN2} $GSS \_ 允許 \_ 繼承的 \_ 通用 $ {REMOVE} $  

$ {ROWSPAN2} $Latn; $ {REMOVE} $  

$ {ROWSPAN2} $Latin $ {REMOVE} $  

使用具有波狀符號的拉丁小寫字母 N

$ {ROWSPAN2} $Ni ño $ {REMOVE} $  

004E 0069 006E 0303 006F

$ {ROWSPAN2} $GSS \_ 允許 \_ 繼承的 \_ 通用 $ {REMOVE} $  

$ {ROWSPAN2} $Latn;Qaii; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + 繼承 $ {REMOVE} $  

使用組合波狀符號

$ {ROWSPAN2} $Sp ооf $ {REMOVE} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $ 0 $ {REMOVE} $  

$ {ROWSPAN2} $Latn;Cyrl; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + 斯拉夫 $ {REMOVE} $  

使用斯拉夫小寫字母 O



U + f000

0

Zzzz

未指定



U + f000

GSS \_ 允許 \_ 繼承 \_ 通用

Zzzz

未指定



 

必要的標頭檔和 DLL 是「 [Microsoft 國際化功能變數名稱 (IDN) 緩和 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) 」下載的一部分，可從 [MSDN 下載中心](https://www.microsoft.com/?ref=go)取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                                                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                                                                        |
| 可轉散發套件<br/>          | Microsoft 國際化功能變數名稱 (IDN) Windows XP (SP2 或更新版本) 、Windows Server 2003 (SP1 或更新版本) 或 Windows Vista 的風險降低 api<br/> |
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

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 

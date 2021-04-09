---
title: 'EM_AUTOURLDETECT 訊息 (Richedit .h) '
description: 啟用或停用 rich edit 控制項的超連結自動偵測。
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934638"
---
# <a name="em_autourldetect-message"></a>EM \_ AUTOURLDETECT 訊息

啟用或停用 rich edit 控制項的超連結自動偵測。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定0會停用自動連結偵測，或指定下列其中一個值來啟用各種類型的偵測。



| 值                                                                                                                                                                                       | 意義                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**：停用包含屬於下列其中一個以上腳本的標籤之功能變數名稱的識別：拉丁、希臘文和斯拉夫文。 <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**：辨識具有前置磁片磁碟機規格的檔案名，例如 c： \\ temp。<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | 此值已被取代;請改用 **AURL \_ ENABLEEAURLS** 。<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | 辨識包含東亞字元的 Url。 <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8**：辨識電子郵件地址。<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8**：辨識電話號碼。<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**：辨識包含路徑的 url。<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

此參數會決定 **AURL \_ ENABLEURL** 是否為使用中時，可辨識的 URL 架構。 如果 *lParam* 為 Null，則會使用預設的配置名稱清單 (請參閱備註) 。 或者， *lParam* 可指向以 null 終止的字串，其中包含最多50個以冒號結束的架構名稱，以取代預設的配置名稱清單。 例如，字串可以是 "news： HTTP： ftp： telnet："。 配置名稱語法定義于 [統一資源識別項 (URI) ：]( https://www.ietf.org/rfc/rfc2396.txt) 網際網路工程任務推動 (小組) 網站上的一般語法檔。 具體來說，配置名稱最多可以包含13個字元 (包括冒號) 、必須以 ASCII 字母開頭，且後面可以加上 ASCII Alphabetics、數位和三個標點符號字元： "."、"+" 和 "-"。 字串類型可以是 **char \** _ 或 _*WCHAR \**_; rich edit 控制項會自動偵測型別。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則傳回值為零。

如果訊息失敗，則傳回值為非零值。 例如，訊息可能會因為記憶體不足、不正確偵測選項或不正確配置名稱字串而失敗。

如果 _lParam * 包含50個以上的配置名稱，訊息會失敗，並傳回值為 **E \_ INVALIDARG**。

## <a name="remarks"></a>備註

如果啟用了自動 URL 偵測 (也就是， *wParam* 包括 **AURL \_ ENABLEURL**) ，rich edit 控制項會掃描任何修改過的文字，以判斷文字是否符合 URL 的格式 (或更常用於 WINDOWS 8 或更新版本的 IRI 國際資源識別碼) 。 如果 *lParam* 為 Null，則控制項會偵測開頭為下列配置名稱的 url：

-   callto
-   file
-   ftp
-   gopher
-   http
-   https
-   mailto
-   新聞
-   版本
-   nntp
-   onenote
-   Outlook
-   普洛斯彼羅
-   tel
-   telnet
-   wais
-   webcal

啟用自動連結偵測時，rich edit 控制項會從沒有控制項可辨識之格式的修改文字中移除 **CFE \_ 連結** 效果。 如果您的應用程式使用 **CFE \_ 連結** 效果來標示其他類型的文字，請不要啟用自動連結偵測。 Rich edit 控制項不會檢查偵測到的連結是否存在;該責任屬於用戶端。

當滑鼠指標停留在具有 **CFE \_ 連結** 效果的文字上方時，rich Edit 控制項會傳送 [en-us \_ 連結](en-link.md)通知。 如需詳細資訊，請參閱 [自動 RichEdit 超連結](/archive/blogs/murrays/automatic-richedit-hyperlinks) 和 [RichEdit 易記名稱超連結](/archive/blogs/murrays/richedit-friendly-name-hyperlinks)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[EN \_ 連結](en-link.md)
</dt> </dl>

 


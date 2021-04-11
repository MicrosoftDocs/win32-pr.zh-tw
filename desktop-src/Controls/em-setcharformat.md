---
title: 'EM_SETCHARFORMAT 訊息 (Richedit .h) '
description: 設定 rich edit 控制項中的字元格式。
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105587"
---
# <a name="em_setcharformat-message"></a>EM \_ SETCHARFORMAT 訊息

設定 rich edit 控制項中的字元格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

套用至控制項的字元格式。 如果此參數為零，則會設定預設的字元格式。 否則，它可以是下列其中一個值。



| 值                                                                                                                                                                           | 意義                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ 全部**</dt> </dl>                                     | 將格式套用至控制項中的所有文字。 **SCF \_ 選取範圍** 或 **SCF \_ 字** 組無效。<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4.1：** 將字型與指定的腳本產生關聯，從而變更該腳本的預設字型。 若要指定字型，請使用下列 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)成員： **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid**。<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4.1：** 將代理 (平面-2) 字型與指定的腳本產生關聯，進而變更該腳本的預設字型。 若要指定字型，請使用下列 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)成員： **yHeight**、 **bCharSet**、 **bPitchAndFamily**、 **szFaceName** 和 **lcid**。<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | 取得從 LCID 所有產品的字元。<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ 預設值**</dt> </dl>                         | **RichEdit 4.1：** 設定控制項的預設字型。 <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**SPF \_ DONTSETDEFAULT**</dt> </dl>    | 當 rich edit 控制項為空白時，防止設定預設段落格式。<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4.1：** 防止鍵盤切換以符合字型。 例如，如果設定了阿拉伯文字型，則雙向語言的自動鍵盤功能通常會將鍵盤變更為阿拉伯文鍵盤。<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SCF \_ 選取專案**</dt> </dl>                   | 將格式套用至目前的選取範圍。 如果選取專案是空的，則會將字元格式套用至插入點，而新的字元格式只會在插入點變更時生效。<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF \_ SETDEFAULT**</dt> </dl>                | 設定預設段落格式化屬性。<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | 只有在可以處理腳本時，才套用字型。<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4.1：** 搭配 **SCF \_ 選項** 使用。 表示格式來自工具列或其他 UI 工具，因此應該使用 UI 格式化規則，而不是常值格式。<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**SCF \_ WORD**</dt> </dl>                                  | 將格式套用至選取的單字或文字。 如果選取範圍是空的，但插入點位於單字內，則會將格式套用至文字。 **SCF \_ 文字** 值必須與 **SCF \_ 選取** 值一起使用。<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構的指標，指定要使用的字元格式。 只有 **dwMask** 成員所指定的格式屬性會變更。

Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) 結構的指標，也就是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構的延伸。 傳送 **EM \_ SETCHARFORMAT** 訊息之前，請將結構的 **cbSize** 成員設定為， `sizeof(CHARFORMAT)` 或指出所使用的 `sizeof(CHARFORMAT2)` 結構版本。

當字元無效時， **szFaceName** 和 **bCharSet** 成員可能會被視為無效，例如：在中文字元上為 Arial。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零值。

如果作業失敗，則傳回值為零。

## <a name="remarks"></a>備註

如果使用相同的參數多次傳送此訊息，則會切換文字的效果。 也就是說，傳送訊息一次會產生效果，傳送訊息兩次會取消效果等等。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 






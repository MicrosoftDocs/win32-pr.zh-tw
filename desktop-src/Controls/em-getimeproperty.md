---
title: 'EM_GETIMEPROPERTY 訊息 (Richedit .h) '
description: 抓取輸入方法編輯器的屬性和功能 (IME) 與目前的輸入地區設定相關聯。
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541108"
---
# <a name="em_getimeproperty-message"></a>EM \_ GETIMEPROPERTY 訊息

抓取輸入方法編輯器的屬性和功能 (IME) 與目前的輸入地區設定相關聯。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要取得之屬性資訊的類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                     | 意義                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**IGP \_ 屬性**</dt> </dl>                | 屬性資訊。<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**IGP \_ 轉換**</dt> </dl>          | 轉換功能。 <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**IGP \_ 句子**</dt> </dl>                | 句子模式功能。 <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**IGP \_ UI**</dt> </dl>                                  | 使用者介面功能。 <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | 撰寫字串功能。 <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP \_ SELECT**</dt> </dl>                      | 選取範圍繼承功能。 <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | 抓取已建立指定 IME 的系統版本號碼。 <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

根據 *lParam* 參數的值，傳回屬性或功能值。 如需詳細資訊，請參閱＜備註＞一節。

## <a name="remarks"></a>備註

如果 *wParam* 是 IGP \_ 屬性，它會傳回下列一或多個值。



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_插入號 \_ 的輸入法 \_                | 如果設定，則轉換視窗位於插入號位置。 若為清除，則視窗接近插入號位置。                                                                                                                                                                  |
| IME \_ 特性 \_ 特殊 \_ UI              | 如果設定，IME 會有非標準的使用者介面。 應用程式不應該在 IME 視窗中繪製。                                                                                                                                                                  |
| IME \_ \_ 的 CANDLIST \_ \_ 從 \_ 1 開始 | 如果設定，候選清單中的字串會從1開始編號。 如果清除，字串就會從零開始。                                                                                                                                                                |
| IME \_ 的 \_ UNICODE                  | 如果設定，則會將 IME 視為 UnicodeIME。 系統和 IME 會透過 UnicodeIME 介面進行通訊。 如果清除，IME 將使用 ANSI 介面與系統通訊。                                                                    |
| \_ \_ \_ 取消選取時完成的 IME \_   | 如果設定，則轉換視窗位於插入號位置。 若為清除，則視窗接近插入號位置。                                                                                                                                                                  |
| IME 的 \_ 主張 \_ 接受 \_ 寬 \_ VKEY       | 如果設定，IME 會使用 VK 封包來處理來自 [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) 函式的插入 Unicode \_ 。 如果清除，IME 可能不會處理插入的 Unicode，而插入的 Unicode 可能會直接傳送至應用程式。 |



 

如果 *wParam* 是 IGP \_ UI，它會傳回下列一或多個值。



| 需求 | 值 |
|-----------------|-------------------------------------------------------------------------------------------------------|
| UI \_ 上限 \_ 2700   | 支援0或2700的文字行距值。 如需詳細資訊，請參閱 **lfEscapement**。             |
| UI \_ 端點 \_ ROT90  | 支援文字行距值0、900、1800或2700。 如需詳細資訊，請參閱 **lfEscapement**。 |
| UI \_ 端點 \_ ROTANY | 支援任何文字行距值。 如需詳細資訊，請參閱 **lfEscapement**。                       |



 

如果 *wParam* 是 IGP \_ SETCOMPSTR，它會傳回下列一或多個值。



| 需求 | 值 |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS \_ 端點 \_ COMPSTR            | 可以透過呼叫 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 函式與 SCS SETSTR 值來建立組合字元串 \_ 。                                                      |
| SCS \_ 端點 \_ MAKEREAD           | 搭配 SCS SETSTR 使用 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 函式時，可以從對應的組合字元串建立讀取字串 \_ ，而不設定 *lpRead*。 |
| SCS \_ 端點 \_ SETRECONVERTSTRING | 此 IME 可以支援漢字重組。 使用 [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) 來執行 [重設]。                                                                             |



 

如果 *wParam* 為 IGP \_ SELECT，則會傳回下列一或多個值。



| 需求 | 值 |
|-----------------------|------------------------------------------------------|
| 選取 \_ 端點 \_ CONVMODE | 選取新的輸入法時繼承轉換模式。 |
| 選取 \_ 端點 \_ 句子 | 選取新的 IME 時繼承句子模式。   |



 

如果 *wParam* 是 IGP \_ GETIMEVERSION，它會傳回下列一或多個值。



| 需求 | 值 |
|--------------|---------------------------------------------|
| IMEVER \_ 0310 | 已針對 Windows 3.1 建立 IME。        |
| IMEVER \_ 0400 | 已針對 Windows 95 或更新版本建立 IME |



 

這則訊息與 [**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)類似，不同之處在于它會使用目前的輸入地區設定。 在呼叫此函式之前，應用程式應該呼叫 [**EM \_ ISIME**](em-isime.md) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

**其他資源**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 


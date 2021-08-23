---
title: 'EM_GETLANGOPTIONS 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的 [輸入方法編輯器] 選項設定， (IME) 和亞洲語言支援。
ms.assetid: 9fd9d27c-7713-454e-b49f-8ecdba848d2e
keywords:
- EM_GETLANGOPTIONS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6e3fa3602259ff0b754c79c69d91048c68c60b2703d4cd06a7da4630fcdf646
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119800198"
---
# <a name="em_getlangoptions-message"></a>EM \_ GETLANGOPTIONS 訊息

取得 rich edit 控制項的 [輸入方法編輯器] 選項設定， (IME) 和亞洲語言支援。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回輸入法和亞洲語言設定，這可以是零或多個下列值。



| 傳回碼                                                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**IMF \_ AUTOFONT**</dt> </dl>                    | 如果設定此旗標，當使用者明確變更為不同的鍵盤配置時，控制項會自動變更字型。 針對通用 Unicode 字型關閉 **IMF \_ AUTOFONT** 相當有用。 預設會開啟此選項 (1) 。<br/>                                                                                                                                                                     |
| <dl> <dt>**IMF \_ AUTOFONTSIZEADJUST**</dt> </dl>          | 如果設定此旗標，控制項會根據腳本，從插入點大小調整字型系結的字型大小。 例如，亞洲字型比西方字體稍微大一點。 預設會開啟此選項 (1) 。<br/>                                                                                                                                                                                              |
| <dl> <dt>**IMF \_ AUTOKEYBOARD**</dt> </dl>                | 如果設定此旗標，當使用者明確變更為不同的字型，或當使用者將插入點明確變更為文字中的新位置時，控制項會自動變更鍵盤配置。 會自動開啟雙向控制項。 針對其他所有控制項，預設會關閉它。 依預設，此選項會關閉 (0) 。<br/>                                 |
| <dl> <dt>**IMF \_ DISABLEAUTOBIDIAUTOKEYBOARD**</dt> </dl> | **Windows 8**：如果設定此旗標，控制項會使用語言中性邏輯來自動切換鍵盤。 依預設，此選項會關閉 (0) 。<br/>                                                                                                                                                                                                                                                            |
| <dl> <dt>**IMF \_ DUALFONT**</dt> </dl>                    | 如果設定此旗標，控制項會使用雙重字型模式。 用於亞洲語言支援。 此控制項使用英文的 ASCII 文字字型，以及亞洲文字的亞洲字型。 預設會開啟此選項 (1) 。<br/>                                                                                                                                                                                                   |
| <dl> <dt>**IMF \_ IMEALWAYSSENDNOTIFY**</dt> </dl>         | 此旗標會控制 rich edit 控制項在 IME 撰寫期間如何通知用戶端： <br/> 0：沒有任何 [en \_ 變更](en-change.md) 或在未確定狀態期間的 [en \_ SELCHANGE](en-selchange.md) 通知。 當最後一個字串進入時傳送通知。 此為預設值。<br/> 1：在未定狀態期間傳送 [en \_ 變更](en-change.md) 和 [en \_ SELCHANGE](en-selchange.md) 事件。<br/> |
| <dl> <dt>**IMF \_ IMECANCELCOMPLETE**</dt> </dl>           | 此旗標會決定當使用者取消 IME 時，控制項如何使用 IME 的組合字元串。 如果這項旗標已設定，控制項就會捨棄組字字串。 如果這項旗標尚未設定，控制項就會使用組字字串做為結果字串。 依預設，此選項會關閉 (0) 。<br/>                                                                                                              |
| <dl> <dt>**IMF \_ NOIMPLICITLANG**</dt> </dl>              | **Windows 8**：如果設定此旗標，請使用鍵盤語言停用戳記鍵盤輸入，並確保非東亞語言 ids 與字元所有產品相容。 依預設，此選項會關閉 (0) 。 <br/>                                                                                                                                                                             |
| <dl> <dt>**IMF \_ NOKBDLIDFIXUP**</dt> </dl>               | **Windows 8**：如果設定此旗標，rich edit 控制項會在空白控制項上停用戳記鍵盤語言。 依預設，此選項會關閉 (0) 。<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**IMF \_ 拼寫**</dt> </dl>               | **Windows 8**：如果設定此旗標，rich edit 控制項會開啟拼寫檢查。 依預設，此選項會關閉 (0) 。 <br/>                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**IMF \_ TKBAUTOCORRECTION**</dt> </dl>           | **Windows 8**：如果設定此旗標，請啟用觸控鍵盤自動校正。 依預設，此選項會關閉 (0) 。 <br/>                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**IMF \_ TKBPREDICTION**</dt> </dl>               | **Windows 10**：已忽略。<br/> **Windows 8**：如果設定此旗標，rich edit 控制項會啟用觸控鍵盤預測。 依預設，此選項會關閉 (0) 。 <br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**IMF \_ UIFONTS**</dt> </dl>                     | 使用使用者介面預設字型。 依預設，此選項會關閉 (0) 。<br/>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>備註

預設會設定 **IMF \_ AUTOFONT** 旗標。 預設會清除 **imf \_ AUTOKEYBOARD** 和 **imf \_ IMECANCELCOMPLETE** 旗標。

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

[**EM \_ SETLANGOPTIONS**](em-setlangoptions.md)
</dt> <dt>

[**EM \_ SETLIMITTEXT**](em-setlimittext.md)
</dt> </dl>

 

 






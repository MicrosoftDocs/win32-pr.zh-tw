---
title: 'EM_STREAMIN 訊息 (Richedit .h) '
description: 以定義為 \ 8211 的應用程式所提供的資料流程，取代 rich edit 控制項的內容。EditStreamCallback 回呼函數。
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 597d6483ef02f0c9f6f4e4459cd6780b91e04c39160c8057e88fc537fde3b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576338"
---
# <a name="em_streamin-message"></a>EM \_ STREAMIN 訊息

以應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 回呼函式所提供的資料流程，取代 rich edit 控制項的內容。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定資料格式和取代選項。 此值必須是下列其中一個值。



| 值                                                                                                                                       | 意義         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ 文字**</dt> </dl> | Text<br/> |



 

此外，您可以指定下列旗標。



| 值                                                                                                                                                         | 意義                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>    | 如果指定，則只會在中串流處理所有語言通用的關鍵字。 資料流程中的語言特定 RTF 關鍵字會被忽略。 如果未指定，則會在中串流處理所有關鍵詞。 您可以結合此旗標與 **SF \_ RTF** 旗標。<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SFF \_ 選取專案**</dt> </dl> | 如果有指定，資料流程會取代目前選取範圍的內容。 如果未指定，資料流程會取代控制項的整個內容。 您可以結合此旗標與 **sf \_ TEXT** 或 **sf \_ rtf** 旗標。<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>          | **Microsoft Rich Edit 2.0 和更新版本：** 指出 Unicode 文字。 您可以結合此旗標與 **SF \_ 文字** 旗標。 <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的指標。 在輸入時，此結構的 **pfnCallback** 成員必須指向應用程式定義的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) 函數。 在輸出中，如果發生錯誤， **dwError** 成員可以包含非零的錯誤碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回讀取的字元數。

## <a name="remarks"></a>備註

當您傳送 **EM \_ STREAMIN** 訊息時，rich Edit 控制項會對 [**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)結構的 **pfnCallback** 成員所指定的 [*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)函數進行重複呼叫。 每次呼叫回呼函式時，就會將資料填入緩衝區，以讀取控制項。 這會繼續進行，直到回呼函式指出資料流程進行中的作業已完成或發生錯誤。

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMOUT**](em-streamout.md)
</dt> </dl>

 

 






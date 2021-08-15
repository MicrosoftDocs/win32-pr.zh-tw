---
title: '轉換模式的旗標 (Ctffunc .h) '
description: 下列旗標可作為 GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE 轉換的值 \_ 。 這相當於 IMM32 的輸入法 \_ CMODE 值。
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- 轉換模式文字服務架構的旗標
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c8c3a452e3115e66e4f0f6e75999cad9bce7e1eadf14b4cadd24fae640a327
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118879214"
---
# <a name="flags-for-conversion-mode"></a>轉換模式的旗標

下列旗標可作為 [GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE \_ 轉換](predefined-compartments.md)的值。 這相當於 IMM32 的 [輸入法 \_ CMODE](../intl/ime-conversion-mode-values.md) 值。



| 旗標                             | 值  | 描述                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| TF \_ CONVERSIONMODE 英 \_ 數位元 | 0x0000 | 如果是英數位元模式，則設為1。                                  |
| TF \_ CONVERSIONMODE \_ NATIVE       | 0x0001 | 如果原生模式，則設定為 1;若為英數位元模式，則為0。                |
| TF \_ CONVERSIONMODE \_ 片假名     | 0x0002 | 若為片假名模式，則設定為 1;若為平假名模式，則為0。                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | 如果全圖形模式，則設定為 1;如果為半形狀模式，則為0。              |
| TF \_ CONVERSIONMODE \_ 羅馬        | 0x0010 | 設定為1以防止依 IME 處理轉換;如果沒有，則為0。 |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | 如果字元碼輸入模式，則設定為 1;如果沒有，則為0。                |
| TF \_ CONVERSIONMODE \_ SOFTKEYBOARD | 0x0080 | 如果軟鍵盤模式，則設定為 1;如果沒有，則為0。                       |
| TF \_ CONVERSIONMODE \_ NOCONVERSION | 0x0100 | 設定為1以防止依 IME 處理轉換;如果沒有，則為0。 |
| TF \_ CONVERSIONMODE \_ 符號       | 0x0400 | 如果符號轉換模式，則設定為 1;如果沒有，則為0。                   |
| TF \_ CONVERSIONMODE 已 \_ 修正        | 0x0800 | 如果固定的轉換模式，則設定為 1;如果沒有，則為0。                    |



 

下列值會當做 [GUID 區間 \_ \_ 鍵盤 \_ INPUTMODE \_ 句子](predefined-compartments.md)的值使用。 這相當於 IMM32 的 [輸入法 \_ SMODE](../intl/ime-composition-string-values.md) 值。



| 旗標                            | 值  | 描述                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ NONE          | 0x0000 | 沒有句子的資訊。                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | IME 使用複數子句資訊來執行轉換處理。 |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | IME 會以單一字元模式執行轉換處理。        |
| TF \_ SENTENCEMODE \_ 自動     | 0x0004 | IME 會在自動模式中執行轉換處理。               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | IME 會使用片語資訊來預測下一個字元。             |
| TF \_ SENTENCEMODE \_ 對話  | 0x0010 | IME 使用交談模式。 這對聊天應用程式很有用。      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 可轉散發套件<br/>          | TSF 1.0 于 windows NT 4.0、Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| 標頭<br/>                   | <dl> <dt>Ctffunc。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Ctffunc .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[預先定義的區間](predefined-compartments.md)
</dt> </dl>

 


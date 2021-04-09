---
title: 'EM_FINDTEXT 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找文字。
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934552"
---
# <a name="em_findtext-message"></a>EM \_ FINDTEXT 訊息

在 rich edit 控制項中尋找文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定搜尋作業的參數。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR-FR \_**</dt> </dl>                               | Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從目前選取範圍的結尾到檔的結尾。 如果未設定，則會從目前選取範圍的結尾到檔的開頭進行搜尋。 <br/> Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。 搜尋一律會從目前選取範圍的結尾到檔的結尾。<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋會區分阿拉伯文 alefs 與不同的重音。 如果未設定，則會將所有 alefs 單獨與 alef 字元相符。 <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文的變音符號。 如果未設定，則會忽略變音符號標記。 <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文 kashidas。 如果未設定，則會忽略 kashidas。 <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8：如果設定，則相同字元的單一位元組和雙位元組版本會視為不相等。<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | 如果設定，作業只會搜尋符合搜尋字串的整個單字。 如果未設定，此作業也會搜尋符合搜尋字串的文字片段。<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)結構，其中包含尋找作業的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。 如果找不到目標，則傳回值為-1。

## <a name="remarks"></a>備註

**FINDTEXT** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。 向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。 向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 






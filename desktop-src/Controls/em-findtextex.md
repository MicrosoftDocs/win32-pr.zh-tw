---
title: 'EM_FINDTEXTEX 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找文字。
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104225"
---
# <a name="em_findtextex-message"></a>EM \_ FINDTEXTEX 訊息

在 rich edit 控制項中尋找文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定搜尋操作的行為。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR-FR \_**</dt> </dl>                               | Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從 **FINDTEXTEX. chrg. cpMin**;如果未設定，則搜尋會從 **FINDTEXTEX. chrg. cpMin**。 <br/> Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。 搜尋一律會向前復原。<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋會區分阿拉伯文和希伯來文 alefs 與不同的強調。 如果未設定，則會將所有 alefs 單獨與 alef 字元相符。 <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | 如果設定，搜尋作業會區分大小寫。 如果未設定，則搜尋作業不區分大小寫。 <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文的變音符號。 如果未設定，則會忽略變音符號標記。 <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 和更新版本：如果設定，搜尋作業會考慮阿拉伯文和希伯來文 kashidas。 如果未設定，則會忽略 kashidas。 <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | 如果設定，作業只會搜尋符合搜尋字串的整個單字。 如果未設定，此作業也會搜尋符合搜尋字串的文字片段。<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構，其中包含尋找作業的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。 如果找不到目標，則傳回值為-1。

## <a name="remarks"></a>備註

使用此訊息來尋找 ANSI 字串。 若為 Unicode，請使用 [**EM \_ FINDTEXTEXW**](em-findtextexw.md)。

**FINDTEXTEX** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。 向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。 向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。

如果搜尋作業找到相符的， [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構的 **chrgText** 成員會傳回包含相符文字的字元位置範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ FINDTEXT**](em-findtext.md)
</dt> </dl>

 

 






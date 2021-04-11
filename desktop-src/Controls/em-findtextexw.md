---
title: 'EM_FINDTEXTEXW 訊息 (Richedit .h) '
description: 在 rich edit 控制項中尋找 Unicode 文字。
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934914"
---
# <a name="em_findtextexw-message"></a>EM \_ FINDTEXTEXW 訊息

在 rich edit 控制項中尋找 Unicode 文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定搜尋操作的行為。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR-FR \_**</dt> </dl>                               | Microsoft Rich Edit 2.0 和更新版本：如果設定，搜尋會從 **FINDTEXTEX. chrg. cpMin**;如果未設定，則搜尋會從 **FINDTEXTEX. chrg. cpMin**。 <br/> Microsoft Rich Edit 1.0： \_ 已忽略 FR 旗標。 搜尋一律會向前復原。<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | 如果設定，搜尋會區分具有不同重音的 alefs。 如果未設定，則具有不同重音的阿拉伯文和希伯來文 alefs 都會以 alef 字元進行比對。 <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | 如果設定，搜尋作業會區分大小寫。 如果未設定，則搜尋作業不區分大小寫。<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | 如果設定，搜尋作業會考慮變音符號。 如果未設定，則會忽略阿拉伯文和希伯來文的變音符號。 <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | 如果設定，搜尋作業會考慮 kashidas。 如果未設定，則會忽略阿拉伯文和希伯來文 kashidas。 <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | 如果設定，作業只會搜尋符合搜尋字串的整個單字。 如果未設定，此作業也會搜尋符合搜尋字串的文字片段。<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構，其中包含尋找作業的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。 如果找不到目標，則傳回值為-1。

## <a name="remarks"></a>備註

使用此訊息來尋找 Unicode 字串。 若是 ANSI，請使用 [**EM \_ FINDTEXTEX**](em-findtextex.md)。

**FINDTEXTEX** 的 **cpMin** 成員一律會指定搜尋的起始點，而 **cpMax** 則會指定結束點。 向前搜尋時， **cpMin** 必須等於或大於 **cpMax**。 向前搜尋時， **cpMax** 中的-1 值會將搜尋範圍延伸至文字的結尾。

如果搜尋作業找到相符的， [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa)結構的 **chrgText** 成員會傳回包含相符文字的字元位置範圍。

**EM \_FINDTEXTEXW** 會使用 [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構，而 [**EM \_ FINDTEXTW**](em-findtextw.md) 會使用 [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構。 差別在於 **EM \_ FINDTEXTEXW** 會報告找到的文字範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ FINDTEXTW**](em-findtextw.md)
</dt> </dl>

 

 






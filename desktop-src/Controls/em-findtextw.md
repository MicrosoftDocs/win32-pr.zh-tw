---
title: 'EM_FINDTEXTW 訊息 (Richedit .h) '
description: EM_FINDTEXTW 訊息-在 rich edit 控制項中尋找 Unicode 文字。
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW message Windows 控制項
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109796"
---
# <a name="em_findtextw-message"></a>EM \_ FINDTEXTW 訊息

在 rich edit 控制項中尋找 Unicode 文字。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定搜尋作業的參數。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                     | 意義                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR-FR \_**</dt> </dl>                               | 如果設定，則作業會從目前選取範圍的結尾開始搜尋檔的結尾。 如果未設定，則作業會從目前選取範圍的結尾開始搜尋檔的開頭。<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | 依預設，具有不同重音的阿拉伯文和希伯來文 alefs 都會以 alef 字元進行比對。 如果您想要讓搜尋區分 alefs 與不同的重音，請設定此旗標。<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | 如果設定，搜尋作業會區分大小寫。 如果未設定，則搜尋作業不區分大小寫。<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDIAC**</dt> </dl>                | 根據預設，會忽略阿拉伯文和希伯來文的變音符號。 如果您想要讓搜尋作業考慮變音符號，請設定此旗標。<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | 依預設，會忽略阿拉伯文和希伯來文 kashidas。 如果您想要搜尋作業考慮 kashidas，請設定此旗標。<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | 如果設定，作業只會搜尋符合搜尋字串的整個單字。 如果未設定，此作業也會搜尋符合搜尋字串的文字片段。<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta)結構，其中包含尋找作業的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到目標字串，則傳回值是比對之第一個字元的以零為基底的位置。 如果找不到目標，則傳回值為-1。

## <a name="remarks"></a>備註

**EM \_FINDTEXTW** 會使用 [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) 結構，而 [**EM \_ FINDTEXTEXW**](em-findtextexw.md) 會使用 [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) 結構。 差別在於 **FINDTEXTEXW** 會回報所找到的文字範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 






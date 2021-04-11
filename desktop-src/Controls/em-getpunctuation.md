---
title: 'EM_GETPUNCTUATION 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前標點符號字元。
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105299"
---
# <a name="em_getpunctuation-message"></a>EM \_ GETPUNCTUATION 訊息

取得 rich edit 控制項的目前標點符號字元。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本的 Rich Edit 都不支援此功能。

 

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

標點符號類型可以是下列其中一個值。



| 值                                                                                                                                                      | 意義                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**電腦 \_ 領先**</dt> </dl>       | 前置標點符號字元<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**電腦 \_ 遵循**</dt> </dl> | 下列標點符號字元<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**電腦 \_ 分隔符號**</dt> </dl> | 分隔符號<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**電腦 \_ 溢位**</dt> </dl>    | 不支援<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

接收標點符號字元之 [**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零值。

如果作業失敗，則傳回值為零。

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

[**EM \_ SETPUNCTUATION**](em-setpunctuation.md)
</dt> <dt>

[**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 






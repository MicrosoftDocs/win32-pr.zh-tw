---
title: 'EM_SETPUNCTUATION 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的標點符號字元。
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062898"
---
# <a name="em_setpunctuation-message"></a>EM \_ SETPUNCTUATION 訊息

設定 rich edit 控制項的標點符號字元。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本都不支援此功能。

 

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定標點符號類型，它可以是下列值之一。



| 值                                                                                                                                                      | 意義                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**電腦 \_ 領先**</dt> </dl>       | 前置標點符號字元。<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**電腦 \_ 遵循**</dt> </dl> | 下列標點符號字元。<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**電腦 \_ 分隔符號**</dt> </dl> | 分隔符號。<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**電腦 \_溢** 位</dt> </dl> | 不支援。<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

包含標點符號字元之 [**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業成功，則傳回值為非零值。

如果作業失敗，則傳回值為零。

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

[**EM \_ GETPUNCTUATION**](em-getpunctuation.md)
</dt> <dt>

[**標點符號**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 






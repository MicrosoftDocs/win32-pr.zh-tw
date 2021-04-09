---
title: 'EM_GETPARAFORMAT 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項中目前選取範圍的段落格式。
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49060861a955e85d153fc9041c9b364db109f83a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934913"
---
# <a name="em_getparaformat-message"></a>EM \_ GETPARAFORMAT 訊息

抓取 rich edit 控制項中目前選取範圍的段落格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構的指標，此結構會接收目前選取範圍的段落格式化屬性。

如果選取了一個以上的段落，結構會接收第一個段落的屬性，而 **dwMask** 成員會指定整個選取範圍中的屬性是一致的。

Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) 結構的指標，也就是 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) 結構的延伸。 傳送 **EM \_ GETPARAFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回 [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)結構之 **dwMask** 成員的值。

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 






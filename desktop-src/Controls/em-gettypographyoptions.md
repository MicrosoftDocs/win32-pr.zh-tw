---
title: 'EM_GETTYPOGRAPHYOPTIONS 訊息 (Richedit .h) '
description: 傳回 rich edit 控制項之印刷樣式選項的目前狀態。
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- EM_GETTYPOGRAPHYOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105107"
---
# <a name="em_gettypographyoptions-message"></a>EM \_ GETTYPOGRAPHYOPTIONS 訊息

傳回 rich edit 控制項之印刷樣式選項的目前狀態。

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

傳回目前的印刷樣式選項。 如需選項的清單，請參閱 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)。

## <a name="remarks"></a>備註

您可以藉由傳送 [**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) 訊息來開啟 advanced line。 Rich edit 控制項（如果特定語言需要的話）也會自動開啟 Advanced 和 normal 分行符號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**EM \_ SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md)
</dt> <dt>

**概念**
</dt> <dt>

[關於 Rich Edit 控制項](about-rich-edit-controls.md)
</dt> </dl>

 

 






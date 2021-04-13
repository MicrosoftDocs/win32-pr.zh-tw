---
title: 'EM_EXGETSEL 訊息 (Richedit .h) '
description: 在 rich edit 控制項中，抓取選取範圍的開始和結束字元位置。
ms.assetid: 60fcf13e-6c45-4f4e-9b54-70f0985122fb
keywords:
- EM_EXGETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXGETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b97fb43a76f0f8ac91dd16c0cfa5700c5431eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465893"
---
# <a name="em_exgetsel-message"></a>EM \_ EXGETSEL 訊息

在 rich edit 控制項中，抓取選取範圍的開始和結束字元位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接收選取範圍的 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange)
</dt> </dl>

 

 






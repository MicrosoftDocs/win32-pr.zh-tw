---
title: 'EM_GETCTFOPENSTATUS 訊息 (Richedit .h) '
description: 決定文字服務架構 (TSF) 鍵盤是開啟或關閉。
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- EM_GETCTFOPENSTATUS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934489"
---
# <a name="em_getctfopenstatus-message"></a>EM \_ GETCTFOPENSTATUS 訊息

決定文字服務架構 (TSF) 鍵盤是開啟或關閉。

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

如果 TSF 鍵盤已開啟，則傳回值為 **TRUE**。 否則為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP1） \[ 桌面應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ SETCTFOPENSTATUS**](em-setctfopenstatus.md)
</dt> </dl>

 

 






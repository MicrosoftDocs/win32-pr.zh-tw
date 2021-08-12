---
title: 'TVM_SETLINECOLOR 訊息 (Commctrl .h) '
description: TVM \_ SETLINECOLOR 訊息會設定目前的線條色彩。
ms.assetid: c5fc28af-5603-489f-aa6b-73e153f9aebc
keywords:
- TVM_SETLINECOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_SETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af66e7a711611ff5e59ec0d68b58a24fb39399245437b0e5d81840c1c38b2d0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669518"
---
# <a name="tvm_setlinecolor-message"></a>TVM \_ SETLINECOLOR 訊息

**TVM \_ SETLINECOLOR** 訊息會設定目前的線條色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

新的線條色彩。 使用 CLR \_ 預設值來還原系統預設色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的線條色彩。

## <a name="remarks"></a>備註

此訊息只會變更線條色彩。 若要變更按鈕內的 ' + ' 和 '-' 色彩，請使用 [**TVM \_ SETTEXTCOLOR**](tvm-settextcolor.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ GETLINECOLOR**](tvm-getlinecolor.md)
</dt> </dl>

 

 






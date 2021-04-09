---
title: 'TVM_GETLINECOLOR 訊息 (Commctrl .h) '
description: TVM \_ GETLINECOLOR 訊息會取得目前的線條色彩。
ms.assetid: e74441b3-5d4f-4454-b896-2e96ce649419
keywords:
- TVM_GETLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- TVM_GETLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd55149f38fb17238e13135e798ebbe55b15009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025245"
---
# <a name="tvm_getlinecolor-message"></a>TVM \_ GETLINECOLOR 訊息

**TVM \_ GETLINECOLOR** 訊息會取得目前的線條色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回目前的線條色彩，如果未指定，則為 CLR \_ 預設值。

## <a name="remarks"></a>備註

此訊息只會抓取線條色彩。 若要取出按鈕內的 ' + ' 和 '-' 色彩，請使用 [**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TVM \_ SETLINECOLOR**](tvm-setlinecolor.md)
</dt> </dl>

 

 






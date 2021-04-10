---
title: 'EM_SETOLECALLBACK 訊息 (Richedit .h) '
description: 提供 rich edit 控制項的 IRichEditOleCallback 物件，讓控制項用來從用戶端取得 OLE 相關的資源和資訊。
ms.assetid: bd1f8048-214c-4ac6-b826-bedabb1aaee5
keywords:
- EM_SETOLECALLBACK message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETOLECALLBACK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfc54db112bba42fc3d51b2e328fc7641990c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934545"
---
# <a name="em_setolecallback-message"></a>EM \_ SETOLECALLBACK 訊息

提供 rich edit 控制項的 [**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback) 物件，讓控制項用來從用戶端取得 OLE 相關的資源和資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**IRichEditOleCallback**](/windows/desktop/api/Richole/nn-richole-iricheditolecallback)物件的指標。 控制項會在傳回之前呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法。

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



 


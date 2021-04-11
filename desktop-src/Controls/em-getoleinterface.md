---
title: 'EM_GETOLEINTERFACE 訊息 (Richedit .h) '
description: 抓取 IRichEditOle 物件，此物件可讓用戶端用來存取 rich edit 控制項的元件物件模型， (COM) 功能。
ms.assetid: fa462c7b-29b9-4694-b7ad-6068c69ffb76
keywords:
- EM_GETOLEINTERFACE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETOLEINTERFACE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7557d40c6dcec38ce629d949a8db9915714821
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104819"
---
# <a name="em_getoleinterface-message"></a>EM \_ GETOLEINTERFACE 訊息

抓取 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 物件，此物件可讓用戶端用來存取 rich edit 控制項的元件物件模型， (COM) 功能。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接收 [**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole) 物件之指標的指標。 控制項會在傳回之前呼叫物件的 [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) 方法，因此呼叫的應用程式必須在物件完成時呼叫 [**釋放**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) 方法。

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

[**IRichEditOle**](/windows/desktop/api/Richole/nn-richole-iricheditole)
</dt> </dl>

 


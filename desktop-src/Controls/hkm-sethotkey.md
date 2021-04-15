---
title: 'HKM_SETHOTKEY 訊息 (Commctrl .h) '
description: 設定快速鍵控制項的快速鍵組合。
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508491"
---
# <a name="hkm_sethotkey-message"></a>HKM \_ SETHOTKEY 訊息

設定快速鍵控制項的快速鍵組合。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))是快速鍵的虛擬按鍵碼。 **LOWORD** 的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85))是索引鍵修飾詞，表示定義快速鍵組合的索引鍵。 如需修飾詞旗標值的清單，請參閱 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息的說明。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

永遠傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


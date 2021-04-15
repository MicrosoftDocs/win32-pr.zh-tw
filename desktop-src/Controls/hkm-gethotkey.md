---
title: 'HKM_GETHOTKEY 訊息 (Commctrl .h) '
description: 從熱鍵控制項取得快速鍵的虛擬按鍵碼和修飾詞旗標。
ms.assetid: 8b061411-604d-46ea-a082-3eca2d47d992
keywords:
- HKM_GETHOTKEY message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_GETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e23e02f32a4dd6f82f61fd735688353f48ec19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465044"
---
# <a name="hkm_gethotkey-message"></a>HKM \_ GETHOTKEY 訊息

從熱鍵控制項取得快速鍵的虛擬按鍵碼和修飾詞旗標。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回虛擬按鍵碼和修飾詞旗標。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))的 [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))是快速鍵的虛擬按鍵碼。 **LOWORD** 的 [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85))是索引鍵修飾詞，可指定定義快速鍵組合的索引鍵。 修飾詞旗標可以是下列值的組合。



| 值            | 意義      |
|------------------|--------------|
| HOTKEYF \_ ALT     | ALT 鍵      |
| HOTKEYF \_ 控制項 | 控制索引鍵  |
| HOTKEYF \_ EXT     | 擴充金鑰 |
| HOTKEYF \_ SHIFT   | SHIFT 鍵    |



 

## <a name="remarks"></a>備註

此訊息所傳回的16位值可用來作為 [**WM \_ SETHOTKEY**](/windows/desktop/inputdev/wm-sethotkey)訊息中的 *wParam* 參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


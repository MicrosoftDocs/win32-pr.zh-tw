---
title: 'TBM_SETTHUMBLENGTH 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的長度。 如果 [FIXEDLENGTH] 沒有 [TB] 樣式，則會忽略此訊息 \_ 。
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509216"
---
# <a name="tbm_setthumblength-message"></a>TBM \_ SETTHUMBLENGTH 訊息

設定捲軸中滑杆的長度。 如果 [FIXEDLENGTH] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

滑杆的長度（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TBM \_ GETTHUMBLENGTH**](tbm-getthumblength.md)
</dt> </dl>

 

 






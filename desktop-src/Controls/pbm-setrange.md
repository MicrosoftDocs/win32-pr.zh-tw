---
title: 'PBM_SETRANGE 訊息 (Commctrl .h) '
description: 設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。
ms.assetid: 251eb8c5-bedc-4e2c-90c2-e1626cb00420
keywords:
- PBM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- PBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e588170c80378082eab7e419e9425e716b8caf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843928"
---
# <a name="pbm_setrange-message"></a>PBM \_ SETRANGE 訊息

設定進度列的最小值和最大值，並重新繪製橫條以反映新的範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定最小範圍值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定最大範圍值。 最小範圍值不得為負數。 根據預設，最小值為零。 最大範圍值必須大於最小範圍值。 根據預設，最大範圍值為100。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回先前的範圍值，否則傳回零。 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))會指定先前的最小值，而 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))會指定先前的最大值。

## <a name="remarks"></a>備註

如果您未設定範圍值，系統會將最小值設定為0，並將最大值設定為100。 因為此訊息以16位不帶正負號的整數表示範圍，所以可以從0延伸至65535。 範圍中的最小值可介於0到65535之間。 同樣地，最大值可以是從0到65535。

若要設定較大的範圍，請呼叫 [**PBM \_ SETRANGE32**](pbm-setrange32.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**PBM \_ GETRANGE**](pbm-getrange.md)
</dt> <dt>

[**PBM \_ SETRANGE32**](pbm-setrange32.md)
</dt> </dl>

 


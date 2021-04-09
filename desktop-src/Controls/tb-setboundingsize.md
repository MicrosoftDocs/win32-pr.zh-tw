---
title: 'TB_SETBOUNDINGSIZE 訊息 (Commctrl .h) '
description: 設定多欄工具列控制項的周框大小。
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843056"
---
# <a name="tb_setboundingsize-message"></a>TB \_ SETBOUNDINGSIZE 訊息

\[適用于內部用途;不建議在應用程式中使用。 未來的 Windows 版本可能不支援此訊息。\]

設定多欄工具列控制項的周框大小。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**大小**](/previous-versions//dd145106(v=vs.85))結構的指標，其 **cy** 成員包含周框高度。 會忽略 (寬度) 的 **cx** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="security-considerations"></a>安全性考量

使用此訊息可能會危害程式的安全性。

## <a name="remarks"></a>備註

周框大小可控制如何將按鈕組織成資料行。 如果工具列控制項沒有 TBSTYLE EX 的多重 [**\_ \_ 列**](toolbar-extended-styles.md) 樣式，則此訊息不會有任何作用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


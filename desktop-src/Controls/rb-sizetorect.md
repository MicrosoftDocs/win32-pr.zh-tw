---
title: 'RB_SIZETORECT 訊息 (Commctrl .h) '
description: 嘗試找出指定矩形之區段的最佳版面配置。
ms.assetid: c6242b54-bd65-489b-b417-9680cc39b64a
keywords:
- RB_SIZETORECT message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SIZETORECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3db5727ee8c94d2473b503c9a81b7669bb829a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106253"
---
# <a name="rb_sizetorect-message"></a>RB \_ SIZETORECT 訊息

嘗試找出指定矩形之區段的最佳版面配置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會指定 Rebar 控制項應調整大小的矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果發生版面配置變更，則傳回非零值，否則傳回零。

## <a name="remarks"></a>備註

將會視需要排列和包裝 Rebar 群組，以配合矩形。 具有 RBBS \_ VARIABLEHEIGHT 樣式的波段會盡可能平均調整大小以符合矩形。 水準 Rebar 或垂直 Rebar 寬度的高度可能會變更，視新的版面配置而定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


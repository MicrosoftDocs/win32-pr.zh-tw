---
title: 'TB_GETITEMDROPDOWNRECT 訊息 (Commctrl .h) '
description: 取得具有樣式 BTNS 下拉式清單的工具列專案之下拉式視窗的周框 \_ 。
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024719"
---
# <a name="tb_getitemdropdownrect-message"></a>TB \_ GETITEMDROPDOWNRECT 訊息

取得具有樣式 [**BTNS \_ 下拉式清單**](toolbar-control-and-button-styles.md)的工具列專案之下拉式視窗的周框。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

要抓取周框的工具列控制項專案之以零為基底的索引。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd><a href="/previous-versions//dd162897(v=vs.85)">**矩形**</a>結構的指標，用來接收周框的資訊。 訊息寄件者負責配置此結構。 在 **矩形** 結構中傳回的座標會以用戶端座標表示。</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回非零值。

## <a name="remarks"></a>備註

專案必須具有 [ [**BTNS \_ ] 下拉式清單**](toolbar-control-and-button-styles.md) 樣式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


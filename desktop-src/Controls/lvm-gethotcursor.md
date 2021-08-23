---
title: 'LVM_GETHOTCURSOR 訊息 (Commctrl .h) '
description: 在啟用熱追蹤時，抓取指標在專案上方時所使用的 HCURSOR 值。 您可以明確地傳送此訊息，或使用 ListView \_ GetHotCursor 宏。
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540798"
---
# <a name="lvm_gethotcursor-message"></a>LVM \_ GETHOTCURSOR 訊息

在啟用熱追蹤時，抓取指標在專案上方時所使用的 HCURSOR 值。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 HCURSOR 值，此值是當啟用熱追蹤時，清單視圖控制項所使用之游標的控制碼。

## <a name="remarks"></a>備註

當設定 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 樣式時，清單視圖控制項會使用熱追蹤和暫留選取專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'LVM_GETHOTCURSOR 訊息 (Commctrl .h) '
description: 在啟用熱追蹤時，抓取指標在專案上方時所使用的 HCURSOR 值。 您可以明確地傳送此訊息，或使用 ListView \_ GetHotCursor 宏。
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR message Windows 控制項
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
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686284"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






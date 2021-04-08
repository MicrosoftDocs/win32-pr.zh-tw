---
title: 'LVM_SETHOTCURSOR 訊息 (Commctrl .h) '
description: 設定當啟用熱追蹤時，清單視圖控制項所使用的 HCURSOR 值。
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685519"
---
# <a name="lvm_sethotcursor-message"></a>LVM \_ SETHOTCURSOR 訊息

設定當啟用熱追蹤時，清單視圖控制項所使用的 HCURSOR 值。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) 宏。 若要檢查是否已啟用熱追蹤，請呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要設定之資料指標的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 HCURSOR 值，此值為先前的熱資料指標。

## <a name="remarks"></a>備註

當設定 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 樣式時，清單視圖控制項會使用熱追蹤和暫留選取專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


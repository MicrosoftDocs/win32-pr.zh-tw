---
title: 'HDM_SETHOTDIVIDER 訊息 (Commctrl .h) '
description: 變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。 您可以明確地傳送此訊息，或使用標頭 \_ SetHotDivider 宏。
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- HDM_SETHOTDIVIDER message Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094500"
---
# <a name="hdm_sethotdivider-message"></a>HDM \_ SETHOTDIVIDER 訊息

變更標題專案之間的分隔線色彩，以表示外部拖放作業的目的地。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 所代表的數值型別。 這個值可以是下列其中一個值：



| 值                                                                                                                                    | 意義                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | 表示 *lParam* 保存指標的用戶端座標。<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | 表示 *lParam* 保留分割索引值。<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

*LParam* 中保留的值會根據 *wParam* 的值來解讀。

如果 *wParam* 為 **TRUE**，則 *lParam* 代表指標的 x 和 y 座標。 X 座標是在低字組中，而 y 座標則是在高字中。 當標題控制項接收訊息時，它會根據 *lParam* 座標反白顯示適當的分隔線。

如果 *wParam* 為 **FALSE**，則 *lParam* 代表要反白顯示之分隔線的整數索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回等於控制項反白顯示之分隔線索引的值。

## <a name="remarks"></a>備註

當標題控制項具有 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式時，此訊息會產生一個效果。 當控制項的擁有者以手動方式處理拖放作業時，會使用 **HDM \_ SETHOTDIVIDER** 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






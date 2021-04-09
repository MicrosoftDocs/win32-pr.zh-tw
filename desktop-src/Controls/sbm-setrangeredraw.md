---
title: 'SBM_SETRANGEREDRAW 訊息 (Winuser .h) '
description: 應用程式會將 SBM \_ SETRANGEREDRAW 訊息傳送到捲軸控制項，以設定最小和最大位置值，以及重新繪製控制項。
ms.assetid: badb58cc-9e3a-4766-a67f-631a7feb6285
keywords:
- SBM_SETRANGEREDRAW message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETRANGEREDRAW
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37c77a8f062ba3c7a8b73adc4338a11cdcf59442
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024578"
---
# <a name="sbm_setrangeredraw-message"></a>SBM \_ SETRANGEREDRAW 訊息

應用程式會將 **SBM \_ SETRANGEREDRAW** 訊息傳送到捲軸控制項，以設定最小和最大位置值，以及重新繪製控制項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定最小滾動位置。

</dd> <dt>

*lParam* 
</dt> <dd>

指定最大滾動位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

**ComCtl32.dll 5.0 版**：如果捲動方塊的位置已變更，則傳回值是捲動方塊的先前位置;否則，它是零。

**ComCtl32.dll 版本 6.0**：捲動方塊的目前位置，不論是否已變更。

## <a name="remarks"></a>備註

預設的最小和最大位置值為零。 *WParam* 和 *lParam* 參數所指定值之間的差異不得大於 MAXLONG。

如果最小和最大位置值相等，則捲軸控制項是隱藏的，且實際上是停用的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**SBM \_ GETPOS**](sbm-getpos.md)
</dt> <dt>

[**SBM \_ GETRANGE**](sbm-getrange.md)
</dt> <dt>

[**SBM \_ SETPOS**](sbm-setpos.md)
</dt> <dt>

[**SBM \_ SETRANGE**](sbm-setrange.md)
</dt> </dl>

 

 






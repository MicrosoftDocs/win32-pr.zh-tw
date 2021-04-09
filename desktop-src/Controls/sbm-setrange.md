---
title: 'SBM_SETRANGE 訊息 (Winuser .h) '
description: 傳送 SBM \_ SETRANGE 訊息來設定捲軸控制項的最小和最大位置值。
ms.assetid: 9cf84354-3944-4c10-9b59-39427b840868
keywords:
- SBM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_SETRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7a720531ae58fdb0712b8f23fd1aef88b3e4caa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844192"
---
# <a name="sbm_setrange-message"></a>SBM \_ SETRANGE 訊息

傳送 **SBM \_ SETRANGE** 訊息來設定捲軸控制項的最小和最大位置值。

應用程式不應直接傳送此訊息。 相反地，它們應該使用 [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) 函數。 視窗會透過其 [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。 執行自訂捲軸控制項的應用程式必須回應這些訊息， **SetScrollRange** 函數才能正常運作。

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

[**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)
</dt> </dl>

 


---
title: 'TBM_GETBUDDY 訊息 (Commctrl .h) '
description: 抓取指定位置上的 [查看點] 控制項好友視窗控制碼。 指定的位置是相對於控制項的方向 (水準或垂直) 。
ms.assetid: 69e4e467-150d-4505-b1c2-2ed9dd83f1a6
keywords:
- TBM_GETBUDDY message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4c076f001a1dff62541c3aa32bc12744b30c012
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935153"
---
# <a name="tbm_getbuddy-message"></a>TBM \_ GETBUDDY 訊息

抓取指定位置上的 [查看點] 控制項好友視窗控制碼。 指定的位置是相對於控制項的方向 (水準或垂直) 。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指出將會依相對位置抓取哪個合作者視窗控制碼的值。 這個值可以是下列其中一個值：



| 值                                                                                                                                    | 意義                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | 抓取對等的合作者左邊的控制碼。 如果 [顯示] 控制項使用的是 [ [**tb] \_ 垂直**](trackbar-control-styles.md) 樣式，則訊息將會抓取 [資訊] 上方的合作者。<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | 抓取對等的合作者右邊的控制碼。 如果 [顯示] 控制項使用的是 [ [**tb] \_ 垂直**](trackbar-control-styles.md) 樣式，則訊息將會抓取下方的合作者。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

在 *wParam* 所指定的位置上，傳回好友視窗的控制碼，如果該位置沒有任何好友視窗，則 **為 Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






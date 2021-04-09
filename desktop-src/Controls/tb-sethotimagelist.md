---
title: 'TB_SETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 設定工具列控制項將用來顯示熱按鈕的影像清單。
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934784"
---
# <a name="tb_sethotimagelist-message"></a>TB \_ SETHOTIMAGELIST 訊息

設定工具列控制項將用來顯示熱按鈕的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

將設定之影像清單的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前用來顯示熱按鈕的影像清單控制碼，如果先前未設定任何影像清單，則傳回 **Null** 。

## <a name="remarks"></a>備註

當游標停留在按鈕上時，按鈕會是經常性的。 Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






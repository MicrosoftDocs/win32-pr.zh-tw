---
title: 'TB_GETHOTIMAGELIST 訊息 (Commctrl .h) '
description: 抓取工具列控制項用來顯示熱按鈕的影像清單。
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- TB_GETHOTIMAGELIST message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104028"
---
# <a name="tb_gethotimagelist-message"></a>TB \_ GETHOTIMAGELIST 訊息

抓取工具列控制項用來顯示熱按鈕的影像清單。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回影像清單的控制碼，控制項會使用此控制碼來顯示熱按鈕; 如果未設定任何熱影像清單，則傳回 **Null** 。

## <a name="remarks"></a>備註

當游標停留在按鈕上時，按鈕會是經常性的。 Toolbar 控制項必須具有 [**TBSTYLE 的 \_**](toolbar-control-and-button-styles.md) 一般或 [**TBSTYLE \_ 清單**](toolbar-control-and-button-styles.md) 樣式，才能有熱專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






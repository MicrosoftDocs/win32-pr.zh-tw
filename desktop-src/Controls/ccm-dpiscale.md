---
title: 'CCM_DPISCALE 訊息 (Commctrl .h) '
description: 在 Tree-View 控制項、List-View 控制項、ComboBoxEx 控制項、標題控制項、按鈕、工具列控制項、動畫控制項和影像清單中，啟用每英寸的自動大點 (DPI) 縮放比例。
ms.assetid: 3c751f10-992c-41f8-8f0b-3dc58f0591e4
keywords:
- CCM_DPISCALE message Windows 控制項
topic_type:
- apiref
api_name:
- CCM_DPISCALE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef978f486f370adf9872d28e1accbacc37a6de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104519"
---
# <a name="ccm_dpiscale-message"></a>CCM \_ DPISCALE 訊息

在 [樹狀檢視控制項](tree-view-controls.md)、 [清單視圖控制項](list-view-control-reference.md)、 [ComboBoxEx 控制項](comboboxex-controls.md)、 [標題控制項](header-controls.md)、 [按鈕](buttons.md)、 [工具列控制項](toolbar-controls-overview.md)、 [動畫控制項](animation-control-overview.md)和 [影像清單](image-lists.md)中，啟用每英寸的自動大點 (DPI) 縮放比例。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

設定為 **TRUE**。

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

快速啟動和 [工作列](/windows/desktop/shell/taskbar) 不應指定 DPI 縮放比例，因為影像已經過調整。

任何使用以 SmallIcon 度量建立之影像清單的控制項，都不應該調整其圖示。

> [!Note]  
> 若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


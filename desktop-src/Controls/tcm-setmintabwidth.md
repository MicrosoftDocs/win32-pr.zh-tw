---
title: 'TCM_SETMINTABWIDTH 訊息 (Commctrl .h) '
description: 設定索引標籤控制項中專案的最小寬度。 您可以使用 TabCtrl SetMinTabWidth 宏明確地傳送此訊息 \_ 。
ms.assetid: c0be3d4e-774c-4233-820f-01ffbb69ecf0
keywords:
- TCM_SETMINTABWIDTH message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETMINTABWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87208275ed52c638751352761961ce1f42e6944a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969557"
---
# <a name="tcm_setmintabwidth-message"></a>TCM \_ SETMINTABWIDTH 訊息

設定索引標籤控制項中專案的最小寬度。 您可以使用 [**TabCtrl \_ SetMinTabWidth**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setmintabwidth) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

要針對索引標籤控制項專案設定的最小寬度。 如果此參數設定為-1，此控制項將會使用預設的定位鍵寬度。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 INT 值，表示先前的最小索引標籤寬度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






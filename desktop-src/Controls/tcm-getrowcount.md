---
title: 'TCM_GETROWCOUNT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中目前的索引標籤數目。 您可以使用 TabCtrl GetRowCount 宏明確地傳送此訊息 \_ 。
ms.assetid: ef104374-1030-46c3-876e-083df73854ab
keywords:
- TCM_GETROWCOUNT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETROWCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e67b2ac40834075b31ccf2415a52c96448b8143dde3d6bc67f9c515e1f601a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104868"
---
# <a name="tcm_getrowcount-message"></a>TCM \_ GETROWCOUNT 訊息

抓取索引標籤控制項中目前的索引標籤數目。 您可以使用 [**TabCtrl \_ GetRowCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getrowcount) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回索引標籤的資料列數目。

## <a name="remarks"></a>備註

只有具有 [**TCS \_ 多行**](tab-control-styles.md) 樣式的索引標籤控制項可以有多個資料列的索引標籤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






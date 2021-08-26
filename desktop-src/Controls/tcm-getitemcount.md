---
title: 'TCM_GETITEMCOUNT 訊息 (Commctrl .h) '
description: 抓取索引標籤控制項中的索引標籤數目。 您可以使用 TabCtrl GetItemCount 宏明確地傳送此訊息 \_ 。
ms.assetid: a8ec7d66-fe44-45ca-8f6c-4e75752ebe95
keywords:
- TCM_GETITEMCOUNT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9bbb954c75a19f15ecee9f946e338a186b6e9903a405aa1c550fb0ccc31392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104878"
---
# <a name="tcm_getitemcount-message"></a>TCM \_ GETITEMCOUNT 訊息

抓取索引標籤控制項中的索引標籤數目。 您可以使用 [**TabCtrl \_ GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitemcount) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回專案的數目，否則為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






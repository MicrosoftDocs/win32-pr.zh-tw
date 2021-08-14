---
title: 'MCM_GETCALENDARGRIDINFO 訊息 (Commctrl .h) '
description: 取得行事曆方格的相關資訊。
ms.assetid: 6b385362-f963-4041-bc9f-d2b7a890c9b4
keywords:
- MCM_GETCALENDARGRIDINFO 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCALENDARGRIDINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26365b940b17617b1f00b93697fc78fa759dd2599d3398ccb8d92725159a70cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170165"
---
# <a name="mcm_getcalendargridinfo-message"></a>MCM \_ GETCALENDARGRIDINFO 訊息

取得行事曆方格的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MCGRIDINFO**](/windows/win32/api/commctrl/ns-commctrl-mcgridinfo)結構的指標，其中包含行事曆方格的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則 **為 TRUE** ，否則為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






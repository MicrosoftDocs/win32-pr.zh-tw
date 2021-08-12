---
title: 'LVM_SORTGROUPS 訊息 (Commctrl .h) '
description: 使用應用程式定義的比較函式，在清單視圖控制項內依識別碼排序群組。
ms.assetid: 553e96d6-a982-4482-8fba-ef11a74fb82e
keywords:
- LVM_SORTGROUPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SORTGROUPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ec17d46205746495cfe95a2af83690644dd8bfced26041906bdea4f809fb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670782"
---
# <a name="lvm_sortgroups-message"></a>LVM \_ SORTGROUPS 訊息

使用應用程式定義的比較函式，在清單視圖控制項內依識別碼排序群組。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>應用程式定義的比較函式 <a href="/windows/desktop/api/commctrl/nc-commctrl-pfnlvgroupcompare">LVGroupCompare</a>的指標。</dd> <dt>

*lParam* 
</dt> <dd>應用程式定義資訊的 Void 指標。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回1，否則傳回0。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVGroupCompare**](/windows/win32/api/commctrl/nc-commctrl-pfnlvgroupcompare)
</dt> </dl>


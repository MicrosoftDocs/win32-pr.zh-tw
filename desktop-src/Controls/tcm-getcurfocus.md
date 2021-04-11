---
title: 'TCM_GETCURFOCUS 訊息 (Commctrl .h) '
description: 傳回在索引標籤控制項中具有焦點之專案的索引。 您可以使用 TabCtrl GetCurFocus 宏明確地傳送此訊息 \_ 。
ms.assetid: ae6ee159-c769-41d6-b0bb-2a9ade4c0e71
keywords:
- TCM_GETCURFOCUS message Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETCURFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0d0f3d2bbd4a7cf0ab2a63c5a988f60768eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934948"
---
# <a name="tcm_getcurfocus-message"></a>TCM \_ GETCURFOCUS 訊息

傳回在索引標籤控制項中具有焦點之專案的索引。 您可以使用 [**TabCtrl \_ GetCurFocus**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcurfocus) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回具有焦點之索引標籤專案的索引。

## <a name="remarks"></a>備註

具有焦點的專案可能會與選取的專案不同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






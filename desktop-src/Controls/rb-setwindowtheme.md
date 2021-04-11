---
title: 'RB_SETWINDOWTHEME 訊息 (Commctrl .h) '
description: 設定 Rebar 控制項的視覺化樣式。
ms.assetid: 5b32b354-3e25-4d02-9334-cc57acf41a73
keywords:
- RB_SETWINDOWTHEME message Windows 控制項
topic_type:
- apiref
api_name:
- RB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e136562394d26dd56d8d4c0c9ae916948144dbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104778"
---
# <a name="rb_setwindowtheme-message"></a>RB \_ SETWINDOWTHEME 訊息

設定 Rebar 控制項的視覺化樣式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

Unicode 字串的指標，其中包含要設定的 Rebar 視覺效果樣式。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






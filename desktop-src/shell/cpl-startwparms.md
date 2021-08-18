---
description: 傳送以通知 CPlApplet，使用者已選擇與指定對話方塊相關聯的圖示。 CPlApplet 應該會顯示對應的對話方塊，並執行任何使用者指定的工作。
title: 'CPL_STARTWPARMS 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f836f868b81daa49e87eb4efc804442bed25690ce126852891327d0eb042aaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460607"
---
# <a name="cpl_startwparms-message"></a>CPL \_ STARTWPARMS 訊息

傳送以通知 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ，使用者已選擇與指定對話方塊相關聯的圖示。 **CPlApplet** 應該會顯示對應的對話方塊，並執行任何使用者指定的工作。

## <a name="parameters"></a>參數

<dl> <dt>

*uAppNum* 
</dt> <dd>

對話方塊編號。 此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。

</dd> <dt>

*lpszExtra* 
</dt> <dd>

字串，包含執行的其他指示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已處理訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

**CPL \_STARTWPARMS** 類似于 [**CPL \_ DBLCLK**](cpl-dblclk.md) ，但可讓您將字串傳遞至 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 而不是 **int**。您可以使用此字串作為提供詳細執行指示的彈性方式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



 

 

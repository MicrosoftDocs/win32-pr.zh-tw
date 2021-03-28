---
description: 當使用者按兩下應用程式所支援之對話方塊的圖示時，傳送至主控台應用程式的 CPlApplet 函式。
title: 'CPL_DBLCLK 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 68d74372-2fc2-45ed-8f77-574b943d28fa
api_name:
- CPL_DBLCLK
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d6c67204c7b4fae5275e50d428a0371af4cf2e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991086"
---
# <a name="cpl_dblclk-message"></a>CPL \_ DBLCLK 訊息

當使用者按兩下應用程式所支援之對話方塊的圖示時，傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式。

## <a name="parameters"></a>參數

<dl> <dt>

*uAppNum* 
</dt> <dd>

對話方塊編號。 此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。

</dd> <dt>

*lData* 
</dt> <dd>

主控台應用程式載入至對話方塊之 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的 **lpData** 成員的值。 應用程式會載入 **lpData** 成員，以回應 [**CPL \_ INQUIRE**](cpl-inquire.md) 或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則傳回值為零。否則，則為非零。

## <a name="remarks"></a>備註

為了回應此訊息，主控台的應用程式必須顯示對應的對話方塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPL \_ 選取**](cpl-select.md)
</dt> </dl>

 

 

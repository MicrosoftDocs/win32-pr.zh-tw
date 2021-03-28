---
description: 當控制主控台的應用程式關閉時，傳送至主控台應用程式的 CPlApplet 函式。 控制應用程式會針對應用程式支援的每個對話方塊傳送一次訊息。
title: 'CPL_STOP 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972041"
---
# <a name="cpl_stop-message"></a>CPL \_ 停止訊息

當控制主控台的應用程式關閉時，傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式。 控制應用程式會針對應用程式支援的每個對話方塊傳送一次訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*uAppNum* 
</dt> <dd>

對話方塊編號。

</dd> <dt>

*lData* 
</dt> <dd>

主控台應用程式載入至對話方塊之 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的 **lpData** 成員的值。 應用程式會載入 **lpData** 成員，以回應 [**CPL \_ INQUIRE**](cpl-inquire.md) 或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

為了回應這則訊息，主控台的應用程式必須在指定的對話方塊中執行清除。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPL \_ 結束**](cpl-exit.md)
</dt> <dt>

[**CPL \_ GETCOUNT**](cpl-getcount.md)
</dt> </dl>

 

 

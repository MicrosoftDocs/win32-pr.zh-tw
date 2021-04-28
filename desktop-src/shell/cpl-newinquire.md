---
description: CPL_NEWINQUIRE 訊息傳送至主控台應用程式的 CPlApplet 函式，以要求應用程式所支援之對話方塊的相關資訊。
title: 'CPL_NEWINQUIRE 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104436"
---
# <a name="cpl_newinquire-message"></a>CPL \_ NEWINQUIRE 訊息

傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以要求應用程式所支援之對話方塊的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*uAppNum* 
</dt> <dd>

對話方塊編號。 此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。

</dd> <dt>

*lpncpli* 
</dt> <dd>

[**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的位址。 主控台應用程式應該以對話方塊的相關資訊來填滿此結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

為了獲得更好的效能，大部分的應用程式應忽略 **cpl \_ NEWINQUIRE** ，並改為處理 [**cpl \_ 查詢**](cpl-inquire.md) 訊息。

主控台會針對您的應用程式所支援的每個對話方塊傳送 **CPL \_ NEWINQUIRE** 訊息一次。 主控台也會為每個對話方塊傳送 [**CPL \_ 查詢**](cpl-inquire.md) 訊息。 這些訊息會緊接在 [**CPL \_ GETCOUNT**](cpl-getcount.md) 訊息之後傳送。 不過，系統不保證會傳送 **cpl \_ 查詢** 和 **cpl \_ NEWINQUIRE** 訊息的順序。

您可以在收到 [**CPL \_ 查詢**](cpl-inquire.md)時執行對話方塊的初始化。 如果您必須配置記憶體，請這麼做以回應 [**CPL \_ INIT**](cpl-init.md) 訊息。

[**CPL \_INQUIRE**](cpl-inquire.md) 是慣用的訊息。 這是因為 **CPL \_ NEWINQUIRE** 會以系統無法快取的形式傳回信息。 因此，每次主控台需要資訊時，都必須載入處理 **CPL \_ NEWINQUIRE** 的應用程式，從而大幅降低效能。

唯一應該使用 **CPL \_ NEWINQUIRE** 的應用程式，是需要變更其圖示或根據電腦狀態顯示字串的應用程式。 在此情況下，您的 [**cpl \_ 查詢**](cpl-inquire.md)處理常式應該 \_ \_ 為 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的 **idIcon**、 **idName** 或 **idInfo** 成員指定 CPL 動態 RES 值，而不是指定有效的資源識別碼。 這會導致主控台在每次需要圖示和顯示字串時傳送 **CPL \_ NEWINQUIRE** 訊息，讓您根據電腦目前的狀態指定資訊。 當然，這比使用快取的資訊來得慢很多。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



 

 

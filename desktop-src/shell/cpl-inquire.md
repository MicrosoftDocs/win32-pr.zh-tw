---
description: CPL_INQUIRE 訊息傳送至主控台應用程式的 CPlApplet 函式，以要求應用程式所支援之對話方塊的相關資訊。
title: 'CPL_INQUIRE 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5998e26eab79d3e5f0b9e3628614e1cc2ecbfb7040e866a898a09ad54fa49f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710718"
---
# <a name="cpl_inquire-message"></a>CPL \_ 查詢訊息

傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以要求應用程式所支援之對話方塊的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*uAppNum* 
</dt> <dd>

對話方塊編號。 此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。

</dd> <dt>

*lpcpli* 
</dt> <dd>

[**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的位址。 應用程式必須在此結構中填入圖示的資源識別碼、簡短名稱、描述，以及與對話方塊相關聯的任何使用者定義值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。

## <a name="remarks"></a>備註

主控台針對您的應用程式所支援的每個對話方塊傳送 **CPL \_ 查詢** 訊息一次。 主控台也會為每個對話方塊傳送 [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。 這些訊息會緊接在 [**CPL \_ GETCOUNT**](cpl-getcount.md) 訊息之後傳送。 不過，系統不保證會傳送 **cpl \_ 查詢** 和 **cpl \_ NEWINQUIRE** 訊息的順序。

您可以在收到 **CPL \_ 查詢** 時執行對話方塊的初始化。 如果您必須配置記憶體，請這麼做以回應 [**CPL \_ INIT**](cpl-init.md) 訊息。

[**CPL \_ NEWINQUIRE**](cpl-newinquire.md)訊息會以系統無法快取的形式傳回信息。 基於這個理由，大部分的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式都應該處理 **cpl \_ 查詢** 並忽略 **CPL \_ NEWINQUIRE**。

唯一應該使用 [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) 的應用程式，是需要變更其圖示或根據電腦狀態顯示字串的應用程式。 在此情況下，您的 **cpl \_ 查詢** 處理常式應該 \_ \_ 為 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的 **idIcon**、 **idName** 或 **idInfo** 成員指定 CPL 動態 RES 值，而不是指定有效的資源識別碼。 這會導致主控台在每次需要圖示和顯示字串時傳送 **CPL \_ NEWINQUIRE** 訊息，讓您根據電腦目前的狀態指定資訊。 這比使用快取的資訊來得慢很多。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



 

 

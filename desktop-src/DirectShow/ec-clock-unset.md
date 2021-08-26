---
description: 時鐘提供者已中斷連線。
ms.assetid: 0a885b7a-840d-4112-85f7-ff6f2d87bb75
title: 'EC_CLOCK_UNSET (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7bc9daecb9e39ca2d121c9fa903b2e4e8257e6247f28d718ca093b302cc2e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998218"
---
# <a name="ec_clock_unset"></a>EC \_ 時鐘未設定 \_

時鐘提供者已中斷連線。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

零個。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

零個。

</dd> </dl>

## <a name="default-action"></a>預設動作

篩選 Graph 管理員會在下一個 pause 或 run 命令上選擇新的參考時鐘。 它也會將事件轉送到應用程式。

## <a name="remarks"></a>備註

當時鐘提供的篩選器的 pin 已中斷連線時，KSProxy 會通知此事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 





---
description: 圖形正在卸載範例，以提供品質控制。
ms.assetid: a21fe766-58a5-4851-a282-883374287e18
title: 'EC_QUALITY_CHANGE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a9c2b540a5740812050532d4d4e6e45fb334eaff9927148471aada09ab1a434
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043358"
---
# <a name="ec_quality_change"></a>EC \_ 品質 \_ 變更

圖形正在卸載範例，以提供品質控制。

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

無。

## <a name="remarks"></a>備註

如果篩選器卸載範例以回應品質控制訊息，則會傳送此事件。 它只會在調整品質層級時傳送事件，而不是針對它所卸載的每個樣本。 如需詳細資訊，請參閱 [品質控制管理](quality-control-management.md)。

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

 

 





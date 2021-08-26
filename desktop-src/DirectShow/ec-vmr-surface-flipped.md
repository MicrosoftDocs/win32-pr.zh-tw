---
description: 當 VMR 7's 配置器展示者在呈現的介面上呼叫 DirectDraw Flip 方法時傳送。 這可讓 VMR 將其 DirectXVA 資料表與 DirectDraw 的翻轉鏈同步處理。
ms.assetid: e298857b-0579-48b4-add0-72320bc52d63
title: 'EC_VMR_SURFACE_FLIPPED (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c352af01ee31728b41aa276d14ca64b7c3fa6770bb4c9328a8c4ee5e91bb07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043348"
---
# <a name="ec_vmr_surface_flipped"></a>已 \_ 翻轉 EC VMR \_ 介面 \_

當 VMR 7's 配置器展示者在呈現的介面上呼叫 DirectDraw Flip 方法時傳送。 這可讓 VMR 將其 DirectXVA 資料表與 DirectDraw 的翻轉鏈同步處理。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**HRESULT**) 從 DirectDraw Flip 方法傳回的狀態碼。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

自訂配置器-VMR-7 的展示者應該傳送此事件。 此事件不會轉送至應用程式，而且不會與 VMR-9 的配置器-展示者一起使用。

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

 

 





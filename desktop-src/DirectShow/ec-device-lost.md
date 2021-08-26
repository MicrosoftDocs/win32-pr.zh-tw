---
description: 隨插即用裝置已移除或變成可供使用。
ms.assetid: 0640ba96-22a5-4b82-bd9f-117b67dee311
title: 'EC_DEVICE_LOST (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4868890967d6448226c1f000ab06b7ccbcf7a06e3062d1cdef03e0ad960bc7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998158"
---
# <a name="ec_device_lost"></a>EC \_ 裝置 \_ 遺失

隨插即用裝置已移除或變成可供使用。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

 (**iunknown** \*) 指標指向代表裝置之篩選的 **iunknown** 介面。

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

如果裝置已移除，則為零; 如果裝置再次可用，則為1。

</dd> </dl>

## <a name="default-action"></a>預設動作

無。

## <a name="remarks"></a>備註

當裝置再次變成可用時，裝置篩選器的先前狀態將不再有效。 應用程式必須重建圖形，才能使用裝置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dshow。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[裝置移除通知](device-removal-notification.md)
</dt> <dt>

[事件通知碼](event-notification-codes.md)
</dt> <dt>

[DirectShow 中的事件通知](event-notification-in-directshow.md)
</dt> </dl>

 

 





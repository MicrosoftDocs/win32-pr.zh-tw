---
description: VMR 已選取其轉譯機制時傳送。
ms.assetid: 815d1254-c6e3-4a6c-ba4a-bf3da7d35d1f
title: 'EC_VMR_RENDERDEVICE_SET (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9855b23e25a2c3b955c1499b9505efffcc5637e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977573"
---
# <a name="ec_vmr_renderdevice_set"></a>EC \_ VMR \_ RENDERDEVICE \_ 集

VMR 已選取其轉譯機制時傳送。

## <a name="parameters"></a>參數

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

可能是下列其中一個值：



| 值                        | 意義                                                  |
|------------------------------|----------------------------------------------------------|
| VMR 轉譯裝置重迭 \_ \_ \_ | VMR 只會轉譯成重迭表面 (VMR-7) 。 |
| VMR \_ 轉譯 \_ 裝置 \_ VIDMEM  | VMR 會轉譯成視訊記憶體。                     |
| VMR \_ 轉譯 \_ 裝置 \_ SYSMEM  | VMR 只會轉譯為系統記憶體 (VMR-7) 。       |



 

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

未使用。

</dd> </dl>

## <a name="remarks"></a>備註

此事件是由 VMR-7 和 VMR-9 所傳送，而且會轉送到應用程式。 請注意，VMR-9 僅支援視訊記憶體呈現目標。

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

 

 





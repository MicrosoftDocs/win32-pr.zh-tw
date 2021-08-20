---
title: 'ICM_DRAW_GETTIME 訊息 (Vfw .h) '
description: ICM \_ DRAW \_ GETTIME 訊息會要求轉譯驅動程式，以控制繪製畫面格的時間，以傳回其內部時鐘的目前值。 您可以使用 ICDrawGetTime 宏明確地傳送此訊息。
ms.assetid: 77f0a322-c0bc-4cfe-a3d0-7633cf8d682a
keywords:
- ICM_DRAW_GETTIME 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_DRAW_GETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ecf151b0c22b4de96421b4c11239ce147a21b6d60808b1d84506f3bad699954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987368"
---
# <a name="icm_draw_gettime-message"></a>ICM \_繪製 \_ GETTIME 訊息

**ICM \_ DRAW \_ GETTIME** 訊息會要求轉譯驅動程式，以控制繪製畫面格的時間，以傳回其內部時鐘的目前值。 您可以使用 [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) 宏明確地傳送此訊息。


```C++
ICM_DRAW_GETTIME 
wParam = (DWORD_PTR) (LPVOID) lplTime; 
lParam = 0; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="lplTime"></span><span id="lpltime"></span><span id="LPLTIME"></span>*lplTime*
</dt> <dd>

包含目前時間的位址。 傳回值應該在範例中指定。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則會傳回 ICERR \_ OK，否則會傳回錯誤。

## <a name="remarks"></a>備註

這則訊息通常是由執行自己的非同步解壓縮、時間和繪圖的硬體所支援。 如果使用硬體作為同步處理主機，也可以傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[影片壓縮管理員](video-compression-manager.md)
</dt> <dt>

[影片壓縮訊息](video-compression-messages.md)
</dt> </dl>

 

 






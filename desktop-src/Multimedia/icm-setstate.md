---
title: 'ICM_SETSTATE 訊息 (Vfw .h) '
description: ICM \_ SETSTATE 訊息會通知視訊壓縮驅動程式，以設定壓縮程式的狀態。 您可以使用 ICSetState 宏明確地傳送此訊息。
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- ICM_SETSTATE 訊息 Windows 多媒體
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525808"
---
# <a name="icm_setstate-message"></a>ICM \_SETSTATE 訊息

**ICM \_ SETSTATE** 訊息會通知視訊壓縮驅動程式，以設定壓縮程式的狀態。 您可以使用 [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) 宏明確地傳送此訊息。


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*光伏*
</dt> <dd>

包含設定資料之記憶體區塊的指標。 您可以為此參數指定 **Null** ，以將壓縮程式重設為預設狀態。

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*Cb*
</dt> <dd>

記憶體區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回壓縮程式所使用的位元組數目，否則為零。

## <a name="remarks"></a>備註

這則訊息所使用的資訊是私用的，而且是指定之壓縮程式的特定資訊。 用戶端應用程式應該只使用此訊息來還原先前使用 [**ICM \_ >getstate**](icm-getstate.md)訊息所取得的資訊，而且應該使用 ICM 設定訊息來調整視訊壓縮驅動程式的 [**\_ 設定**](icm-configure.md)。

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

 

 






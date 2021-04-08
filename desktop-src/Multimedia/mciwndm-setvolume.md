---
title: 'MCIWNDM_SETVOLUME 訊息 (Vfw .h) '
description: MCIWNDM \_ SETVOLUME 訊息會設定 MCI 裝置的磁片區層級。 您可以使用 MCIWndSetVolume 宏明確地傳送此訊息。
ms.assetid: 04151588-b761-447a-9a57-808c034c3059
keywords:
- MCIWNDM_SETVOLUME message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_SETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2215f8df3ea6f7b36b224318ebac68175ff9c265
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685590"
---
# <a name="mciwndm_setvolume-message"></a>MCIWNDM \_ SETVOLUME 訊息

**MCIWNDM \_ SETVOLUME** 訊息會設定 MCI 裝置的磁片區層級。 您可以使用 [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) 宏明確地傳送此訊息。


```C++
MCIWNDM_SETVOLUME 
wParam = 0; 
lParam = (LPARAM) (UINT) iVol; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="iVol"></span><span id="ivol"></span><span id="IVOL"></span>*iVol*
</dt> <dd>

新的磁片區層級。 針對一般磁片區層級指定1000。 針對較大的磁片區指定較高的值，或針對較低的磁片區指定較低的值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume)
</dt> </dl>

 

 






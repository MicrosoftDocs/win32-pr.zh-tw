---
title: 'MCIWNDM_GETDEVICE 訊息 (Vfw .h) '
description: MCIWNDM \_ GETDEVICE 訊息會抓取目前開啟之 MCI 裝置的名稱。 您可以使用 MCIWndGetDevice 宏明確地傳送此訊息。
ms.assetid: e69a73a6-a927-4536-98c7-ee7d5b16668a
keywords:
- MCIWNDM_GETDEVICE message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32664508a577db9d5a077e3cb4fd00aab34fbdf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464520"
---
# <a name="mciwndm_getdevice-message"></a>MCIWNDM \_ GETDEVICE 訊息

**MCIWNDM \_ GETDEVICE** 訊息會抓取目前開啟之 MCI 裝置的名稱。 您可以使用 [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) 宏明確地傳送此訊息。


```C++
MCIWNDM_GETDEVICE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPVOID) lp; 
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="len"></span><span id="LEN"></span>*萊恩*
</dt> <dd>

緩衝區的大小（以位元組為單位）。

</dd> <dt>

<span id="lp"></span><span id="LP"></span>*Lp*
</dt> <dd>

應用程式定義之緩衝區的指標，以傳回裝置名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功則傳回零，否則傳回非零值。

## <a name="remarks"></a>備註

如果包含裝置名稱的以 null 終止的字串長度超過緩衝區，MCIWnd 會將它截斷。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



 

 






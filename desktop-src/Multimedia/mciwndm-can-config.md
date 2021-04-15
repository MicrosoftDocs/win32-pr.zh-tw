---
title: 'MCIWNDM_CAN_CONFIG 訊息 (Vfw .h) '
description: MCIWNDM \_ 可設定 \_ 訊息可判斷 MCI 裝置是否可顯示 [設定] 對話方塊。 您可以使用 MCIWndCanConfig 宏明確地傳送此訊息。
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- MCIWNDM_CAN_CONFIG message Windows 多媒體
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466921"
---
# <a name="mciwndm_can_config-message"></a>MCIWNDM \_ 可以設定 \_ 訊息

**MCIWNDM \_ 可 \_** 設定訊息可判斷 MCI 裝置是否可顯示 [設定] 對話方塊。 您可以使用 [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) 宏明確地傳送此訊息。


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>傳回值

如果裝置支援設定，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                       |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Vfw。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 






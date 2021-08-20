---
description: 應用程式會將 WM \_ MDIICONARRANGE 訊息傳送至多重文件介面， (mdi) 用戶端視窗來排列所有最小化的 mdi 子視窗。 它不會影響未最小化的子視窗。
ms.assetid: 935b9e29-224d-449e-b89f-b6062bed7702
title: 'WM_MDIICONARRANGE 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacb38a03ab71f185bd4db0618e3f0180515f7af370e0cab3cc1ac9010dd3edd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030806"
---
# <a name="wm_mdiiconarrange-message"></a>WM \_ MDIICONARRANGE 訊息

應用程式會將 **WM \_ MDIICONARRANGE** 訊息傳送至多重文件介面， (mdi) 用戶端視窗來排列所有最小化的 mdi 子視窗。 它不會影響未最小化的子視窗。


```C++
#define WM_MDIICONARRANGE               0x0228
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**WM \_ MDICASCADE**](wm-mdicascade.md)
</dt> <dt>

[**WM \_ MDITILE**](wm-mditile.md)
</dt> <dt>

**概念**
</dt> <dt>

[多個檔介面](multiple-document-interface.md)
</dt> </dl>

 

 





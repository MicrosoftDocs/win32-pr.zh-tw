---
description: 抓取目前視窗的功能表控制碼。
ms.assetid: a2f6e917-39ff-42a3-8ff4-ce01db3ef9ea
title: 'MN_GETHMENU 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cfc1eb6086f94f64e1a0e152e6f86fe89a0ea0278a6c4cc25a487edb6f93ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089928"
---
# <a name="mn_gethmenu-message"></a>MN \_ GETHMENU 訊息

抓取目前視窗的功能表控制碼。


```C++
#define MN_GETHMENU                     0x01E1
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

不使用這個參數。

</dd> <dt>

*lParam* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HMENU**

如果成功，則傳回值是目前視窗的 **HMENU** 。 如果失敗，則傳回值為 **Null**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



 

 





---
description: '\_ \_ 從 Windows 移除 TABLET 裝置時，會發佈 WM tablet DELETED 訊息。'
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: 'WM_TABLET_DELETED 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986333"
---
# <a name="wm_tablet_deleted-message"></a>WM \_ TABLET \_ DELETED 訊息

從 Windows 移除 TABLET 裝置時，會發佈 **WM \_ tablet \_ DELETED** 訊息。


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要移除的 tablet 裝置索引。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="remarks"></a>備註

這則訊息會傳送至系統中的所有最上層視窗，包括已停用或隱藏的無主視窗、重迭的視窗和快顯視窗;但是訊息不會傳送至子視窗。

在 *wParam* 中傳遞的索引與 [**ITabletManager：： GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) 方法所使用的索引相關。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                        |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>Tpcshrd。h</dt> </dl> |



 

 

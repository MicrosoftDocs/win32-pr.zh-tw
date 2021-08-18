---
title: 'TBN_MAPACCELERATOR (Commctrl 的通知碼) '
description: 要求工具列中對應至指定之快速鍵字元的按鈕索引。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434188"
---
# <a name="tbn_mapaccelerator-notification-code"></a>TBN \_ MAPACCELERATOR 通知碼

要求工具列中對應至指定之快速鍵字元的按鈕索引。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含快速鍵字元，並會接收對應按鈕的索引。 如果快速鍵未對應至命令， **dwItemNext** 欄位會是-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **NMCHAR. dwItemNext** 設定為值，則為 TRUE。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






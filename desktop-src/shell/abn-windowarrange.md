---
description: 通知 appbar，使用者已從工作列的快捷方式功能表中選取了 [Cascade]、[水準並排] 或 [垂直並排顯示] 命令。
title: 'ABN_WINDOWARRANGE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 27c679b7ccdb5eb92ebe87676cd136c71adcda862472f6f300056511001a683a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118225019"
---
# <a name="abn_windowarrange-message"></a>ABN \_ WINDOWARRANGE 訊息

通知 appbar，使用者已從工作列的快捷方式功能表中選取了 [Cascade]、[水準並排] 或 [垂直並排顯示] 命令。


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*fBeginning* 
</dt> <dd>

旗標，指定是否要開始串聯或磚作業。 如果作業正在啟動，而且 windows 尚未移動，這個參數就是 **TRUE** 。 如果作業已完成，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

系統會先傳送這則通知訊息，將 *lParam* 設為 **TRUE** ，然後將 *lParam* 設定為 **FALSE**。 第一個通知是在視窗進行串聯或並排顯示之前傳送，而第二個通知則是在發生 cascade 或磚作業之後傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





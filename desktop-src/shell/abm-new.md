---
description: 註冊新的 appbar，並指定系統應該用來傳送通知訊息的訊息識別碼。 Appbar 應該會在傳送任何其他 appbar 訊息之前傳送此訊息。
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: 'ABM_NEW 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400439e6808d40eb74c18fa4219109a0abca1973cdac4dcb9de5154384fd0071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460965"
---
# <a name="abm_new-message"></a>ABM \_ 新訊息

註冊新的 appbar，並指定系統應該用來傳送通知訊息的訊息識別碼。 Appbar 應該會在傳送任何其他 appbar 訊息之前傳送此訊息。


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其中包含新 appbar 的視窗控制碼和訊息識別碼。 傳送此訊息時，您必須指定 **cbSize**、 **hWnd** 和 **uCallbackMessage** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ; 如果發生錯誤或已註冊 appbar，則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





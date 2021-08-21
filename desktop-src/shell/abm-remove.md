---
description: 從系統的內部清單中移除 appbar，將其取消註冊。 系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。
title: 'ABM_REMOVE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c32fd2c7a12fc8146a01d3722b31b46bad01f61b526397806a5121b7381b069e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861705"
---
# <a name="abm_remove-message"></a>ABM \_ 移除訊息

從系統的內部清單中移除 appbar，將其取消註冊。 系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pabd* 
</dt> <dd>

[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其中包含要取消註冊之 appbar 的控制碼。 傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員;所有其他成員都會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

一律傳回 **TRUE**。

## <a name="remarks"></a>備註

這則訊息會導致系統將 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息傳送至所有透過像 appbars。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





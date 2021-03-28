---
description: 開啟或關閉全螢幕應用程式時，通知 appbar。 此通知是以應用程式定義的訊息形式傳送，此訊息是由 ABM 的 \_ 新訊息所設定。
title: 'ABN_FULLSCREENAPP 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112360"
---
# <a name="abn_fullscreenapp-message"></a>ABN \_ FULLSCREENAPP 訊息

開啟或關閉全螢幕應用程式時，通知 appbar。 此通知是以應用程式定義的訊息形式傳送，此訊息是由 ABM 的 [**\_ 新**](abm-new.md) 訊息所設定。


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*fOpen* 
</dt> <dd>

指定全螢幕應用程式是否開啟或關閉的旗標。 如果應用程式是開啟的，則此參數為 **TRUE** ，如果關閉，則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

開啟全螢幕應用程式時，appbar 必須放到迭置順序的底部。 當它關閉時，appbar 應該會還原其 z 順序位置。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Shellapi。h</dt> </dl> |



 

 





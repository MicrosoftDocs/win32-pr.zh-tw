---
title: 'TTN_LINKCLICK (Commctrl 的通知碼) '
description: 按一下氣球工具提示內的文字連結時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d3e76431-5b5f-4d67-8528-db21fd939917
keywords:
- TTN_LINKCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_LINKCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90be24910c2739b4495b651abf97156342d955b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995579"
---
# <a name="ttn_linkclick-notification-code"></a>TTN \_ LINKCLICK 通知碼

按一下氣球工具提示內的文字連結時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TTN_LINKCLICK
```



## <a name="parameters"></a>參數

此通知碼沒有任何參數。

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="remarks"></a>備註

以下是傳送此通知的範例。 假設您的氣球工具提示包含下列文字：「這是 <A>連結</A>」。 按一下 [連結] 時，工具提示控制項會傳送 TTN \_ LINKCLICK 通知碼。

> [!Note]  
> 若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






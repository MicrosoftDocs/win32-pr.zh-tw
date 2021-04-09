---
title: 'PSN_GETOBJECT (Prsht.idl 的通知碼) '
description: 由屬性工作表傳送，以在游標通過其中一個索引標籤控制項按鈕時，要求放置目標物件。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024800"
---
# <a name="psn_getobject-notification-code"></a>PSN \_ GETOBJECT 通知碼

由屬性工作表傳送，以在游標通過其中一個索引標籤控制項按鈕時，要求放置目標物件。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，該結構會在進入時包含通知碼的相關資訊。 如果已處理此通知程式碼，您必須將物件資訊插入此結構中。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此通知程式碼的應用程式必須傳回零。

## <a name="remarks"></a>備註

若要提供物件，應用程式必須在 *lParam* 的部分 [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的成員中設定值。 **PObject** 成員必須設定為有效的物件指標，且 **hResult** 成員必須設定為成功旗標。 為了符合元件物件模型 (COM) 標準，請在提供物件指標時，一律遞增物件的參考計數。

如果應用程式不提供物件，則必須將 **pObject** 設定為 **Null** ，並將 **hResult** 設定為失敗旗標。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

 






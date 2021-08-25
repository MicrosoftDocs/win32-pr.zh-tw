---
title: 'TBN_GETOBJECT (Commctrl 的通知碼) '
description: 由使用 TBSTYLE REGISTERDROP 樣式的工具列控制項所傳送， \_ 以在指標通過其按鈕時，要求放置目標物件。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c50f3d403089ca7db42ab89232e57d68121424c066914c534ba13a826adb8ea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876728"
---
# <a name="tbn_getobject-notification-code"></a>TBN \_ GETOBJECT 通知碼

由使用 [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) 樣式的工具列控制項所傳送，以在指標通過其按鈕時，要求放置目標物件。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的指標，其中包含指標所傳遞之按鈕的相關資訊，並接收應用程式提供的資料，以回應此通知碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

處理此通知程式碼的應用程式必須傳回零。

## <a name="remarks"></a>備註

若要提供物件，應用程式必須在 *lParam* 的部分 [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify)結構的成員中設定值。 **PObject** 成員必須設定為有效的物件指標，且 **hResult** 成員必須設定為成功旗標。 為了符合元件物件模型 (COM) 標準，請在提供物件指標時，一律遞增物件的參考計數。

如果應用程式不提供物件，則必須將 **pObject** 設定為 **Null** ，並將 **hResult** 設定為失敗旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'HDN_ENDDRAG (Commctrl 的通知碼) '
description: 當拖曳作業在其中一個專案上結束時，由標題控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。 只有設定為 HDS System.windows.dragdrop.drop> 樣式的標題控制項才會 \_ 傳送此通知碼。
ms.assetid: a28df985-73f1-4fc7-a1db-81a86a131c06
keywords:
- HDN_ENDDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05df56beb0b5b4a75716723330711714b7db9f4f27100ffe3296626d2be5798a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544614"
---
# <a name="hdn_enddrag-notification-code"></a>HDN \_ ENDDRAG 通知碼

當拖曳作業在其中一個專案上結束時，由標題控制項所傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。


```C++
HDN_ENDDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含所要拖曳之標頭專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要允許控制項自動放置和重新排序專案，請傳回 **FALSE**。 若要避免放置專案，請傳回 **TRUE**。

## <a name="remarks"></a>備註

如果擁有者正在執行外部 (手動) 拖放管理，它必須傳回 **FALSE**。 然後，擁有者必須藉由傳送 [**HDM \_ SETITEM**](hdm-setitem.md) 或 [**HDM \_ SETORDERARRAY**](hdm-setorderarray.md)，手動重新排序標頭專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






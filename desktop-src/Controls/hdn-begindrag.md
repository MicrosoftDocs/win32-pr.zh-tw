---
title: 'HDN_BEGINDRAG (Commctrl 的通知碼) '
description: 當拖曳作業在其中一個專案上開始時，由標題控制項所傳送。 只有設定為 HDS System.windows.dragdrop.drop> 樣式的標題控制項才會傳送此通知碼 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- HDN_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025028"
---
# <a name="hdn_begindrag-notification-code"></a>HDN \_ BEGINDRAG 通知碼

當拖曳作業在其中一個專案上開始時，由標題控制項所傳送。 只有設定為 [**HDS \_ system.windows.dragdrop.drop>**](header-control-styles.md) 樣式的標題控制項才會傳送此通知碼。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含正在拖曳之標頭專案的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要允許標題控制項自動管理拖放作業，請傳回 **FALSE**。 如果控制項的擁有者以手動方式執行拖放重新排列，則傳回 **TRUE**。

## <a name="remarks"></a>備註

標題控制項預設會自動管理拖放重新排列。 傳回 **TRUE** 表示外部 (手動) 拖放管理可讓控制項的擁有者在拖放程式中提供自訂的服務。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






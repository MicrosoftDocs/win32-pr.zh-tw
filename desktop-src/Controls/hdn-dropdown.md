---
title: 'HDN_DROPDOWN (Commctrl 的通知碼) '
description: 當按一下標題控制項上的下拉箭號時，由標題控制項傳送至其父代。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844488"
---
# <a name="hdn_dropdown-notification-code"></a>HDN \_ 下拉式通知碼

當按一下標題控制項上的下拉箭號時，由標題控制項傳送至其父代。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

「語法」一節中的範例會顯示通知接收者如何轉換 **LPARAM** 以取得 [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) 結構。 **WPARAM** 包含傳送此訊息之控制項的識別碼。

只有在 \_ 標題專案上設定 STYLE HDF SPLITBUTTON 時，才會傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






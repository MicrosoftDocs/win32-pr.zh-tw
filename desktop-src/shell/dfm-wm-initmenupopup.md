---
description: DFM_WM_INITMENUPOPUP 訊息-在下拉式功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。
title: 'DFM_WM_INITMENUPOPUP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 314e83f7-839d-4ca0-b5c1-842c5bf14923
api_name:
- DFM_WM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9df2700403dcdc0ce00b6d90d9c3a87d373b0a34
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096996"
---
# <a name="dfm_wm_initmenupopup-message"></a>DFM \_ WM \_ INITMENUPOPUP 訊息

當下拉功能表或子功能表即將變成作用中時傳送。 這可讓應用程式在功能表顯示前修改功能表，而不需要變更整個功能表。


```C++
DFM_WM_INITMENUPOPUP 

    wParam = (WPARAM);

    lParam = (LPARAM);

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

下拉式功能表或子功能表的控制碼。

</dd> <dt>

*lParam* \[在\]
</dt> <dd>

低序位字組會指定開啟下拉式功能表或子功能表之功能表項目的以零為起始的相對位置。

高序位單字指出下拉式功能表是否為 [視窗] 功能表。 如果功能表是 [視窗] 功能表，此參數為 **TRUE**;否則為 **FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果應用程式處理此訊息，它應該會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 





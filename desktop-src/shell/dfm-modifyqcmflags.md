---
description: 允許回呼修改 \_ 傳遞給 ICoNtextMenu：： QueryCoNtextMenu 的 CFM XXX 值。
title: 'DFM_MODIFYQCMFLAGS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847793"
---
# <a name="dfm_modifyqcmflags-message"></a>DFM \_ MODIFYQCMFLAGS 訊息

允許回呼修改 \_ 傳遞給 [**ICoNtextMenu：： QUERYCONTEXTMENU**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)的 CFM XXX 值。


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*puNewFlags* \[在\]
</dt> <dd>

新旗標值的指標。

</dd> <dt>

*uFlags* \[在\]
</dt> <dd>

指定如何變更內容功能表的旗標。 此參數會使用 \_ [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)中所述的 CMF XXX 值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 





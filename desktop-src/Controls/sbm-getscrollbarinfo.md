---
title: 'SBM_GETSCROLLBARINFO 訊息 (Winuser .h) '
description: 由應用程式傳送以取得指定捲軸的相關資訊。
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- SBM_GETSCROLLBARINFO message Windows 控制項
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685876"
---
# <a name="sbm_getscrollbarinfo-message"></a>SBM \_ GETSCROLLBARINFO 訊息

由應用程式傳送以取得指定捲軸的相關資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

接收資訊之 [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**GetScrollBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 


---
title: 'TB_MAPACCELERATOR 訊息 (Commctrl .h) '
description: 判斷對應至指定快速鍵的按鈕識別碼。
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168082"
---
# <a name="tb_mapaccelerator-message"></a>TB \_ MAPACCELERATOR 訊息

判斷對應至指定快速鍵的按鈕識別碼。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

快速鍵字元。

</dd> <dt>

*lParam* \[擴展\]
</dt> <dd>

**UINT** 的指標。 傳回時，如果成功，此參數將會保留 *wParam* 為其快速鍵的按鈕的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果其中一個按鈕的 *wParam* 為其快速鍵，則會傳回非零值，否則會傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_MAPACCELERATORW** (Unicode) 和 **TB \_ MAPACCELERATORA** (ANSI) <br/>       |



 

 






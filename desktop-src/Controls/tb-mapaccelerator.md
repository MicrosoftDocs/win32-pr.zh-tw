---
title: 'TB_MAPACCELERATOR 訊息 (Commctrl .h) '
description: 判斷對應至指定快速鍵的按鈕識別碼。
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR message Windows 控制項
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
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686197"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TB \_MAPACCELERATORW** (Unicode) 和 **TB \_ MAPACCELERATORA** (ANSI) <br/>       |



 

 






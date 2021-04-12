---
title: 'LVM_GETHEADER 訊息 (Commctrl .h) '
description: 取得清單視圖控制項所使用之標題控制項的控制碼。 您可以明確地傳送此訊息，或使用 ListView \_ messageheaders 宏。
ms.assetid: 4708b493-4449-4844-bf0d-e6969bcf0246
keywords:
- LVM_GETHEADER message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETHEADER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d53082092118cad373005743849498791f0e1ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024664"
---
# <a name="lvm_getheader-message"></a>LVM \_ messageheaders 訊息

取得清單視圖控制項所使用之標題控制項的控制碼。 您可以明確地傳送此訊息，或使用 [**ListView \_ messageheaders**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getheader) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

將控制碼傳回至標題控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






---
title: 'EM_EXSETSEL 訊息 (Richedit .h) '
description: 在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL message Windows 控制項
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843820"
---
# <a name="em_exsetsel-message"></a>EM \_ EXSETSEL 訊息

在 Microsoft Rich Edit 控制項中，選取 (COM) 物件的字元或元件物件模型範圍。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

指定選取範圍的 [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是實際設定的選取專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 






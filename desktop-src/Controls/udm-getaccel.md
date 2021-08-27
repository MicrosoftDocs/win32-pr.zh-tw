---
title: 'UDM_GETACCEL 訊息 (Commctrl .h) '
description: 抓取上下按鈕控制項的加速資訊。
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3603f364a6caa4f4726460e4b5b71e0d79564fbe9178414576fbed2ce5f5777d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132188"
---
# <a name="udm_getaccel-message"></a>UDM \_ GETACCEL 訊息

抓取上下按鈕控制項的加速資訊。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

*LParam* 所指定陣列中的元素數目。

</dd> <dt>

*lParam* 
</dt> <dd>

接收加速資訊之 [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) 結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是目前為控制項設定的快速鍵數目。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UDM \_ SETACCEL**](udm-setaccel.md)
</dt> </dl>

 

 






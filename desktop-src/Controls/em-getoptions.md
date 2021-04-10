---
title: 'EM_GETOPTIONS 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項選項。
ms.assetid: 183f0fed-8666-4ed5-ac48-362c818378d2
keywords:
- EM_GETOPTIONS message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b31af3663331b63553fc262fc9bdbd5613c5768
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934729"
---
# <a name="em_getoptions-message"></a>EM \_ GETOPTIONS 訊息

抓取 rich edit 控制項選項。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回 [**EM \_ >setoptions**](em-setoptions.md) 訊息中所述之目前選項旗標值的組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ >SETOPTIONS**](em-setoptions.md)
</dt> </dl>

 

 






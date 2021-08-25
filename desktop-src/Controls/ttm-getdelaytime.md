---
title: 'TTM_GETDELAYTIME 訊息 (Commctrl .h) '
description: 抓取目前針對工具提示控制項設定的初始、快顯和 reshow 持續時間。
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0e63eca126477a6f602e6e23be75495319d30aa2814d2d72b8426a96c078326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769258"
---
# <a name="ttm_getdelaytime-message"></a>TTM \_ GETDELAYTIME 訊息

抓取目前針對工具提示控制項設定的初始、快顯和 reshow 持續時間。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

旗標，指定將取出的持續時間值。 這個參數的值可以是下列其中一個：



| 值                                                                                                                                                      | 意義                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | 如果指標在工具周框內是固定的，則取得工具提示視窗保持可見的時間量。<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ 初始**</dt> </dl> | 在出現工具提示視窗之前，取出指標在工具的周框中必須保持靜止的時間量。<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>    | 取得當指標從某個工具移至另一個工具時，後續工具提示視窗顯示所需的時間量。<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

使用指定的持續時間（以毫秒為單位）傳回和 INT 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)
</dt> </dl>

 

 






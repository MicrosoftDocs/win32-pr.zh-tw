---
title: 'TVM_HITTEST 訊息 (Commctrl .h) '
description: 判斷指定點相對於樹狀檢視控制項工作區的位置。 您可以使用 TreeView System.windows.media.visualtreehelper.hittest 宏明確地傳送此訊息 \_ 。
ms.assetid: 18ea3737-f429-4c10-9133-3b5729aa36fa
keywords:
- TVM_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564b6d82c04c0d007784aac39284db13b3776267d524d2f615353ede50eb945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060148"
---
# <a name="tvm_hittest-message"></a>TVM \_ system.windows.media.visualtreehelper.hittest 訊息

判斷指定點相對於樹狀檢視控制項工作區的位置。 您可以使用 [**TreeView \_ system.windows.media.visualtreehelper.hittest**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_hittest) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**TVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-tvhittestinfo)結構的指標。 傳送訊息時， **pt** 成員會指定要測試之點的座標。 當訊息傳回時， **hItem** 成員是位於指定點之專案的控制碼; 如果沒有任何專案佔用點，則為 **Null** 。 此外，當訊息傳回時， **旗標** 成員是點擊測試值，指出指定點的位置。 如需點擊測試值的清單，請參閱 **TVHITTESTINFO** 結構的描述。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回佔據指定點之樹狀檢視專案的控制碼; 如果沒有任何專案佔用點，則為 **Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






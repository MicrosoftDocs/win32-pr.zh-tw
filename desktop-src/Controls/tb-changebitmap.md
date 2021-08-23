---
title: 'TB_CHANGEBITMAP 訊息 (Commctrl .h) '
description: 變更工具列中按鈕的點陣圖。
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb75e4586960a68e68c52d01d19ad78a3b3c848dcfb7acbd495dffbe530770c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957937"
---
# <a name="tb_changebitmap-message"></a>TB \_ CHANGEBITMAP 訊息

變更工具列中按鈕的點陣圖。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要接收新點陣圖之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

工具列影像清單中影像以零為起始的索引。 系統會在按鈕中顯示指定的影像。 將此參數設定為 I \_ IMAGECALLBACK，工具列會傳送 [**TBN \_ GETDISPINFO**](tbn-getdispinfo.md) 通知，以在需要時取出影像索引。

[版本 5.81](common-control-versions.md)。 將此參數設定為 I \_ IMAGENONE，表示按鈕沒有影像。 按鈕配置不會包含任何點陣圖的空間，只會包含文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






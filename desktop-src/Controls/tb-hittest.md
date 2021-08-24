---
title: 'TB_HITTEST 訊息 (Commctrl .h) '
description: 判中斷點位於工具列控制項中的位置。
ms.assetid: d08f3805-2042-470e-8f5a-8a6a681d1189
keywords:
- TB_HITTEST 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d89cecf1d1df5c370ab9a00ae1251df9df7ef919f9959b998407a9fb5881178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696158"
---
# <a name="tb_hittest-message"></a>TB \_ system.windows.media.visualtreehelper.hittest 訊息

判中斷點位於工具列控制項中的位置。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含 **x** 成員中點擊測試的 x 座標，以及 **y** 成員中點擊測試的 y 座標。 座標是相對於工具列的工作區。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值。 如果傳回值為零或正值，則為點所在之 nonseparator 專案的以零為基底的索引。 如果傳回值為負數，則點不在按鈕中。 傳回值的絕對值是分隔符號專案或最接近 nonseparator 專案的索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 


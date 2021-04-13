---
title: 'EM_GETWORDWRAPMODE 訊息 (Richedit .h) '
description: 取得 rich edit 控制項的目前文字換行和斷詞選項。
ms.assetid: a87d80d6-2e9e-40ba-9348-a1cc1ef8ec10
keywords:
- EM_GETWORDWRAPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efc8a2b6d17623964eb0d3714c1c099f47fc788a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464541"
---
# <a name="em_getwordwrapmode-message"></a>EM \_ GETWORDWRAPMODE 訊息

取得 rich edit 控制項的目前文字換行和斷詞選項。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本的 Rich Edit 都不支援此功能。

 

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

訊息會傳回目前的自動換行和斷詞選項。

## <a name="remarks"></a>備註

此訊息不得由應用程式定義的斷詞程式傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 






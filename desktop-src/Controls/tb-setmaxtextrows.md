---
title: 'TB_SETMAXTEXTROWS 訊息 (Commctrl .h) '
description: 設定工具列按鈕上顯示之文字資料列的最大數目。
ms.assetid: a14d74e8-cc21-482d-9bca-38dc7c0528ec
keywords:
- TB_SETMAXTEXTROWS message Windows 控制項
topic_type:
- apiref
api_name:
- TB_SETMAXTEXTROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0984c0b73280ec90c4e659d3bb3b4cc89cdcf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934094"
---
# <a name="tb_setmaxtextrows-message"></a>TB \_ SETMAXTEXTROWS 訊息

設定工具列按鈕上顯示之文字資料列的最大數目。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

可顯示之文字的最大資料列數。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

若要讓文字換行，您必須藉由傳送 [**TB \_ SETBUTTONWIDTH**](tb-setbuttonwidth.md) 訊息來設定最大按鈕寬度。 文字會在字組分隔處換行;\\文字中的 "n" )  ( 的分行符號會被忽略。 TBSTYLE 清單工具列中的文字 \_ 一律會顯示在同一行上。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






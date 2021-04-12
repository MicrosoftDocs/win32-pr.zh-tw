---
title: 'RB_IDTOINDEX 訊息 (Commctrl .h) '
description: 將帶狀識別碼轉換為 Rebar 控制項中的寬線索引。
ms.assetid: vs|controls|~\controls\rebar\messages\rb_idtoindex.htm
keywords:
- RB_IDTOINDEX message Windows 控制項
topic_type:
- apiref
api_name:
- RB_IDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7acd85862bc4787a6b32d2fdd3c897a52913b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464393"
---
# <a name="rb_idtoindex-message"></a>RB \_ IDTOINDEX 訊息

將帶狀識別碼轉換為 Rebar 控制項中的寬線索引。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

有問題之帶狀的應用程式定義識別碼。 這是插入寬線時，在 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa)結構的 **wID** 成員中傳遞的值。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回以零為基底的帶索引，否則為-1。 如果有重複的頻外識別碼，就會傳回第一個。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 






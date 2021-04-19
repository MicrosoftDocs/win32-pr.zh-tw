---
title: 'CBEM_INSERTITEM 訊息 (Commctrl .h) '
description: 在 ComboBoxEx 控制項中插入新專案。
ms.assetid: c99db676-204d-44c9-aaa3-81b70fe2cf44
keywords:
- CBEM_INSERTITEM message Windows 控制項
topic_type:
- apiref
api_name:
- CBEM_INSERTITEM
- CBEM_INSERTITEMA
- CBEM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23e6cb26a575472e53703d65e407a94a024dcfac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976977"
---
# <a name="cbem_insertitem-message"></a>CBEM \_ INSERTITEM 訊息

在 ComboBoxEx 控制項中插入新專案。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema)結構的指標，其中包含要插入之專案的相關資訊。 傳送訊息時，必須設定 **iItem** 成員，以表示要插入專案的以零為基底的索引。 若要在清單結尾插入專案，請將 **iItem** 成員設定為-1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回插入新專案的索引，否則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **CBEM \_INSERTITEMW** (Unicode) 和 **CBEM \_ INSERTITEMA** (ANSI) <br/>           |



 

 






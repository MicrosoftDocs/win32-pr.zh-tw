---
title: 'BCM_GETNOTE 訊息 (Commctrl .h) '
description: 取得與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用按鈕 \_ GetNote 宏。
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b552f79e1d6c7bda2808b99701ff11e45deb169232b8bb52c4ecf231cdcbfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921698"
---
# <a name="bcm_getnote-message"></a>BCM \_ GETNOTE 訊息

取得與命令連結按鈕相關聯的備註文字。 您可以明確地傳送此訊息，或使用 [**按鈕 \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[in、out\]
</dt> <dd>

**DWORD** ，指定 *lParam* 所指向的緩衝區大小（以字元為單位）。

</dd> <dt>

*lParam* \[擴展\]
</dt> <dd>

要接收文字的字串緩衝區。 緩衝區必須夠大，才能容納終止的 Null 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果訊息成功，則會傳回 **TRUE**。 否則會傳回 **FALSE**。

## <a name="remarks"></a>備註

**BCM \_ GETNOTE** 訊息只適用于具有 [**BS \_ COMMANDLINK**](button-styles.md)或 [**BS \_ DEFCOMMANDLINK**](button-styles.md)按鈕樣式的按鈕。

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 將包含：

-   \_ \_ 如果按鈕沒有 [**BS \_ DEFCOMMANDLINK**](button-styles.md)或 [**BS \_ COMMANDLINK**](button-styles.md)樣式，則不支援錯誤。
-   \_緩衝區不足 \_ ，如果 *lParam* 緩衝區太小，則為錯誤。 *WParam* 參數將包含所需的緩衝區大小（以字元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[按鈕樣式](button-styles.md)
</dt> <dt>

**概念**
</dt> <dt>

[按鈕類型](button-types-and-styles.md)
</dt> </dl>

 

